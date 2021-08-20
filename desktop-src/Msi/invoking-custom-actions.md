---
description: Le azioni personalizzate vengono richiamate nello stesso modo delle azioni standard, tramite una chiamata esplicita o durante l'esecuzione di una tabella di sequenza.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Chiamata di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba80afbd573ffb77fddb7723c433b7476055da2dc11deda39bb3cae4148b7f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629754"
---
# <a name="invoking-custom-actions"></a>Chiamata di azioni personalizzate

Le azioni personalizzate vengono richiamate nello stesso modo delle azioni standard, tramite una chiamata esplicita o durante l'esecuzione di una tabella di sequenza. Esistono due metodi per chiamare le azioni:

-   L'azione specificata viene chiamata direttamente con la [**funzione MsiDoAction.**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)
-   Un'azione di primo livello chiama la tabella di sequenza contenente l'azione personalizzata. Per altre informazioni sulla pianificazione di un'azione personalizzata in una tabella di sequenza, vedere [Sequenziazione di azioni personalizzate](sequencing-custom-actions.md).

Quando il programma di installazione ottiene un nome di azione dalla [**funzione MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o da una tabella di sequenza, cerca innanzitutto un'azione standard con tale nome. Se non riesce a trovare l'azione standard, il programma di installazione esegue una query [sulla tabella CustomAction](customaction-table.md) per verificare se l'azione specificata è un'azione personalizzata. Se l'azione specificata non è un'azione personalizzata, il programma di installazione esegue una query nella [tabella Finestra](dialog-table.md) di dialogo per trovare una finestra di dialogo.

 

 



