---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la \_ \_ Proprietà VerticalPositioning FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047212"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>Interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning

Identifica la \_ \_ Proprietà VerticalPositioning FontProperties di pkey dell'interfaccia utente \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning viene utilizzata da un'applicazione per eseguire una query sul valore dei controlli **apice** e **pedice** .

Il valore della proprietà è dall' [**enumerazione \_ FONTVERTICALPOSITION dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .

Il valore predefinito è `UI_FONTVERTICALPOSITION_NOTSET`.

La schermata seguente mostra i pulsanti **apice e** **Indice** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-subsuper.png)

Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | I pulsanti apice e **pedice** sono disabilitati **e possono** essere impostati solo dall'applicazione. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | I pulsanti **apice e** **pedice** non sono selezionati.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | Il pulsante **apice** è selezionato.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | Il pulsante **Indice** è selezionato.                                                              |



 

> [!Note]  
> Non è possibile selezionare **entrambi i pulsanti apice e** **pedice** .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 