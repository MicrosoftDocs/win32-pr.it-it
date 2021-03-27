---
description: I valori del registro di sistema devono essere impostati per i verbi per gestire le situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento. Un verbo richiede valori di registro distinti per ognuna di queste tre situazioni supportate dal verbo.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Come utilizzare il modello di selezione dei verbi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979575"
---
# <a name="how-to-employ-the-verb-selection-model"></a>Come utilizzare il modello di selezione dei verbi

I valori del registro di sistema devono essere impostati per i verbi per gestire le situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento. Un verbo richiede valori di registro distinti per ognuna di queste tre situazioni supportate dal verbo.

## <a name="instructions"></a>Istruzioni


Specificare il valore MultiSelectModel per tutti i verbi. Se il valore MultiSelectModel non è specificato, viene dedotto dal tipo di implementazione del verbo scelto. Per i metodi basati su COM, ad esempio DropTarget e ExecuteCommand, viene utilizzato il **lettore** e per gli altri metodi viene utilizzato il **documento** .

I valori possibili per il modello di selezione dei verbi sono i seguenti:

1.  Specificare **Single** per i verbi che supportano una sola selezione.
2.  Specificare il **lettore** per i verbi che supportano un numero qualsiasi di elementi.
3.  Specificare il **documento** per i verbi che creano una finestra di primo livello per ogni elemento. Questa operazione limita il numero di elementi attivati e consente di evitare l'esaurimento delle risorse di sistema se l'utente apre troppe finestre.

## <a name="remarks"></a>Commenti

Quando il numero di elementi selezionati non corrisponde al modello di selezione dei verbi o è maggiore dei limiti predefiniti indicati nella tabella seguente, il verbo non viene visualizzato.



| Tipo di implementazione del verbo | Documento | Lettore    |
|-----------------------------|----------|-----------|
| Legacy                      | 15 elementi | 100 elementi |
| COM                         | 15 elementi | Nessun limite  |



 

Di seguito sono riportate voci del registro di sistema di esempio che utilizzano il valore MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



