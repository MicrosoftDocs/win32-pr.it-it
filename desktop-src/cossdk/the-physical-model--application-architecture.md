---
description: Una volta completati i modelli concettuali e logici, è possibile prendere decisioni sull'implementazione fisica dell'applicazione.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: "Modello fisico: architettura dell'applicazione"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127542"
---
# <a name="the-physical-model-application-architecture"></a>Modello fisico: architettura dell'applicazione

Una volta completati i modelli concettuali e logici, è possibile prendere decisioni sull'implementazione fisica dell'applicazione. Per creare il modello fisico, è necessario conoscere la posizione dei vari servizi dell'applicazione e il modo in cui devono essere implementati. Determinare la posizione in cui risiedono i servizi deve precedere il modo in cui verranno implementati i servizi.

Una regola di base per determinare la posizione in cui risiedono i diversi servizi è la seguente: inserire il componente in cui viene usato. Se, ad esempio, un componente Visualizza informazioni per il client di base, deve essere installato nel computer dell'utente. Se un componente convalida le informazioni dal client di base, deve risiedere anche nel computer del client di base. Se un componente Aggiorna le informazioni in un database, dovrebbe risiedere nel server di database.

Esistono, naturalmente, considerazioni aggiuntive che fanno eccezioni a questa regola. I problemi di prestazioni e sicurezza possono anche determinare la posizione di un componente. Considerare quanto segue:

-   Un componente verrà modificato di frequente, rendendo difficile la distribuzione degli aggiornamenti?
-   Il componente verrà usato da altre applicazioni, ad esempio un componente comune di verifica della sicurezza?
-   Il componente esegue calcoli lunghi o esegue funzioni, ad esempio la stampa, di cui è possibile eseguire il offload in un server?
-   È possibile migliorare la sicurezza di un componente inserendolo in un server?

Individuare correttamente i componenti di un'applicazione può anche isolare il team di sviluppo dalla ricodifica costosa se il sistema o la posizione dei dati cambia. Se ad esempio si inseriscono le regole di accesso ai dati in un livello dati piuttosto che nelle stored procedure, l'applicazione è più facilmente isolata dalla dipendenza da un DBMS specifico. Non solo le modifiche sono conformi e il test di compartimentato, ma le origini dati possono essere modificate e i dati possono essere distribuiti senza modificare radicalmente l'applicazione.

Infine, l'individuazione dei componenti dovrebbe sfruttare le efficienze del sistema. Il posizionamento di oggetti business in posizioni centralizzate sulla rete è una soluzione conveniente. Gli oggetti possono essere condivisi tra le applicazioni e il testing unità può essere eseguito prima della distribuzione di qualsiasi componente. È anche possibile ridurre i costi di manutenzione perché le modifiche alle regole si verificano solo in un singolo punto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello concettuale: requisiti delle applicazioni](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Modello logico: definizione dell'applicazione e pianificazione](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



