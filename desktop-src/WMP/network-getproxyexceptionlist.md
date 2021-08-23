---
title: Metodo Network.getProxyExceptionList
description: Il metodo getProxyExceptionList recupera l'elenco di eccezioni proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- Metodo getProxyExceptionList Windows Media Player
- Metodo getProxyExceptionList Windows Media Player , classe Network
- Classe di rete Windows Media Player, metodo getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2becc6c74a5ada575f1bfa85473bd3204bf53a4a739640149cffdd57e3facf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054574"
---
# <a name="networkgetproxyexceptionlist-method"></a>Metodo Network.getProxyExceptionList

Il **metodo getProxyExceptionList** recupera l'elenco di eccezioni proxy.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco dei protocolli supportati, vedere [Protocolli e tipi di file supportati.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore String** che specifica un elenco delimitato da punto e virgola degli host per i quali il server proxy viene ignorato. Il valore restituito è significativo solo quando **getProxySettings** restituisce un valore di due (usare le impostazioni manuali).

## <a name="remarks"></a>Commenti

Si tratta di un elenco di computer, domini e/o indirizzi che ignorano il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce dell'elenco.

Il \* carattere può essere usato come carattere jolly per elencare le voci. Ad esempio, .com corrisponderebbe a tutti gli host nel dominio com, mentre 67. corrisponderebbe a tutti gli host nella \* subnet A di classe \* 67.

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **getProxyExceptionList** per visualizzare gli elenchi di proxy ignorati per i protocolli MMS e HTTP. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Di rete**](network-object.md)
</dt> <dt>

[**Network.getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





