---
description: Un contesto di dispositivo padre consente a un'applicazione di ridurre al minimo il tempo necessario per configurare l'area di visualizzazione per una finestra.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Contesti dispositivo di visualizzazione padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978442"
---
# <a name="parent-display-device-contexts"></a>Contesti dispositivo di visualizzazione padre

Un *contesto di dispositivo padre* consente a un'applicazione di ridurre al minimo il tempo necessario per configurare l'area di visualizzazione per una finestra. Un'applicazione usa in genere i contesti di dispositivo padre per velocizzare il disegno per le finestre di controllo senza richiedere un contesto di dispositivo privato o di classe. Ad esempio, il sistema usa i contesti di dispositivo padre per i pulsanti di comando e di modifica. I contesti di dispositivo padre sono destinati all'uso solo con le finestre figlio, mai con finestre popup o di primo livello.

Un'applicazione può specificare lo \_ stile cs PARENTDC per impostare l'area di visualizzazione della finestra figlio sulla finestra padre in modo che l'elemento figlio possa disegnarlo nell'elemento padre. La specifica di CS \_ PARENTDC migliora le prestazioni di un'applicazione perché non è necessario che il sistema continui a ricalcolare l'area visibile per ogni finestra figlio.

I valori di attributo impostati dalla finestra padre non vengono conservati per la finestra figlio; la finestra padre, ad esempio, non può impostare il pennello per le finestre figlio. L'unica proprietà conservata è l'area di ridimensionamento. La finestra deve ritagliare il proprio output ai limiti della finestra. Poiché l'area di ridimensionamento per il contesto di dispositivo padre è identica alla finestra padre, è possibile che la finestra figlio si avvicini all'intera finestra padre, ma il contesto di dispositivo padre non deve essere usato in questo modo.

Il sistema ignora lo stile CS \_ PARENTDC se la finestra padre utilizza un contesto di dispositivo privato o di classe, se la finestra padre Ritaglia le finestre figlio o se la finestra figlio Ritaglia le finestre figlio o le finestre di pari livello.

 

 



