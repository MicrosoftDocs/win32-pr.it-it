---
title: Metodo Network.setProxyName
description: Il metodo setProxyName specifica il nome del server proxy da usare. | Metodo Network.setProxyName
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- Metodo setProxyName Windows Media Player
- Metodo setProxyName Windows Media Player , classe Network
- Classe di rete Windows Media Player, metodo setProxyName
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9831b25e37fd6e19b70c1ee2589736394560c97f841b5d18c3a128a82997cc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134924"
---
# <a name="networksetproxyname-method"></a>Metodo Network.setProxyName

Il **metodo setProxyName** specifica il nome del server proxy da usare.

## <a name="syntax"></a>Sintassi


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco dei protocolli supportati, vedere [Protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il nome del server proxy da utilizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non ha alcun effetto a meno **che getProxySettings non** restituisca il valore 2 (usare le impostazioni manuali).

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **setProxyName** per specificare il nome del Windows Media Player proxy per il protocollo MMS. Il nuovo nome viene recuperato da un elemento HTML TEXT con ID = "NAME". **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





