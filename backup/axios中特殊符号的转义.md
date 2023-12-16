请求参数在url上需要转义，如果手动转义后传进request中的params中，会出现转义多一次的情况

解决方法是先转义后直接拼接在url上调用

function param(json) {
  if (!json) return '';
  return cleanArray(
    Object.keys(json).map((key) => {
      if (json[key] === undefined) return '';
      return encodeURIComponent(key) + '=' + encodeURIComponent(json[key]);
    })
  ).join('&');
}


function rejectTestOrder(id: any, params: { description: string }) {
  const stringParam = param(params);
  const url = `/qixiao/v1/test-orders/${id}/reject?${stringParam}`;
  return request({
    url: url,
    method: 'put'
  });
}