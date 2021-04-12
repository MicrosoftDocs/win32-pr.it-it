---
title: UI_PKEY_FontProperties_Underline
description: Identifica la \_ proprietà di \_ sottolineatura pkey FontProperties dell'interfaccia utente \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473587"
---
# <a name="ui_pkey_fontproperties_underline"></a>\_ \_ Sottolineato FontProperties pkey dell'interfaccia utente \_

Identifica la \_ proprietà di \_ sottolineatura pkey FontProperties dell'interfaccia utente \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ FontProperties \_ Underline viene utilizzata da un'applicazione per eseguire una query sullo stato del pulsante **sottolineato** .

Il valore della proprietà è dall' [**enumerazione \_ FONTUNDERLINE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .

Il valore predefinito è `UI_FONTUNDERLINE_NOTSET`.

Lo screenshot seguente mostra il pulsante **sottolineato** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-underline.png)

Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | Il pulsante **sottolineato** è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTUNDERLINE_NOTSET`       | Il pulsante **sottolineato** non è selezionato.                                    |
| `UI_FONTUNDERLINE_SET`          | Il pulsante **sottolineatura** è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 