---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la \_ \_ Proprietà DeltaSize FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046760"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>Interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize

Identifica la \_ \_ Proprietà DeltaSize FontProperties di pkey dell'interfaccia utente \_ .

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

L'interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize viene utilizzata da un'applicazione nei casi in cui non è possibile che l'applicazione specifichi un valore per le **dimensioni del carattere**, ad esempio quando viene selezionata un'esecuzione di testo di dimensioni eterogenee. Il controllo delle **dimensioni del carattere** è impostato su Blank e l'interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize viene utilizzata per acquisire l'interazione dell'utente con i pulsanti di **espansione del tipo di carattere** e **compattazione dei caratteri** .

UI \_ pkey \_ FontProperties \_ DeltaSize è incluso nell' [interfaccia \_ utente \_ pkey \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)ChangedProperties.

La schermata seguente mostra i pulsanti **dimensioni** del carattere e **compattazione del carattere** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).

![cattura di schermata dei pulsanti dimensioni e compattazione carattere in fontcontrol.](images/markup/fontcontrol-incdec.png)

Nella tabella seguente vengono descritti i valori delle proprietà.



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | Pulsante **aumenta carattere** selezionato.   |
| `UI_FONTDELTASIZE_SHRINK` | Pulsante **compatta carattere** selezionato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ FONTDELTASIZE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 