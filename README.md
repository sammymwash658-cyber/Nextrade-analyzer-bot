# Nextrade-analyzer-bot
 function getLastDigit(tick) {   const precision = Number(tick.pip_size);    if (!Number.isInteger(precision) ||       precision &lt; 0 || precision > 10) {     return null;   }    const quote = Number(tick.quote);   if (!Number.isFinite(quote)) return null;    const displayed = quote.toFixed(precision);   return Number(displayed.slice(-1)); }
