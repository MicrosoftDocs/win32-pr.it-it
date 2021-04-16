---
title: Test con AccChecker
description: Descrive il flusso di lavoro di test tipico che incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- test con AccChecker
- AccChecker, test del flusso di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515523"
---
# <a name="testing-with-accchecker"></a>Test con AccChecker

Nello scenario seguente vengono descritti i passaggi che si seguono in genere durante il test con AccChecker.

> [!Note]  
> Quando le routine di verifica AccChecker sono in esecuzione, l'interazione dell'utente con il computer host può interferire con alcune routine. Si consiglia di non eseguire ulteriori interazioni da parte dell'utente fino a quando AccChecker non notifica all'utente che tutte le attività sono state completate.

 

1.  Eseguire le verifiche AccChecker su un'applicazione o un controllo di destinazione specifico. Per ulteriori informazioni, vedere la [scheda verifiche](the-accchecker-graphical-user-interface.md).
    > [!Note]  
    > AccChecker non Esplora tutte le permutazioni dell'interfaccia utente in un'applicazione. Gli elementi nascosti all'interno di controlli quali Windows, i riquadri, le schede e i menu devono essere esposti manualmente.

     

2.  Esaminare il log degli errori di AccChecker e valutare o valutare i risultati. Risolvere i problemi semplici e registrare i bug gravi nel modo appropriato.
3.  Genera un file di eliminazione per bug ed errori che possono essere ignorati fino al test di regressione.
4.  Eseguire di nuovo le verifiche AccChecker con il file di eliminazione e le correzioni di bug iniziali. Questo fornisce uno snapshot dei problemi nell'implementazione corrente di Microsoft Active Accessibility e stabilisce una baseline per i test di regressione.
5.  Integrare le API AccChecker e il file di eliminazione in un Framework di test automatico per i test di regressione sui bug registrati dalle verifiche AccChecker iniziali.
    > [!Note]  
    > Con la correzione dei bug, il file di eliminazione deve essere modificato in modo obbligatorio.

     

6.  Verificare che non siano state introdotte regressioni o nuovi bug di accessibilità nell'applicazione o nel controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 




