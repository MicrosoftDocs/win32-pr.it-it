---
title: Uso di WinSAT
description: È possibile usare l'API WinSAT (System Assessment Tool) di Windows per avviare valutazioni formali e ad hoc della configurazione hardware del computer, recuperare il punteggio di base per il computer e i punteggi per ogni sottocomponente della valutazione e recuperare i dettagli della valutazione, ad esempio i dettagli del processore valutato.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23cf26d31ccbd3eb6e51fb1717c055fb6538c57612d374b0a3b7a2a5b2382681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733781"
---
# <a name="using-winsat"></a>Uso di WinSAT

\[WinSAT può essere modificato o non disponibile per le versioni dopo Windows 8.1.\]

È possibile usare l'API WinSAT (System Assessment Tool) di Windows per avviare valutazioni formali e [ad hoc](#initiating-an-assessment) della configurazione hardware del computer, recuperare il punteggio di base per il [computer](#retrieving-the-scores-of-the-assessment) e i punteggi per ogni sottocomponente della valutazione e recuperare i dettagli della [valutazione,](#retrieving-details-of-the-assessment)ad esempio i dettagli del processore valutato.

## <a name="initiating-an-assessment"></a>Avvio di una valutazione

Dopo Windows 8.1 è possibile avviare valutazioni formali e ad hoc del computer. Una valutazione formale valuta i sottocomponenti seguenti del computer:

-   CPU
-   Memoria
-   Disco principale
-   Scheda video

Per avviare una valutazione formale, chiamare il metodo [**IInitiateWinSATAssessment::InitiateFormalAssessment.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) I risultati delle valutazioni formali vengono salvati nell'archivio di valutazione e possono essere recuperati in un secondo momento.

In genere, si usano valutazioni ad hoc per valutare un solo sottocomponente del computer, ad esempio la CPU o la memoria. Tuttavia, è possibile usare **l'opzione formale** per valutare tutti i sottocomponenti. Per avviare una valutazione ad hoc, chiamare il metodo [**IInitiateWinSATAssessment::InitiateAssessment.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) Si noti che i risultati delle valutazioni ad hoc non vengono salvati nell'archivio valutazioni.

Per recuperare la notifica quando viene effettuato lo stato o al termine della valutazione, implementare [**l'interfaccia IWinSATInitiateEvents.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents)

Non è possibile eseguire valutazioni formali in modalità remota o in un computer in esecuzione su batterie. Non è inoltre possibile eseguire in remoto una valutazione ad hoc nel sottocomponente grafico.

## <a name="retrieving-the-scores-of-the-assessment"></a>Recupero dei punteggi della valutazione

È possibile recuperare il punteggio di base del computer e il punteggio per ogni sottocomponente della valutazione. È possibile usare l'API per recuperare i punteggi solo per le valutazioni formali. Per recuperare i punteggi per le valutazioni ad hoc, è necessario includere l'argomento **-xml** nella riga di comando per salvare i risultati della valutazione in un file XML e quindi analizzare il file per il punteggio del sottocomponente.

Il punteggio di base è una misura generale della configurazione hardware del computer. Un punteggio di base più alto in genere significa che il computer avrà prestazioni migliori e più veloci rispetto a un computer con un punteggio di base inferiore, soprattutto quando si eseguono attività più avanzate e a elevato utilizzo di risorse.

Ogni componente hardware riceve un singolo sottocore. Il punteggio di base del computer è determinato dal sottocore più basso. Ad esempio, se il sottocore più basso di un singolo componente hardware è 2,6, il punteggio di base è 2,6. Il punteggio di base non è una media dei sottocore combinati.

Un utente può usare il punteggio di base per acquistare in modo sicuro programmi e altri software corrispondenti al punteggio di base del computer. Ad esempio, se il computer ha un punteggio di base di 3,3, l'utente può acquistare con sicurezza qualsiasi software progettato per questa versione di Windows che richiede un computer con un punteggio di base pari a 3 o inferiore.

Per recuperare il punteggio di base, chiamare prima il metodo [**IQueryRecentWinSATAssessment::get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) per ottenere l'interfaccia [**IProvideWinSATResultsInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) Chiamare quindi il [**metodo IProvideWinSATResultsInfo::get \_ SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) per ottenere il punteggio di base.

Un utente può usare i punteggi dei sottocomponenti per determinare se un sottocomponente del computer può supportare un tipo specifico di applicazione. Ad esempio, un utente che dedica più tempo alla lettura o alla scrittura di documenti può richiedere un punteggio più alto per il disco rispetto a un utente che esegue applicazioni scientifiche e un utente che esegue applicazioni scientifiche probabilmente richiederebbe un punteggio di sottocomponente della CPU superiore e potrebbe non essere interessato da un punteggio del disco inferiore.

Per recuperare il punteggio per ogni sottocomponente, chiamare prima il metodo [**IQueryRecentWinSATAssessment::get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) per ottenere l'interfaccia [**IProvideWinSATResultsInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) Chiamare quindi il [**metodo IProvideWinSATResultsInfo::GetAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) per ottenere l'interfaccia [**IProvideWinSATAssessmentInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) Per ogni sottocomponente di cui si vuole recuperare il punteggio, chiamare il metodo [**IProvideWinSATAssessmentInfo::get \_ Score.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score)

## <a name="retrieving-details-of-the-assessment"></a>Recupero dei dettagli della valutazione

L'API WinSAT fornisce il punteggio di base complessivo e i punteggi per ogni sottocomponente. Per ottenere i dettagli della valutazione,ad esempio le metriche usate per calcolare il punteggio e i dettagli del processore valutato, è necessario recuperare i dati dal documento di valutazione XML. Per recuperare i dettagli della valutazione formale più recente, chiamare il metodo [**IQueryRecentWinSATAssessment::get \_ XML.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) Per recuperare i dettagli da ogni valutazione nell'archivio dati WinSAT, chiamare il metodo [**IQueryAllWinSATAssessments::get \_ AllXML.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml)

Per informazioni sullo schema XML e sui dettagli che è possibile recuperare, vedere [Schema WinSAT](winsat-schema.md).

 

 




