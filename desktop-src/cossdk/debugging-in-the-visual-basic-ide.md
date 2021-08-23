---
description: L'uso di Microsoft Visual Basic ide (Integrated Development Environment) per il debug consente Visual Basic agli sviluppatori di accedere a strumenti familiari e facilità d'uso.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Debug nell'IDE Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 284e97a766256cd281b3515bdd142d15ff5208e2c1a1555438c428daeca8f3a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548010"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Debug nell'IDE Visual Basic

L'uso di Microsoft Visual Basic ide (Integrated Development Environment) per il debug consente Visual Basic agli sviluppatori di accedere a strumenti familiari e facilità d'uso. Anche se sarà necessario eseguire il debug completo di molti componenti usando l'ambiente Microsoft Visual C++, una strategia potrebbe consistere nel eseguire prima il debug del maggior numero possibile di funzionalità con Visual Basic. Ad esempio, è possibile usare l'IDE di Visual Basic per il debug all'interno di COM+ quando non si esegue ancora il debug di multithreading, rilevamento dei componenti, chiamate remote o isolamento del processo.

In generale, quando si usa l'ambiente Visual Basic per il debug, è innanzitutto necessario compilare il progetto e aggiungere la DLL a un'applicazione COM+. Si imposta quindi la compatibilità binaria per il progetto, si fa riferimento alla DLL effettuata e si avvia il progetto per avviare il debug.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Linee guida generali per il debug nell Visual Basic ambiente

-   Durante il debug con Visual Basic, COM+ considera i componenti Visual Basic come se appartengano a un'applicazione di libreria, anche se i componenti sono registrati come appartenenti a un'applicazione server. Poiché viene eseguito come applicazione di libreria, le icone dei componenti nello strumento di amministrazione Servizi componenti non ruotano durante il debug dei componenti.
-   Se si modificano gli attributi della transazione in un componente durante il debug o si apporta una modifica al codice sorgente che richiede Visual Basic per generare un nuovo CLSID o ProgID, assicurarsi di eliminare e reinstallare l'applicazione COM+ contenente il componente. Se è stata impostata la compatibilità binaria per il componente, verrà visualizzato un avviso che indica che sono state apportate modifiche.

## <a name="notes-on-debugging-within-a-com-application"></a>Note sul debug all'interno di un'applicazione COM+

-   Se si apportano modifiche nell'IDE di Visual Basic nelle interfacce, nei nomi di classe, nei nomi di progetto, nel supporto transazionale o in altre impostazioni del componente, è possibile che non vi siano corrispondenze tra i dati di configurazione nell'explorer Servizi componenti e la configurazione effettiva in esecuzione nel debugger di Visual Basic.
-   Non esportare un'applicazione COM+ durante il debug di un componente nell'applicazione. COM+ considera l'Visual Basic di sviluppo come componente.
-   Se si esegue un componente all'esterno del debugger e quindi si decide di avviare il debug, è possibile che un'istanza del componente sia ancora in esecuzione in COM+ quando viene avviata nel debugger. COM+ rileverà questa condizione e tenterà di arrestare automaticamente l'istanza che controlla. Per evitare questo problema, rimuovere il componente dallo strumento di amministrazione Servizi componenti prima di iniziare il debug.

**Per eseguire il debug usando l'ambiente Visual Basic**

1.  Aprire il progetto del componente in Visual Basic.

2.  Compilare il componente e quindi impostare la compatibilità binaria nel progetto sul componente compilato.

3.  Impostare la proprietà MTSTransactionMode su un valore diverso da 0 - NotAnMTSObject. Quando si avvia il progetto, questa impostazione richiede Visual Basic di attivare il componente all'interno di COM+.

4.  Scegliere **Proprietà dal** menu Project e quindi immettere il programma di avvio nella **scheda** Debug . Il programma di avvio è l'eseguibile client che chiama questo componente.

    > [!Note]  
    > Il programma di avvio deve essere locale per il componente di cui si esegue il debug.

     

5.  Premere F5 per avviare il debug del componente.

Dopo aver premuto F5, Visual Basic avvia l'applicazione client ed esegue il componente in modalità di debug. È possibile inserire punti di interruzione nel codice del componente e impostare espressioni di controllo sulle variabili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto del debug Visual Basic COM+ in contrasto con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



