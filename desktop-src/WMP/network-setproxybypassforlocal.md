---
title: Metodo Network. setProxyBypassForLocal
description: Il metodo setProxyBypassForLocal specifica un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- Metodo setProxyBypassForLocal Windows Media Player
- Metodo setProxyBypassForLocal Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo setProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328713"
---
# <a name="networksetproxybypassforlocal-method"></a>Metodo Network. setProxyBypassForLocal

Il metodo **setProxyBypassForLocal** specifica un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.

## <a name="syntax"></a>Sintassi


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ di in\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> <dt>

*Ignora* \[ in\]
</dt> <dd>

**Valore booleano** che specifica se il server proxy viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **setProxyBypassForLocal** consente di specificare se il server proxy di Windows Media Player viene ignorato, quando si utilizza il protocollo MMS se il server di origine si trova in una rete locale. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
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

 

 





