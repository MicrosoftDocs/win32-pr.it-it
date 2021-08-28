---
title: Test con AccChecker
description: Descrive il flusso di lavoro di test tipico che incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- test con AccChecker
- AccChecker, flusso di lavoro di test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addf725431a17a9b63376dfc3fc7ef8563a1737c9867b950f09eb123bf7daf18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795511"
---
# <a name="testing-with-accchecker"></a>Test con AccChecker

Lo scenario seguente descrive i passaggi che in genere si seguono durante i test con AccChecker.

> [!Note]  
> Quando le routine di verifica AccChecker sono in esecuzione, l'interazione dell'utente con il computer host può interferire con alcune routine. È consigliabile non eseguire altre interazioni con l'utente fino a quando AccChecker non notifica all'utente che tutte le attività sono state completate.

 

1.  Eseguire le verifiche AccChecker in un'applicazione o un controllo di destinazione specifico. Per altre informazioni, vedere [Scheda Verifiche.](the-accchecker-graphical-user-interface.md)
    > [!Note]  
    > AccChecker non esplora tutte le permutazioni dell'interfaccia utente in un'applicazione. Gli elementi nascosti all'interno di controlli quali finestre, riquadri, schede e menu devono essere esposti manualmente.

     

2.  Esaminare il log degli errori di AccChecker e valutare o valutare i risultati. Risolvere problemi semplici e registrare bug gravi in base alle esigenze.
3.  Generare un file di eliminazione per i bug e gli errori che possono essere ignorati fino al test di regressione.
4.  Eseguire nuovamente le verifiche AccChecker con il file di eliminazione e le correzioni di bug iniziali. In questo modo viene fornito uno snapshot dei problemi nell'implementazione corrente di Microsoft Active Accessibility e viene stabilita una baseline per i test di regressione.
5.  Integrare le API AccChecker e il file di eliminazione in un framework di test automatizzato per i test di regressione sui bug registrati dalle verifiche iniziali di AccChecker.
    > [!Note]  
    > Quando vengono corretti i bug, il file di eliminazione deve essere modificato in base alle esigenze.

     

6.  Verificare che non siano state introdotte regressioni o nuovi bug di accessibilità nell'applicazione o nel controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 




