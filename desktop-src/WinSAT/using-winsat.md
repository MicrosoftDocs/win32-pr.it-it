---
title: Uso di WinSAT
description: È possibile utilizzare l'API Windows System Assessment Tool (WinSAT) per avviare valutazioni formali ed ad hoc della configurazione hardware del computer, recuperare il Punteggio di base per il computer e i punteggi per ogni sottocomponente della valutazione e recuperare i dettagli della valutazione, ad esempio i dettagli del processore valutato.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a23ab35d989a736fa61833e678c0a4c79954e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395787"
---
# <a name="using-winsat"></a>Uso di WinSAT

\[WinSAT può essere modificato o non disponibile per le versioni dopo Windows 8.1.\]

È possibile utilizzare l'API Windows System Assessment Tool (WinSAT) per [avviare valutazioni formali ed ad hoc](#initiating-an-assessment) della configurazione hardware del computer, [recuperare il Punteggio di base per il computer](#retrieving-the-scores-of-the-assessment) e i punteggi per ogni sottocomponente della valutazione e recuperare i [Dettagli della valutazione](#retrieving-details-of-the-assessment), ad esempio i dettagli del processore valutato.

## <a name="initiating-an-assessment"></a>Avvio di una valutazione

Dopo Windows 8.1 è possibile avviare valutazioni formali ed ad hoc del computer. Una valutazione formale valuta i seguenti sottocomponenti del computer:

-   CPU
-   Memoria
-   Disco principale
-   Scheda video

Per avviare una valutazione formale, chiamare il metodo [**IInitiateWinSATAssessment:: InitiateFormalAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) . I risultati delle valutazioni formali vengono salvati nell'archivio di valutazione e possono essere recuperati in un secondo momento.

In genere, le valutazioni ad hoc vengono utilizzate per valutare solo un sottocomponente del computer, ad esempio la CPU o la memoria. Tuttavia, è possibile usare l'opzione **formale** per valutare tutti i sottocomponenti. Per avviare una valutazione ad hoc, chiamare il metodo [**IInitiateWinSATAssessment:: InitiateAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) . Si noti che i risultati delle valutazioni ad hoc non vengono salvati nell'archivio di valutazione.

Per recuperare la notifica quando viene eseguito lo stato di avanzamento o quando la valutazione viene completata, implementare l'interfaccia [**IWinSATInitiateEvents**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents) .

Non è possibile eseguire valutazioni formali in remoto o in un computer in cui è in esecuzione batterie. Non è inoltre possibile eseguire in modalità remota una valutazione ad hoc sul sottocomponente graphics.

## <a name="retrieving-the-scores-of-the-assessment"></a>Recupero dei punteggi della valutazione

È possibile recuperare il Punteggio di base del computer e il punteggio per ogni sottocomponente della valutazione. È possibile usare l'API per recuperare i punteggi solo per le valutazioni formali. Per recuperare i punteggi per le valutazioni ad hoc, è necessario includere l'argomento **-XML** nella riga di comando per salvare i risultati della valutazione in un file XML e quindi analizzare il file per il punteggio del sottocomponente.

Il Punteggio di base è una misurazione generale della configurazione hardware del computer. Un punteggio di base più elevato in genere significa che il computer è più efficiente e più veloce rispetto a un computer con un punteggio di base inferiore, soprattutto quando si eseguono attività più avanzate e a elevato utilizzo di risorse.

Ogni componente hardware riceve un singolo Punteggio di sottolineatura. Il Punteggio di base del computer è determinato dal punteggio di sottolineatura più basso. Se, ad esempio, il Punteggio di sottolineatura più basso di un singolo componente hardware è 2,6, il Punteggio di base è 2,6. Il Punteggio di base non è una media dei punteggi di sottolineatura combinati.

Un utente può utilizzare il Punteggio di base per acquistare in modo sicuro programmi e altri software corrispondenti al Punteggio di base del computer. Se, ad esempio, il computer dispone di un punteggio di base di 3,3, l'utente potrà acquistare con fiducia il software progettato per questa versione di Windows che richiede un computer con un punteggio di base di 3 o inferiore.

Per recuperare il Punteggio di base, chiamare prima il metodo [**IQueryRecentWinSATAssessment:: Get \_ info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) per ottenere l'interfaccia [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) . Chiamare quindi il metodo [**IProvideWinSATResultsInfo:: Get \_ SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) per ottenere il Punteggio di base.

Un utente può utilizzare i punteggi dei sottocomponenti per determinare se un sottocomponente del computer può supportare un tipo specifico di applicazione. Ad esempio, un utente che dedica più tempo per la lettura o la scrittura di documenti potrebbe richiedere un punteggio più alto per il disco rispetto a un utente che esegue applicazioni scientifiche e un utente che esegue applicazioni scientifiche potrebbe desiderare un punteggio di sottocomponente CPU superiore e potrebbe non essere interessato da un punteggio del disco inferiore.

Per recuperare il punteggio per ogni sottocomponente, chiamare prima il metodo [**IQueryRecentWinSATAssessment:: Get \_ info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) per ottenere l'interfaccia [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) . Chiamare quindi il metodo [**IProvideWinSATResultsInfo:: GetAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) per ottenere l'interfaccia [**IProvideWinSATAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) . Per ogni sottocomponente di cui si vuole recuperare il punteggio, chiamare il metodo [**IProvideWinSATAssessmentInfo:: Get \_ Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="retrieving-details-of-the-assessment"></a>Recupero dei dettagli della valutazione

L'API WinSAT fornisce il Punteggio di base e i punteggi complessivi per ogni sottocomponente. Per ottenere i dettagli della valutazione (ad esempio, le metriche utilizzate per calcolare il punteggio e i dettagli del processore valutato), è necessario recuperare i dati dal documento di valutazione XML. Per recuperare i dettagli della valutazione formale più recente, chiamare il metodo [**IQueryRecentWinSATAssessment:: Get \_ XML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) . Per recuperare i dettagli da ogni valutazione nell'archivio dati WinSAT, chiamare il metodo [**IQueryAllWinSATAssessments:: Get \_ AllXML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml) .

Per informazioni sul XML Schema e sui dettagli che è possibile recuperare, vedere [schema WinSAT](winsat-schema.md).

 

 




