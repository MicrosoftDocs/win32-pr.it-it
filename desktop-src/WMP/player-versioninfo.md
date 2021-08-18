---
title: Player.versionInfo
description: La proprietà versionInfo recupera un valore String che specifica la versione del Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player.versionInfo Windows Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2251d610ad8a522155e37c8d416123c9d09faef5da2b4af4da75aeb745940f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995831"
---
# <a name="playerversioninfo"></a>Player.versionInfo

La **proprietà versionInfo** recupera un valore String che specifica la versione del Windows Media Player.

## <a name="syntax"></a>Sintassi

*lettore* . **versionInfo**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **sola** lettura nel formato seguente: "*X*.0.0. *AAAA*" dove *X* rappresenta il numero di versione principale e *AAAA rappresenta* il numero di build.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando si fa clic, visualizza una finestra di messaggio contenente le informazioni sulla versione per Windows Media Player. **L'oggetto** Player è stato creato con ID = "Player".


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





