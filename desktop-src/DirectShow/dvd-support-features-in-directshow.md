---
description: Funzionalità di supporto DVD in DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Funzionalità di supporto DVD in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f143bab35a8b9a4a0cb12af20c2c2c3b66a0822a24cfc054b1f5d30bd4bc3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107901"
---
# <a name="dvd-support-features-in-directshow"></a>Funzionalità di supporto DVD in DirectShow

La funzionalità del filtro [DVD Navigator](dvd-navigator-filter.md) viene esposta tramite due interfacce, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), che fornisce i metodi "set" per DVD Navigator e [**IDvdInfo2,**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)che fornisce i metodi "get".

DVD Navigator supporta le funzionalità seguenti:

-   Supporto Disartie: è possibile scrivere un'applicazione DVD-dvd-dvd con DVD Navigator. Questa operazione richiede un decodificatore compatibile.
-   Accesso semplificato alle stringhe di informazioni di testo DVD: lo strumento di navigazione DVD analizza queste stringhe e consente alle applicazioni di enumerarle, identificarle e recuperarle facilmente.
-   Controllo del volume audio tramite [ **IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Supporto per la personalizzazione del comportamento dello Strumento di navigazione DVD quando viene eseguito il comando Arresta: le applicazioni possono indicare a DVD Navigator di riprendere dalla posizione corrente quando si riavvia il grafico dei filtri o di avviare la riproduzione dall'inizio del disco.
-   Supporto audio DTS (Digital Digital Digital Systems) e SDDS (Digital Digital Sound). I flussi audio DTS e SDDS vengono riconosciuti dallo strumento di navigazione DVD e passati al decodificatore audio. Per decodificare e riprodurre l'audio è necessario un decodificatore compatibile con DTS o SDDS di terze parti.
-   Supporto migliorato per le modifiche a livello di genitori: lo strumento di spostamento DVD consente a un'applicazione di accettare, rifiutare o ignorare i comandi di modifica a livello di genitori dal disco.
-   Opzioni avanzate per la gestione dello stato dello Strumento di navigazione DVD e la sincronizzazione dei comandi
-   Supporto per l'esecuzione di istruzioni dei fotogrammi, la ricerca accurata dei fotogrammi e la riproduzione inversa. Queste funzionalità richiedono un decodificatore video che le supporti.
-   Possibilità di salvare la posizione corrente in un titolo e di tornarla in qualsiasi momento.
-   Supporto semplificato per gli eventi temporizzato in titoli PGC non sequenziali: per i titoli PGC non sequenziali, DVD Navigator inoltra le informazioni time code non elaborati all'applicazione.
-   Informazioni sul codice temporale. La [**struttura \_ \_ TIMECODE del DVD HMSF**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) può essere usata al posto del formato BCD (Binary Coded Decimal). **DVD \_ HMSF \_ TIMECODE contiene** membri facilmente accessibili per ore, minuti, secondi e frame e può essere eseguito il cast a/da un **ULONG.**
-   Possibilità di controllare se il grafico dei filtri viene scaricato dopo un'operazione di ricerca: i buffer del grafo possono contenere fino a pochi secondi di video in qualsiasi momento. È possibile indicare al grafo di completare la riproduzione del video memorizzato nel buffer dopo una ricerca o di iniziare immediatamente la riproduzione nella nuova posizione.
-   Possibilità di impostare valori nei registri di parametri generali: funzionalità avanzata per gli utenti che hanno familiarità con la specifica DVD che desiderano implementare funzionalità avanzate.
-   Possibilità di generare identificatori di disco numerici univoci per tutti gli scopi pratici

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>Quali sono le informazioni di base necessarie per scrivere un'applicazione DVD?

Tutti gli sviluppatori di applicazioni devono avere una conoscenza di base delle funzionalità fornite dalla tecnologia DVD, ad esempio i livelli di gestione dei genitori, più flussi audio e di sottopanoture e blocchi angolari. [Dvd Basics](dvd-basics.md) descrive brevemente ognuna di queste funzionalità. sono disponibili descrizioni più complete nelle pubblicazioni di terze parti. Non è necessario fare riferimento alla specifica DVD a meno che non si intenda implementare funzionalità avanzate oltre il set di comandi Annex J.

Gli sviluppatori C/C++ che usano DirectShow devono avere familiarità con le tecniche di programmazione client COM, ad esempio la creazione di oggetti COM e il recupero e il rilascio di puntatori a interfaccia COM. Potrebbe anche essere necessaria una conoscenza generale delle operazioni del grafo dei filtri, perché potrebbe essere necessario accedere al grafo e modificarlo direttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



