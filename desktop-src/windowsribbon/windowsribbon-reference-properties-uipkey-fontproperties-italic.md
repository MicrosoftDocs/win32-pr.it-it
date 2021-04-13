---
title: UI_PKEY_FontProperties_Italic
description: Identifica la \_ Proprietà pkey \_ FontProperties corsivo dell'interfaccia utente \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399166"
---
# <a name="ui_pkey_fontproperties_italic"></a>Interfaccia utente \_ pkey \_ FontProperties \_ corsivo

Identifica la \_ Proprietà pkey \_ FontProperties corsivo dell'interfaccia utente \_ .

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

L'interfaccia utente \_ pkey \_ FontProperties \_ corsivo viene utilizzata da un'applicazione per eseguire una query sullo stato del pulsante **corsivo** .

Il valore della proprietà è dall' [**enumerazione \_ FONTPROPERTIES dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.

Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Il pulsante **corsivo** è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTPROPERTIES_NOTSET`       | Il pulsante **corsivo** non è selezionato.                                    |
| `UI_FONTPROPERTIES_SET`          | Il pulsante **corsivo** è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 