---
title: Player. versionInfo
description: La proprietà versionInfo recupera un valore stringa che specifica la versione di Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player. versionInfo Windows Media Player
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
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327056"
---
# <a name="playerversioninfo"></a>Player. versionInfo

La proprietà **VERSIONINFO** recupera un valore stringa che specifica la versione di Windows Media Player.

## <a name="syntax"></a>Sintassi

*Player* . **VERSIONINFO**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura nel formato seguente: "*X*. 0,0. *Aaaa*"dove *X* rappresenta il numero di versione principale e *aaaa* rappresenta il numero di Build.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando selezionato, Visualizza una finestra di messaggio contenente le informazioni sulla versione di Windows Media Player. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





