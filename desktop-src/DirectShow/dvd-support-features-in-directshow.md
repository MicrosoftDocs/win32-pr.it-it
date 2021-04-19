---
description: Funzionalità di supporto DVD in DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Funzionalità di supporto DVD in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035af51bbe44ec8dcc95f199c502b71d37d834f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304014"
---
# <a name="dvd-support-features-in-directshow"></a>Funzionalità di supporto DVD in DirectShow

La funzionalità del filtro di [DVD Navigator](dvd-navigator-filter.md) viene esposta tramite due interfacce, [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), che fornisce i metodi "set" per il navigatore DVD e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), che fornisce i metodi "Get".

Il navigatore DVD supporta le funzionalità seguenti:

-   Supporto per Karaoke: è possibile scrivere un'applicazione DVD-karaoke usando il navigatore DVD. Questa operazione richiede un decodificatore compatibile.
-   Accesso semplificato alle stringhe di informazioni di testo DVD: il navigatore DVD analizza queste stringhe e consente alle applicazioni di enumerarle, identificarle e recuperarle facilmente.
-   Controllo del volume audio tramite [ **IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Supporto per la personalizzazione del comportamento del navigatore DVD quando viene emesso il comando di arresto: le applicazioni possono indicare allo strumento di spostamento DVD di riprendersi dalla posizione corrente al riavvio del grafico del filtro oppure avviare la riproduzione dall'inizio del disco.
-   Digital Theater Systems (DTS) e supporto audio di Sony Dynamic Digital Sound (SDD). I flussi audio DTS e SDD sono riconosciuti dal navigatore DVD e passati al decodificatore audio. Per decodificare e riprodurre l'audio è necessario un decodificatore compatibile con DTS di terze parti o compatibile con SDD.
-   Supporto migliorato per le modifiche a livello padre: il navigatore DVD consente a un'applicazione di accettare, rifiutare o ignorare i comandi di modifica a livello padre dal disco.
-   Opzioni avanzate per la gestione dello stato del navigatore DVD e la sincronizzazione dei comandi
-   Supporto per l'esecuzione dei frame, la ricerca con precisione del frame e la riproduzione inversa. Queste funzionalità richiedono un decodificatore video che li supporta.
-   Possibilità di salvare il percorso corrente in un titolo e di restituirlo in qualsiasi momento.
-   Supporto semplificato per gli eventi temporali nei titoli PGC non sequenziali: per i titoli PGC non sequenziali, il navigatore DVD inoltra le informazioni sul codice dell'ora non elaborata all'applicazione.
-   Informazioni del codice temporale. La struttura del [**\_ \_ timecode del HMSF DVD**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) può essere usata al posto del formato decimale codificato binario (BCD). **DVD \_ di Il \_ timecode HMSF** contiene membri facilmente accessibili per ore, minuti, secondi e frame ed è possibile eseguirne il cast a/da un **ULONG**.
-   La possibilità di controllare se il grafico del filtro viene scaricato dopo un'operazione di ricerca: i buffer del grafico possono contenere fino a pochi secondi di video in un determinato momento. È possibile impostare il grafico in modo da terminare la riproduzione del video memorizzato nel buffer dopo una ricerca o iniziare subito la riproduzione nella nuova posizione.
-   La possibilità di impostare i valori in registri parametri generali: una funzionalità avanzata per coloro che hanno familiarità con la specifica DVD che desiderano implementare funzionalità avanzate.
-   Possibilità di generare identificatori di dischi numerici per tutti gli scopi pratici specifici

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>Quali sono I retroscena necessari per scrivere un'applicazione DVD?

Tutti gli sviluppatori di applicazioni devono avere una conoscenza di base delle funzionalità fornite dalla tecnologia DVD, ad esempio i livelli di gestione padre, più flussi audio e di sottoimmagine e blocchi angolari. Le [nozioni di base sui DVD](dvd-basics.md) descrivono brevemente ognuna di queste funzionalità. le descrizioni più complete sono disponibili nelle pubblicazioni di terze parti. Non è necessario fare riferimento alla specifica DVD, a meno che non si intenda implementare funzionalità avanzate oltre al set di comandi allegato J.

Gli sviluppatori C/C++ che usano DirectShow dovrebbero avere familiarità con le tecniche di programmazione dei client COM, come la creazione di oggetti COM e il recupero e il rilascio di puntatori di interfaccia COM. Potrebbe inoltre essere necessaria una conoscenza generale delle operazioni di filtro dei grafici, perché potrebbe essere necessario accedere al grafo e modificarlo direttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



