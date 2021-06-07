---
title: UI_PKEY_FontProperties_Bold
description: Identifica la proprietà \_ FontProperties Bold PKEY \_ \_ dell'interfaccia utente.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444382"
---
# <a name="ui_pkey_fontproperties_bold"></a>UI \_ PKEY \_ FontProperties \_ Bold

Identifica la proprietà \_ FontProperties Bold PKEY \_ \_ dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Commenti

UI \_ PKEY \_ FontProperties \_ Bold viene usato da un'applicazione per eseguire query sullo stato del **pulsante** Grassetto.

Il valore della proprietà deriva dall'enumerazione [**\_ FONTPROPERTIES dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) utente.

Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.

La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.



|      Proprietà                    |    Risultato dell'interfaccia utente                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Il pulsante** Grassetto è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTPROPERTIES_NOTSET`       | **Il pulsante** Grassetto non è selezionato.                                    |
| `UI_FONTPROPERTIES_SET`          | **Il pulsante** Grassetto è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**PROPRIETÀ CARATTERE \_ DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controllo Font](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 