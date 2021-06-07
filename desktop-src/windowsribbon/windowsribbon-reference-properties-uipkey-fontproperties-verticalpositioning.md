---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ VerticalPositioning.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444302"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>UI \_ PKEY \_ FontProperties \_ VerticalPositioning

Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ VerticalPositioning.

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

Ui PKEY FontProperties VerticalPositioning viene usato da un'applicazione per eseguire query sul valore dei \_ \_ controlli \_ **Apice** **e Pedice.**

Il valore della proprietà deriva [**dall'enumerazione \_ FONTVERTICALPOSITION dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) utente.

Il valore predefinito è `UI_FONTVERTICALPOSITION_NOTSET`.

Lo screenshot seguente mostra i **pulsanti Apice** e **Pedice** della barra [**multifunzione FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-subsuper.png)

La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.



|     Proprietà                           |          Risultato dell'interfaccia utente                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | **I pulsanti Apice** **e Pedice** sono disabilitati e possono essere impostati solo dall'applicazione. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | **I pulsanti Apice** **e Pedice** non sono selezionati.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | **Il pulsante Apice** è selezionato.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | **Il pulsante Pedice** è selezionato.                                                              |



 

> [!Note]  
> Non **è possibile selezionare** entrambi **i** pulsanti Apice e Pedice.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTVERTICALPOSITION DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 