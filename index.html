exports.handler = async (event) => {
  if (event.httpMethod === 'OPTIONS') {
    return {
      statusCode: 200,
      headers: {
        'Access-Control-Allow-Origin': '*',
        'Access-Control-Allow-Headers': 'Content-Type'
      },
      body: ''
    };
  }

  try {
    const { url } = event.queryStringParameters || {};
    if (!url) return { statusCode: 400, body: JSON.stringify({ error: 'Missing url' }) };

    const realUrl = decodeURIComponent(url).replace('VLUCHT_KEY', process.env.FLIGHTAPI_KEY);
    console.log('Fetching:', realUrl.replace(process.env.FLIGHTAPI_KEY, '***'));

    const response = await fetch(realUrl);
    const text = await response.text();
    
    return {
      statusCode: 200,
      headers: {
        'Content-Type': 'application/json',
        'Access-Control-Allow-Origin': '*'
      },
      body: text
    };
  } catch (err) {
    console.error('Flights error:', err);
    return {
      statusCode: 500,
      headers: { 'Access-Control-Allow-Origin': '*' },
      body: JSON.stringify({ error: err.message })
    };
  }
};
