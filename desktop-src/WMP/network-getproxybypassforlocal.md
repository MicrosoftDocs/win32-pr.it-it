---
title: Metodo Network. getProxyBypassForLocal
description: Il metodo getProxyBypassForLocal recupera un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- Metodo getProxyBypassForLocal Windows Media Player
- Metodo getProxyBypassForLocal Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327483"
---
# <a name="networkgetproxybypassforlocal-method"></a>Metodo Network. getProxyBypassForLocal

Il metodo **getProxyBypassForLocal** recupera un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ di in\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano** che indica se il server proxy viene ignorato. Il valore restituito è significativo solo quando **getProxySettings** restituisce un valore pari a due (usare impostazioni manuali).

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **getProxyBypassForLocal** per visualizzare se Windows Media Player è impostato in modo da ignorare il server proxy per gli indirizzi locali. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Rete. getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





