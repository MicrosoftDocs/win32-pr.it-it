---
description: L'uso di Microsoft Visual Basic Integrated Development Environment (IDE) per il debug offre agli sviluppatori Visual Basic l'accesso a strumenti e semplicità d'uso noti.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Debug nell'IDE di Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401400"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Debug nell'IDE di Visual Basic

L'uso di Microsoft Visual Basic Integrated Development Environment (IDE) per il debug offre agli sviluppatori Visual Basic l'accesso a strumenti e semplicità d'uso noti. Sebbene sia necessario eseguire il debug di molti componenti in modo più completo utilizzando l'ambiente Microsoft Visual C++, una strategia potrebbe consistere nel eseguire prima il debug della maggior parte delle funzionalità possibili con Visual Basic. Ad esempio, è possibile usare l'IDE di Visual Basic per il debug all'interno di COM+ quando non è ancora in corso il debug del multithreading, il rilevamento dei componenti, le chiamate remote o l'isolamento dei processi.

In generale, quando si utilizza l'ambiente Visual Basic per il debug, è necessario innanzitutto compilare il progetto e aggiungere la DLL a un'applicazione COM+. Si imposta quindi la compatibilità binaria per il progetto, si fa riferimento alla DLL creata e si avvia il progetto per avviare il debug.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Linee guida generali per il debug nell'ambiente Visual Basic

-   Durante il debug con Visual Basic, COM+ considera i componenti Visual Basic come se appartengano a un'applicazione di libreria, anche se i componenti sono registrati come appartenenti a un'applicazione server. Poiché viene eseguito come applicazione libreria, le icone dei componenti nello strumento di amministrazione Servizi componenti non vengono spinte durante il debug dei componenti.
-   Se si modificano gli attributi delle transazioni in un componente durante il debug o si crea una modifica del codice sorgente che richiede Visual Basic per generare un nuovo CLSID o ProgID, assicurarsi di eliminare e reinstallare l'applicazione COM+ contenente il componente. Se è stata impostata la compatibilità binaria per il componente, si riceverà un avviso per segnalare che si sono verificate modifiche.

## <a name="notes-on-debugging-within-a-com-application"></a>Note sul debug in un'applicazione COM+

-   Se si apportano modifiche nell'IDE di Visual Basic nelle interfacce del componente, nomi di classi, nomi di progetti, supporto transazionale o altre impostazioni, potrebbe esserci una mancata corrispondenza tra i dati di configurazione in Esplora servizi componenti e la configurazione effettiva in esecuzione nel debugger di Visual Basic.
-   Non esportare un'applicazione COM+ durante il debug di un componente nell'applicazione. COM+ considererà l'ambiente di sviluppo Visual Basic come componente.
-   Se si esegue un componente all'esterno del debugger e si decide di avviare il debug, un'istanza del componente potrebbe essere ancora in esecuzione in COM+ quando viene avviata nel debugger. COM+ rileverà questa condizione e tenterà di arrestare automaticamente l'istanza che controlla. Per evitare questo problema, rimuovere il componente dallo strumento di amministrazione Servizi componenti prima di avviare il debug.

**Per eseguire il debug con l'ambiente Visual Basic**

1.  Aprire il progetto componente in Visual Basic.

2.  Compilare il componente, quindi impostare la compatibilità binaria nel progetto sul componente compilato.

3.  Impostare la proprietà MTSTransactionMode su un valore diverso da 0-NotAnMTSObject. Quando si avvia il progetto, questa impostazione richiede Visual Basic per attivare il componente all'interno di COM+.

4.  Scegliere **Proprietà** dal menu **progetto** , quindi immettere il programma avvia nella scheda **debug** . Il programma di avvio è l'eseguibile del client che chiama il componente.

    > [!Note]  
    > Il programma di avvio deve essere locale per il componente di cui si esegue il debug.

     

5.  Premere il tasto F5 per avviare il debug del componente.

Dopo aver premuto F5, Visual Basic avvia l'applicazione client ed esegue il componente in modalità di debug. È possibile inserire punti di interruzione nel codice del componente e impostare gli orologi sulle variabili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto per il debug di Visual Basic COM+ a differenza di MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



