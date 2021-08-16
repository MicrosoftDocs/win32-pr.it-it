---
title: Metodo Network.getProxySettings
description: Il metodo getProxySettings recupera l'impostazione proxy per un protocollo specificato.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- Metodo getProxySettings Windows Media Player
- Metodo getProxySettings Windows Media Player , classe Network
- Classe di rete Windows Media Player, metodo getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e142e7366c9e2b03e55dbd3768ee9c4fb41f30266d221a2ac5ac80019d5a7b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647441"
---
# <a name="networkgetproxysettings-method"></a>Metodo Network.getProxySettings

Il **metodo getProxySettings** recupera l'impostazione proxy per un protocollo specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Network.getProxySettings(
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

Questo metodo restituisce un **valore Number** (**long**) contenente uno dei valori seguenti.



| Valore | Descrizione                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Non è in uso un server proxy.                                                |
| 1     | Vengono usate le impostazioni proxy per il browser corrente (valide solo per HTTP). |
| 2     | Vengono usate le impostazioni proxy specificate manualmente.                            |
| 3     | Le impostazioni proxy vengono rilevate automaticamente.                                      |



 

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **getProxySettings** per visualizzare un messaggio, che fornisce informazioni sulle impostazioni proxy correnti del lettore, nella finestra del browser. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Di rete**](network-object.md)
</dt> </dl>

 

 





