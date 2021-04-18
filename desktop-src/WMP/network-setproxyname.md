---
title: Metodo Network. seproxyname
description: Il metodo seproxyname specifica il nome del server proxy da usare. | Metodo Network. seproxyname
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- Metodo seproxyname Media Player Windows
- Metodo seproxyname Media Player Windows, classe di rete
- Classe di rete Windows Media Player, metodo seproxyname
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
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329305"
---
# <a name="networksetproxyname-method"></a>Metodo Network. seproxyname

Il metodo **Seproxyname** specifica il nome del server proxy da usare.

## <a name="syntax"></a>Sintassi


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ di in\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** che specifica il nome del server proxy da utilizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **Seproxyname** per specificare il nome del server proxy di Windows Media Player per il protocollo MMS. Il nuovo nome viene recuperato da un elemento di testo HTML con ID = "NAME". L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





