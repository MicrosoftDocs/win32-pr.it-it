---
title: Metodo Network.setProxySettings
description: Il metodo setProxySettings specifica l'impostazione proxy per un protocollo specificato.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- Metodo setProxySettings Windows Media Player
- Metodo setProxySettings Windows Media Player , classe Network
- Classe di rete Windows Media Player, metodo setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6501d097a4ec342c2831e4b72bf8f17edc4e4e1bec02b2b51cd7840325674b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573859"
---
# <a name="networksetproxysettings-method"></a>Metodo Network.setProxySettings

Il **metodo setProxySettings** specifica l'impostazione proxy per un protocollo specificato.

## <a name="syntax"></a>Sintassi


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*protocollo* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il nome del protocollo. Per un elenco dei protocolli supportati, vedere [Protocolli e tipi di file supportati.](supported-protocols-and-file-types.md)

</dd> <dt>

*impostazione* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente uno dei valori seguenti.



| Valore | Descrizione                                                          |
|-------|----------------------------------------------------------------------|
| 0     | Non usare un server proxy.                                           |
| 1     | Usare le impostazioni proxy del browser corrente (valido solo per HTTP). |
| 2     | Usare le impostazioni proxy specificate manualmente.                           |
| 3     | Rilevare automaticamente le impostazioni del proxy.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene JScript con un elemento HTML SELECT per consentire all'utente di specificare l Windows Media Player **proxy per il protocollo HTTP. L'oggetto Player** è stato creato con ID = "Player".


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

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

 

 





