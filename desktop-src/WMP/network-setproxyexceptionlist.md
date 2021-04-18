---
title: Metodo Network. setProxyExceptionList
description: Il metodo setProxyExceptionList specifica l'elenco di eccezioni del proxy. | Metodo Network. setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- Metodo setProxyExceptionList Windows Media Player
- Metodo setProxyExceptionList Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324378"
---
# <a name="networksetproxyexceptionlist-method"></a>Metodo Network. setProxyExceptionList

Il metodo **setProxyExceptionList** specifica l'elenco di eccezioni del proxy.

## <a name="syntax"></a>Sintassi


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ di in\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> <dt>

*elenco* \[ di in\]
</dt> <dd>

**Stringa** che specifica un elenco delimitato da punti e virgola di host per i quali il server proxy viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Si tratta di un elenco di computer, domini e/o indirizzi che ignoreranno il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce nell'elenco.

Il \* carattere può essere usato come carattere jolly per elencare le voci. Ad esempio, \* . com corrisponde a tutti gli host nel dominio com, mentre 67. \* corrisponderebbe a tutti gli host della classe 67 una subnet.

Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **setProxyExceptionList** per specificare un elenco di host per cui il server proxy viene ignorato quando si utilizza il protocollo MMS. Il nuovo elenco viene recuperato da un elemento di testo HTML con ID = "XLIST". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





