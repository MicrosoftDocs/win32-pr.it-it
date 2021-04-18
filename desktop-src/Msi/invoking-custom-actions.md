---
description: Le azioni personalizzate vengono richiamate allo stesso modo delle azioni standard, tramite chiamata esplicita o durante l'esecuzione di una tabella di sequenza.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Richiamo di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318280"
---
# <a name="invoking-custom-actions"></a>Richiamo di azioni personalizzate

Le azioni personalizzate vengono richiamate allo stesso modo delle azioni standard, tramite chiamata esplicita o durante l'esecuzione di una tabella di sequenza. Esistono due metodi per chiamare le azioni:

-   L'azione specificata viene chiamata direttamente con la funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .
-   Un'azione di primo livello chiama la tabella di sequenza contenente l'azione personalizzata. Per ulteriori informazioni sulla pianificazione di un'azione personalizzata in una tabella di sequenza, vedere [sequenziazione di azioni personalizzate](sequencing-custom-actions.md).

Quando il programma di installazione ottiene un nome di azione dalla funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o da una tabella Sequence, cerca innanzitutto un'azione standard con tale nome. Se non riesce a trovare l'azione standard, il programma di installazione esegue una query sulla [tabella CustomAction](customaction-table.md) per verificare se l'azione specificata è un'azione personalizzata. Se l'azione specificata non è un'azione personalizzata, il programma di installazione esegue una query nella [tabella](dialog-table.md) della finestra di dialogo per una finestra di dialogo.

 

 



