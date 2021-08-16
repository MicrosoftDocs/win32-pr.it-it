---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la proprietà \_ FontProperties Strikethrough PKEY \_ \_ dell'interfaccia utente.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746172ec2209861615375e73dee3f2336950a2dd93e76b33893190e9f7e8bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850307"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>UI \_ PKEY \_ FontProperties \_ Strikethrough

Identifica la proprietà \_ FontProperties Strikethrough PKEY \_ \_ dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Commenti

UI \_ PKEY \_ FontProperties \_ Strikethrough viene usato da un'applicazione per eseguire query sullo stato del **pulsante Barrato.**

Il valore della proprietà deriva [**dall'enumerazione \_ FONTPROPERTIES dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) utente.

Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.

Lo screenshot seguente mostra il pulsante **Barrato** dell'oggetto [**FontControl della barra multifunzione.**](windowsribbon-element-fontcontrol.md)

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-strikethrough.png)

La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.



|   Proprietà                       |    Risultato dell'interfaccia utente                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Il pulsante Barrato** è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTPROPERTIES_NOTSET`       | **Il pulsante Barrato** non è selezionato.                                    |
| `UI_FONTPROPERTIES_SET`          | **Il pulsante Barrato** è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**PROPRIETÀ CARATTERE \_ DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controllo Font](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 