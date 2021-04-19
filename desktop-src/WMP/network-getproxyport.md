---
title: Metodo Network. getProxyPort
description: Il metodo getProxyPort recupera la porta proxy utilizzata.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- Metodo getProxyPort Windows Media Player
- Metodo getProxyPort Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326330"
---
# <a name="networkgetproxyport-method"></a>Metodo Network. getProxyPort

Il metodo **getProxyPort** recupera la porta proxy utilizzata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Network.getProxyPort(
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

Questo metodo restituisce un **numero** (**Long**) che contiene la porta proxy utilizzata. Il valore restituito è significativo solo quando **getProxySettings** restituisce un valore pari a due (usare impostazioni manuali).

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **getProxyPort** per visualizzare i numeri di porta proxy di Windows Media Player correnti per i protocolli MMS e http. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

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

 

 





