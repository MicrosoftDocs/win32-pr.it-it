---
description: Parametri di raggruppamento
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Parametri di raggruppamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3083c3a7ad0971d6d3334303cf9eaf4c0313c4482825c3623a04a12ae046b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018369"
---
# <a name="grouping-parameters"></a>Parametri di raggruppamento

Un parametro di raggruppamento identifica una raccolta di [sessioni audio](audio-sessions.md) controllate tutte da un singolo controllo del volume nel programma di controllo del volume di sistema, Sndvol. Il parametro di raggruppamento è un GUID che identifica in modo univoco la raccolta all'interno dell'ambito del computer.

Lo scopo di un parametro di raggruppamento è simile a quello del GUID della sessione per una sessione multi-processo. In altre informazioni, il parametro di raggruppamento consente all'utente di controllare una raccolta di flussi da un numero qualsiasi di processi come singola unità. Tuttavia, il parametro di raggruppamento serve a questo scopo in circostanze in cui le sessioni multi-processo non possono fornire una soluzione.

Se più client assegnano i rispettivi flussi a sessioni separate ma assegnano lo stesso parametro di raggruppamento a tutte le sessioni, Sndvol visualizza un singolo controllo del volume per queste sessioni. Per fornire il supporto per i parametri di raggruppamento, Sndvol o qualsiasi applicazione di controllo del volume simile deve eseguire le operazioni seguenti:

-   Prima di visualizzare i controlli volume, controllare i parametri di raggruppamento di tutte le sessioni attive. Raggruppare in un singolo volume controllare tutte le sessioni che hanno lo stesso parametro di raggruppamento.
-   Quando l'utente modifica l'impostazione in un controllo volume per un parametro di raggruppamento specifico, aggiornare i livelli di volume di tutte le sessioni che condividono tale parametro di raggruppamento.

I parametri di raggruppamento consentono di ridurre il numero di controlli del volume visualizzati da Sndvol. Gli utenti potrebbero confondersi se Sndvol ingombra la visualizzazione con troppi controlli. Senza il supporto per i parametri di raggruppamento, Sndvol visualizza sempre un controllo del volume separato per ogni sessione, che potrebbe non essere appropriato in tutte le circostanze. Inoltre, i parametri di raggruppamento offrono un modo pratico per garantire che le sessioni che contengono tipi simili di contenuto audio possano essere facilmente impostate sullo stesso livello di volume.

Come illustrato in precedenza, le API audio di livello superiore assegnano in genere i flussi alla sessione predefinita specifica del processo (identificata dal valore GUID della sessione GUID \_ NULL). Questa impostazione predefinita consente a Sndvol di visualizzare un controllo del volume separato per ogni processo dell'applicazione client, che è spesso il comportamento desiderato. Inoltre, se più istanze dello stesso client vengono eseguite in processi separati ma richiedono un singolo controllo del volume condiviso, i client possono semplicemente assegnare i propri flussi alla stessa sessione tra processi. Nessuno di questi casi richiede l'uso di parametri di raggruppamento. Tuttavia, un caso importante, come esemplificato da Microsoft Internet Explorer, richiede l'uso di parametri di raggruppamento per ottenere il comportamento desiderato.

Internet Explorer consente agli utenti di aprire più finestre del browser e queste finestre potrebbero non essere tutte eseguite nello stesso processo. Gli utenti potrebbero confondersi se Sndvol visualizza un controllo del volume separato per ogni istanza dell'applicazione, tutti con la stessa etichetta, "Internet Explorer". Una sessione tra processi non è una soluzione fattibile in questo caso. Se diverse istanze di Internet Explorer vengono eseguite in processi diversi, potrebbero non essere in grado di assegnare tutti i flussi audio a una singola sessione tra processi. Il motivo è che le finestre Internet Explorer potrebbero eseguire istanze di Windows Media Player o un altro plug-in multimediale che usa un'API audio di livello superiore per riprodurre i flussi audio. Queste API assegnano in genere i flussi in un processo a una sessione predefinita specifica del processo. Internet Explorer non ha alcun controllo sull'assegnazione di questi flussi alle sessioni.

WASAPI risolve questo problema consentendo a ogni istanza di Internet Explorer di accedere ai controlli sessione per la sessione predefinita specifica del processo e di assegnare un parametro di raggruppamento a tale sessione. Se tutte le istanze Internet Explorer lo stesso parametro di raggruppamento a tutte le sessioni audio, Sndvol visualizza un singolo controllo del volume per queste sessioni.

Per impostazione predefinita, una sessione non appartiene ad alcun raggruppamento. Se un client non assegna in modo esplicito una sessione a un raggruppamento, Sndvol visualizza un controllo del volume dedicato per tale sessione. Il valore del parametro di raggruppamento GUID \_ NULL indica che una sessione non appartiene ad alcun raggruppamento. Se nessun client ha assegnato in modo esplicito un parametro di raggruppamento a una sessione, il valore del parametro di raggruppamento per tale sessione è \_ GUID NULL per impostazione predefinita.

Un client può modificare dinamicamente il raggruppamento a cui è assegnata una sessione.

Un raggruppamento può includere qualsiasi combinazione di sessioni tra processi e sessioni specifiche del processo in un [dispositivo endpoint audio.](audio-endpoint-devices.md)

L'interfaccia utente di Sndvol consente all'utente di visualizzare i controlli del volume per un solo dispositivo endpoint audio alla volta. Quando l'utente regola i controlli del volume per un determinato dispositivo, i livelli di volume delle sessioni che si connettono ad altri dispositivi non sono interessati. In particolare, un controllo del volume per un particolare parametro di raggruppamento influisce solo sulle sessioni che condividono il parametro di raggruppamento e sono connesse al dispositivo attualmente selezionato. Una sessione che ha un parametro di raggruppamento identico ma è connessa a un altro dispositivo non è interessata.

Come descritto in precedenza, Sndvol etichetta ogni controllo volume visualizzato con un nome visualizzato e un'icona. Nel caso di un controllo volume per un raggruppamento, Sndvol seleziona arbitrariamente una delle sessioni nel raggruppamento come origine per il nome visualizzato e l'icona che visualizza con il controllo del volume. Pertanto, per garantire che Sndvol visualizzi sempre lo stesso nome visualizzato e lo stesso icona per un raggruppamento, tutte le istanze dell'applicazione che assegnano sessioni a tale raggruppamento devono garantire che le rispettive sessioni hanno lo stesso nome visualizzato e lo stesso icona. Per altre informazioni sui nomi visualizzati e sulle icone, vedere [Sessioni audio](audio-sessions.md).

Un'applicazione come Sndvol può registrarsi per ricevere notifiche quando cambia il parametro di raggruppamento per una sessione. Queste notifiche possono essere utili se l'applicazione memorizza nella cache le informazioni sull'assegnazione delle sessioni ai parametri di raggruppamento. Una notifica informa l'applicazione che le informazioni memorizzate nella cache potrebbero non essere più valide.

Per assegnare un parametro di raggruppamento a una sessione, chiamare il [**metodo IAudioSessionControl::SetGroupingParam.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) Per ottenere il parametro di raggruppamento assegnato a una sessione, chiamare il [**metodo IAudioSessionControl::GetGroupingParam.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessioni audio](audio-sessions.md)
</dt> </dl>

 

 



