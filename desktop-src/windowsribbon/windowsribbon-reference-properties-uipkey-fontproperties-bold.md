---
title: UI_PKEY_FontProperties_Bold
description: Identifica la \_ \_ Proprietà FontProperties Bold dell'interfaccia utente pkey \_ .
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300234"
---
# <a name="ui_pkey_fontproperties_bold"></a>Interfaccia utente \_ pkey \_ FontProperties \_ Bold

Identifica la \_ \_ Proprietà FontProperties Bold dell'interfaccia utente pkey \_ .

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

L'interfaccia utente \_ pkey \_ FontProperties \_ Bold viene utilizzata da un'applicazione per eseguire una query sullo stato del pulsante in **grassetto** .

Il valore della proprietà è dall' [**enumerazione \_ FONTPROPERTIES dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.

Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Il pulsante **grassetto** è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTPROPERTIES_NOTSET`       | Il pulsante **grassetto** non è selezionato.                                    |
| `UI_FONTPROPERTIES_SET`          | Il pulsante **grassetto** è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 