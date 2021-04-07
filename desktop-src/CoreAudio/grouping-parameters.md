---
description: Raggruppamento di parametri
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Raggruppamento di parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfb674d4349f351ce36fe1e236d1ecd3b265d8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748383"
---
# <a name="grouping-parameters"></a>Raggruppamento di parametri

Un parametro di raggruppamento identifica una raccolta di [sessioni audio](audio-sessions.md) che sono tutte controllate da un singolo controllo volume nel programma di controllo del volume di sistema, sndvol. Il parametro GROUPING è un GUID che identifica in modo univoco la raccolta nell'ambito del computer.

Lo scopo di un parametro di raggruppamento è simile a quello del GUID della sessione per una sessione tra processi. Ovvero il parametro GROUPING consente all'utente di controllare una raccolta di flussi da un numero qualsiasi di processi come una singola unità. Tuttavia, il parametro GROUPING serve a questo scopo in circostanze in cui le sessioni tra processi non possono fornire una soluzione.

Se più client assegnano i rispettivi flussi a sessioni separate, ma assegnano lo stesso parametro di raggruppamento a tutte le sessioni, sndvol Visualizza un singolo controllo volume per queste sessioni. Per fornire supporto per il raggruppamento di parametri, sndvol o qualsiasi applicazione di controllo del volume simile deve eseguire le operazioni seguenti:

-   Prima di visualizzare i controlli del volume, controllare i parametri di raggruppamento di tutte le sessioni attive. Raggruppare in un singolo volume controllare tutte le sessioni con lo stesso parametro di raggruppamento.
-   Quando l'utente modifica l'impostazione in un controllo del volume per un determinato parametro di raggruppamento, aggiornare i livelli del volume di tutte le sessioni che condividono tale parametro di raggruppamento.

I parametri di raggruppamento consentono di ridurre il numero di controlli del volume visualizzati da sndvol. Gli utenti potrebbero essere confusi se sndvol ingombra la visualizzazione con troppi controlli. Senza il supporto per il raggruppamento dei parametri, sndvol Visualizza sempre un controllo del volume separato per ogni sessione, che potrebbe non essere appropriato in tutte le circostanze. Inoltre, i parametri di raggruppamento rappresentano un modo pratico per garantire che le sessioni che contengono tipi simili di contenuto audio possano essere facilmente impostate sullo stesso livello di volume.

Come spiegato in precedenza, le API audio di livello superiore in genere assegnano i flussi alla sessione predefinita specifica del processo (identificata dal GUID del valore GUID della sessione \_ null). Questa impostazione predefinita consente a sndvol di visualizzare un controllo del volume separato per ogni processo dell'applicazione client, che è spesso il comportamento desiderato. Inoltre, se più istanze dello stesso client vengono eseguite in processi distinti ma richiedono un singolo controllo del volume condiviso, i client possono semplicemente assegnare i propri flussi alla stessa sessione tra processi. Nessuno di questi casi richiede l'utilizzo di parametri di raggruppamento. Tuttavia, un caso importante, come esemplificato da Microsoft Internet Explorer, richiede l'uso di parametri di raggruppamento per ottenere il comportamento desiderato.

Internet Explorer consente agli utenti di aprire più finestre del browser e queste finestre potrebbero non essere tutte eseguite nello stesso processo. Gli utenti possono essere confusi se sndvol Visualizza un controllo del volume separato per ogni istanza dell'applicazione, tutti con la stessa etichetta "Internet Explorer". Una sessione tra processi non è una soluzione fattibile, in questo caso, se più istanze di Internet Explorer vengono eseguite in processi diversi, potrebbero non essere in grado di assegnare tutti i flussi audio a una singola sessione tra processi. Il motivo è che le finestre di Internet Explorer potrebbero eseguire istanze di Windows Media Player o altri plug-in multimediali che usano un'API audio di livello superiore per riprodurre i flussi audio. Queste API in genere assegnano i flussi in un processo a una sessione predefinita specifica del processo. Internet Explorer non ha alcun controllo sull'assegnazione di questi flussi alle sessioni.

WASAPI risolve questo problema consentendo a ogni istanza di Internet Explorer di accedere ai controlli della sessione per la sessione predefinita specifica del processo e di assegnare un parametro di raggruppamento a tale sessione. Se tutte le istanze di Internet Explorer assegnano lo stesso parametro di raggruppamento a tutte le sessioni audio, sndvol visualizzerà un singolo controllo volume per queste sessioni.

Per impostazione predefinita, una sessione non appartiene ad alcun raggruppamento. Se un client non assegna una sessione in modo esplicito a un raggruppamento, sndvol visualizzerà un controllo volume dedicato per tale sessione. Il valore del parametro di raggruppamento GUID \_ null indica che una sessione non appartiene ad alcun raggruppamento. Se nessun client ha assegnato in modo esplicito un parametro di raggruppamento a una sessione, il valore del parametro di raggruppamento per tale sessione è \_ null per impostazione predefinita.

Un client può modificare dinamicamente il raggruppamento a cui è assegnata una sessione.

Un raggruppamento può includere qualsiasi combinazione di sessioni tra processi e sessioni specifiche del processo in un [dispositivo endpoint audio](audio-endpoint-devices.md).

L'interfaccia utente di sndvol consente all'utente di visualizzare i controlli volume solo per un dispositivo dell'endpoint audio alla volta. Quando l'utente modifica i controlli del volume per un particolare dispositivo, i livelli di sessioni del volume che si connettono ad altri dispositivi non sono interessati. In particolare, un controllo volume per un determinato parametro di raggruppamento ha effetto solo sulle sessioni che condividono il parametro di raggruppamento e sono connesse al dispositivo attualmente selezionato. Una sessione che ha un parametro di raggruppamento identico ma è connessa a un altro dispositivo non è interessata.

Come descritto in precedenza, sndvol etichetta ogni controllo volume visualizzato con un nome visualizzato e un'icona. Nel caso di un controllo volume per un raggruppamento, sndvol seleziona arbitrariamente una delle sessioni nel raggruppamento come origine per il nome visualizzato e l'icona visualizzata con il controllo volume. Pertanto, per assicurarsi che sndvol visualizzi sempre lo stesso nome visualizzato e l'icona per un raggruppamento, tutte le istanze dell'applicazione che assegnano sessioni a tale raggruppamento devono garantire che le rispettive sessioni abbiano lo stesso nome visualizzato e l'icona. Per ulteriori informazioni sui nomi visualizzati e sulle icone, vedere [sessioni audio](audio-sessions.md).

Un'applicazione come sndvol può registrarsi per ricevere notifiche in caso di modifica del parametro di raggruppamento per una sessione. Queste notifiche possono essere utili se l'applicazione memorizza nella cache le informazioni sull'assegnazione delle sessioni ai parametri di raggruppamento. Una notifica informa l'applicazione che le informazioni memorizzate nella cache potrebbero non essere più valide.

Per assegnare un parametro di raggruppamento a una sessione, chiamare il metodo [**IAudioSessionControl:: SetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) . Per ottenere il parametro di raggruppamento assegnato a una sessione, chiamare il metodo [**IAudioSessionControl:: GetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessioni audio](audio-sessions.md)
</dt> </dl>

 

 



