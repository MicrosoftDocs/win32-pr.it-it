---
title: Metodo Network. setProxyPort
description: Il metodo setProxyPort specifica la porta proxy da usare. | Metodo Network. setProxyPort
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- Metodo setProxyPort Windows Media Player
- Metodo setProxyPort Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324088"
---
# <a name="networksetproxyport-method"></a>Metodo Network. setProxyPort

Il metodo **setProxyPort** specifica la porta proxy da usare.

## <a name="syntax"></a>Sintassi


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ di in\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> <dt>

*porta* \[ in\]
</dt> <dd>

**Numero** (**Long**) che specifica la porta del proxy da usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **setProxyPort** per specificare il numero di porta del proxy di Windows Media Player per il protocollo MMS. Il numero di porta viene recuperato da un elemento INPUT HTML con ID = "PORT". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
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

 

 





