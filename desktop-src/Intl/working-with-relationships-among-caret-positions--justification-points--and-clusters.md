---
description: La tabella seguente illustra i diversi metodi che possono essere usati dall'applicazione per gestire il punto di inserimento, la giustificazione e i cluster.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Utilizzo delle relazioni tra le posizioni del punto di inserimento, i punti di giustificazione e i cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307271"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>Utilizzo delle relazioni tra le posizioni del punto di inserimento, i punti di giustificazione e i cluster

La tabella seguente illustra i diversi metodi che possono essere usati dall'applicazione per gestire il punto di inserimento, la giustificazione e i cluster.



| Attività                             | Supporto di Uniscribe                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spostamento del punto di inserimento per cluster di caratteri  | Il parametro *pwLogClust* del membro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** della struttura di [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> Membro **fCharStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Interruzioni di riga tra caratteri | Il parametro *pwLogClust* del membro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** della struttura di [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> Membro **fCharStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Spostamento del cursore per parola               | Membro **fWordStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Interruzioni di riga tra le parole      | Membro **fWordStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Giustificazione                    | Membro **uJustification** della struttura [**\_ VISATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_visattr)                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




