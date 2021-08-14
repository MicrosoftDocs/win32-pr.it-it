---
title: UI_PKEY_FontProperties_Italic
description: Identifica la proprietà \_ FontProperties Italic dell'interfaccia \_ utente \_ PKEY.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bb72e1ba43b29f5e3815fe42d0ace454ff0219a188a128b422e4a621af210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438536"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ PKEY \_ FontProperties \_ Italic

Identifica la proprietà \_ FontProperties Italic dell'interfaccia \_ utente \_ PKEY.

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Commenti

Ui \_ PKEY \_ FontProperties \_ Italic viene usato da un'applicazione per eseguire query sullo stato del **pulsante Corsivo.**

Il valore della proprietà deriva [**dall'enumerazione \_ FONTPROPERTIES dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) utente.

Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.

La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.



|    Proprietà                      |       Risultato dell'interfaccia utente                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Il pulsante** Corsivo è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTPROPERTIES_NOTSET`       | **Il pulsante** Corsivo non è selezionato.                                    |
| `UI_FONTPROPERTIES_SET`          | **Il pulsante** Corsivo è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**PROPRIETÀ FONT \_ DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 