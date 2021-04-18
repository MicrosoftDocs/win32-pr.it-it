---
description: È possibile utilizzare le funzioni del programma di installazione per eseguire azioni specifiche o sequenze di azioni.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Azioni in esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309452"
---
# <a name="running-actions"></a>Azioni in esecuzione

È possibile utilizzare le funzioni del programma di installazione per eseguire azioni specifiche o sequenze di azioni. Queste azioni possono essere azioni [standard](standard-actions.md) o [personalizzate](custom-actions.md) . Nella procedura seguente viene descritto come eseguire le azioni:

**Per eseguire una sequenza di azione**

1.  Eseguire una sequenza di azioni definite in una tabella chiamando la funzione [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .

    Il programma di installazione esegue una query sulla tabella indicata ed esegue ogni azione se la relativa espressione condizionale restituisce TRUE.

2.  Controllare le espressioni condizionali chiamando la funzione [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .
3.  Eseguire l'azione chiamando la funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) . L'azione può essere un'azione standard, un'azione personalizzata o una finestra di dialogo dell'interfaccia utente.
4.  Se si è verificato un errore durante l'esecuzione di questa azione, chiamare la funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . L'errore verrà elaborato dal programma di installazione.

 

 



