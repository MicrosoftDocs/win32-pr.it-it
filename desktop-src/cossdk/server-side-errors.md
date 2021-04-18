---
description: Errori Server-Side
ms.assetid: ce8ddb52-237c-4d46-a088-9f592afadcd2
title: Errori Server-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7946b8197553874b8da22d35f8fab5b83f14862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304935"
---
# <a name="server-side-errors"></a>Errori Server-Side

Il listener e il lettore collaborano per gestire i messaggi non elaborabili. Se una transazione riprodotta non riesce, [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) sposta di nuovo il messaggio di input nella coda di input. Il giocatore interrompe la transazione se riceve un HRESULT con esito negativo dal componente server o se intercetta un'eccezione. Se il problema persiste, il listener potrebbe scorrere in modo continuo nel modello seguente:

-   Rimuove il messaggio dalla coda
-   Crea un'istanza dell'oggetto
-   Subisce un rollback
-   Riporta il messaggio nella parte superiore della coda

Il servizio componenti in coda gestisce questo errore utilizzando una serie di code di tentativi specifiche dell'applicazione. Creato quando viene installato il componente, sono presenti sette code per ogni applicazione, come indicato di seguito:

1.  Coda di input normale. Il nome di questa coda è il nome dell'applicazione COM+. Coda pubblica di Accodamento messaggi.

2.  Prima coda di tentativi. I messaggi vengono spostati qui se la transazione ha ripetutamente esito negativo durante l'elaborazione dei messaggi dalla coda di input normale. I messaggi in questa coda vengono elaborati dopo un minuto. Un messaggio può essere ripetuto tre volte in questa coda prima di essere spostato nella parte posteriore della seconda coda dei tentativi. Questa coda è denominata *ApplicationName* \_ 0. Questa coda è una coda di Accodamento messaggi privata.

3.  Seconda coda dei tentativi. I messaggi vengono spostati qui se la transazione ha ripetutamente esito negativo durante l'elaborazione dei messaggi dalla prima coda di tentativi. I messaggi in questa coda vengono elaborati dopo due minuti. Un messaggio può essere ripetuto tre volte in questa coda prima di essere spostato nella parte posteriore della terza coda di tentativi. Questa coda è denominata *ApplicationName* \_ 1. Questa coda è una coda di Accodamento messaggi privata.

4.  Terza coda di tentativi. I messaggi vengono spostati qui se la transazione ha ripetutamente esito negativo durante l'elaborazione dei messaggi dalla seconda coda di tentativi. I messaggi in questa coda vengono elaborati dopo quattro minuti. Un messaggio può essere ripetuto tre volte in questa coda prima di essere spostato nella parte posteriore della quarta coda dei tentativi. Questa coda è denominata *ApplicationName* \_ 2. Questa coda è una coda di Accodamento messaggi privata.

5.  Quarta coda di tentativi. I messaggi vengono spostati qui se la transazione ha ripetutamente esito negativo durante l'elaborazione dei messaggi dalla terza coda di tentativi. I messaggi in questa coda vengono elaborati dopo otto minuti. Un messaggio può essere ripetuto tre volte in questa coda prima di essere spostato nella quinta coda di tentativi. Questa coda è denominata *ApplicationName* \_ 3. Questa coda è una coda di Accodamento messaggi privata.

6.  Quinta coda di tentativi. I messaggi vengono spostati qui se la transazione ha ripetutamente esito negativo durante l'elaborazione dei messaggi dalla quarta coda di tentativi. I messaggi in questa coda vengono elaborati dopo sedici minuti. Un messaggio può essere ripetuto tre volte in questa coda prima di essere spostato nella coda di riposo finale. Questa coda è denominata *ApplicationName* \_ 4. Coda di Accodamento messaggi privata.

7.  Coda di riposo finale specifica dell'applicazione. I messaggi vengono spostati qui se la transazione si interrompe ripetutamente quando viene eseguito un tentativo nella quinta coda di tentativi. Questa coda è denominata *ApplicationName* \_ DeadQueue. Coda di Accodamento messaggi privata. La coda di riposo finale non viene gestita da un listener della coda. I messaggi rimangono qui fino a quando non vengono spostati manualmente (probabilmente dall'utilità del Mover dei componenti in coda) o eliminati da Esplora Accodamento messaggi.

Messaggi non riproducibili perché è chiaro che ogni nuovo tentativo avrà esito negativo e sarà possibile spostarli direttamente nella coda di riposo finale specifica dell'applicazione senza essere avanzati attraverso tutti i livelli di ripetizione dei tentativi.

Il lettore emette un evento COM+ per notificare alle parti interessate che i messaggi non possono essere riprodotti. Gli eventi COM+ vengono rilasciati nelle situazioni seguenti:

-   Interruzione di una transazione
-   Quando un messaggio viene spostato da una coda a un'altra
-   Quando un messaggio viene depositato nella coda di riposo finale

I messaggi possono essere modificati prima di essere spostati da una coda a un'altra. Il meccanismo di sicurezza dei componenti in coda COM+ consente lo spostamento di un messaggio in code di tentativi e quindi il reinserimento nella coda di input iniziale dell'applicazione. Per ulteriori informazioni sulla sicurezza dei componenti in coda, vedere [sicurezza dei componenti in coda](queued-components-security.md).

Le code di tentativi vengono create insieme alla coda dell'applicazione principale quando l'applicazione è contrassegnata come accodata dallo strumento di amministrazione Servizi componenti o utilizzando le funzioni SDK di amministrazione COM+. Il servizio componenti in coda consente di garantire flessibilità nel meccanismo di ripetizione dei tentativi consentendo l'eliminazione delle code di tentativi. Se, ad esempio, vengono eliminate tutte le code di tentativi, un messaggio che si interrompe in modo permanente verrà spostato direttamente dalla coda dell'applicazione alla coda di riposo finale specifica dell'applicazione. Rimuovendo una o più code di tentativi, è possibile ridurre il numero e la lunghezza dei tentativi. Se le code vengono rimosse dalla sequenza di ripetizione dei tentativi, l'intervallo delle code rimanenti corrisponde alla posizione nella sequenza delle code di ripetizione dei tentativi. Se, ad esempio, si rimuove Retry Queue *ApplicationName* \_ 1, *ApplicationName* \_ 2 e *ApplicationName* \_ 3, i messaggi in *ApplicationName* \_ 4 verrebbero elaborati come se la coda fosse la seconda coda di tentativi.

Il meccanismo di ripetizione dei tentativi è progettato per completare un messaggio, se possibile. In alcuni casi, potrebbe non essere possibile che il messaggio abbia esito positivo. È ad esempio possibile che un client tenti di prelevare denaro da un account che non dispone di fondi sufficienti. In questi casi, è possibile gestire l'errore in diversi modi, inclusi i seguenti:

-   Genera una diagnostica ed emette un avviso
-   Creare una transazione di compensazione
-   Ignorare il problema e chiudere il messaggio

Analogamente agli errori persistenti sul lato client, il servizio componenti in coda consente di associare una classe di eccezione a un componente. La classe Exception è associata al componente utilizzando la scheda **Avanzate** della pagina Proprietà componente dello strumento di amministrazione Servizi componenti o utilizzando le funzioni amministrative com+. La classe Exception consente allo sviluppatore di avere il controllo dopo che un messaggio è stato ritentato e prima che il messaggio venga spostato nella coda di riposo finale specifica dell'applicazione. Per ulteriori informazioni sulla classe Exception, vedere la pagina relativa agli [errori persistenti Client-Side](persistent-client-side-failures.md).

Di seguito è riportata la sequenza di eventi per la gestione delle eccezioni lato server:

1.  Il messaggio viene spostato attraverso le code di tentativi specifiche dell'applicazione disponibili.
2.  Il tentativo finale sull'ultima coda di tentativi ha esito negativo.
3.  Il runtime del servizio componenti in coda recupera il componente di destinazione dal messaggio e verifica la presenza di una classe di eccezione.
4.  La fase di esecuzione crea un'istanza della classe Exception.
5.  Le query di run-time [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) sulla classe Exception.
6.  La fase di esecuzione chiama [**IPlaybackControl:: FinalServerRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalserverretry) nella classe Exception.
7.  Il runtime riproduce tutte le chiamate a proprietà e metodi dal messaggio alla classe di eccezione.
8.  Se i passaggi da 4 a 6 non hanno esito positivo, il runtime sposta il messaggio nella coda di riposo finale specifica dell'applicazione.

Se è necessario intervenire nel processo descritto in precedenza o se è necessario spostare un messaggio non elaborabile dalla coda di riposo finale, usare l'utilità del Mover del messaggio. Per ulteriori informazioni sull'utilità Message Mover, vedere [gestione degli errori](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori lato client](client-side-errors.md)
</dt> <dt>

[Errori persistenti Client-Side](persistent-client-side-failures.md)
</dt> </dl>

 

 



