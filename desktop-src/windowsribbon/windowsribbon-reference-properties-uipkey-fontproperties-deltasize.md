---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la proprietà \_ \_ DeltaSize FontProperties PKEY \_ dell'interfaccia utente.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35d2660d2221b4edad567b0fd05eb8283fce4b3cc7d1cb8e35c735838f385d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438754"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>UI \_ PKEY \_ FontProperties \_ DeltaSize

Identifica la proprietà \_ \_ DeltaSize FontProperties PKEY \_ dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Commenti

Ui PKEY FontProperties DeltaSize viene usato da un'applicazione nei casi in cui non è possibile per l'applicazione specificare un valore per Dimensioni carattere, ad esempio quando viene selezionata un'esecuzione di testo di \_ \_ dimensioni \_ eterogenee.  Il **controllo Dimensioni carattere è** impostato su vuoto e l'interfaccia utente \_ PKEY FontProperties DeltaSize viene usata per acquisire l'interazione dell'utente con i pulsanti Aumenta carattere e Riduci \_ \_ **carattere.** 

UI \_ PKEY \_ FontProperties \_ DeltaSize è incluso in [UI \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).

Lo screenshot seguente mostra i pulsanti **Aumenta carattere e** Riduci carattere del controllo FontControl della barra [**multifunzione.**](windowsribbon-element-fontcontrol.md) 

![Screenshot dei pulsanti per l'estensione e la riduzione del tipo di carattere in fontcontrol.](images/markup/fontcontrol-incdec.png)

Nella tabella seguente vengono descritti i valori delle proprietà.



|     Valore                 |  Descrizione                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | **Pulsante Aumenta dimensioni** carattere selezionato.   |
| `UI_FONTDELTASIZE_SHRINK` | **È stato fatto clic sul** pulsante Riduci carattere. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTDELTASIZE DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Controllo Font](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 