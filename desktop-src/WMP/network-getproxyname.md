---
title: Metodo Network.getProxyName
description: Il metodo getProxyName recupera il nome del server proxy in uso.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- Metodo getProxyName Windows Media Player
- Metodo getProxyName Windows Media Player , classe Network
- Classe di rete Windows Media Player, metodo getProxyName
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f40eb7eb695376768cd8168e1eb1d1916c8e84e6ede8ef93251df6097a15d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647451"
---
# <a name="networkgetproxyname-method"></a>Metodo Network.getProxyName

Il **metodo getProxyName** recupera il nome del server proxy in uso.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Network.getProxyName(
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

Questo metodo restituisce un **valore String** contenente il nome del server proxy in uso. Il valore restituito è significativo solo quando **getProxySettings** restituisce il valore 2 (usare le impostazioni manuali).

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **getProxyName per** visualizzare i Windows Media Player server proxy per i protocolli HTTP e MMS. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

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

 

 





