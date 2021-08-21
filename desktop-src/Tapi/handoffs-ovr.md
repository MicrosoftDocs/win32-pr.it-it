---
description: Quando un'applicazione ha privilegi di proprietario per una sessione di comunicazione, l'applicazione può scegliere di traslare la proprietà a un'altra applicazione.
ms.assetid: d6d188c9-9cbd-45af-93f0-b78850374919
title: Handoff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60668fa5c0138de137e0dab81ba8159d00b7727f7eca699d207128615db5c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866137"
---
# <a name="handoffs"></a>Handoff

Quando un'applicazione ha privilegi [di proprietario per](privilege-ovr.md) una sessione di comunicazione, l'applicazione può scegliere di traslare la proprietà a un'altra applicazione. L'operazione di consegna viene in genere usata per consentire la modifica del tipo di supporto della chiamata. L'applicazione con la priorità più alta per il nuovo tipo di supporto deve prendere e gestire la chiamata. La modifica del tipo di supporto si verifica in genere per uno dei motivi seguenti.

**Comando utente:** Tramite un'interfaccia utente o messaggi finestra, l'applicazione apprende che l'utente locale vuole modificare il tipo di supporto. Ad esempio, l'utente ha detto alla nuova applicazione di destinazione (che non è ancora un proprietario) di ottenere una chiamata vocale esistente per la trasmissione dei dati. L'applicazione di destinazione deve ora assumere il controllo della chiamata. In questo caso, il proprietario corrente nota l'aumento del numero di proprietari e quindi cesa il controllo della chiamata. In alternativa, l'utente può indicare al proprietario corrente della chiamata di consegnarla a un'applicazione in grado di gestire il nuovo tipo di supporto.

**Modifica del tipo di supporto:** Il provider di servizi può rilevare una modifica del tipo di supporto. Ad esempio, l'applicazione locale sta riproducendo un messaggio vocale registrato per il chiamante. Durante questo messaggio, il chiamante decide di trasmettere un segnale acustico per il fax e l'applicazione locale può rispondere di conseguenza modificando il tipo di supporto in fax e, se necessario, consegnando la chiamata a un'applicazione fax. Un altro modo per farlo è consentire a un'applicazione di monitoraggio di abilitare il monitoraggio del tipo di supporto e, quando il tipo di supporto a cui è interessata viene rilevato in una chiamata, può richiedere la proprietà della chiamata. Questo meccanismo rende superfluo per ogni applicazione monitorare ogni chiamata per ogni tipo di supporto.

**Comando entità remota:** L'entità remota può indicare in modo interattivo una modifica nei tipi di supporti durante una chiamata esistente, ad esempio se l'applicazione locale monitora l'input DTMF dal chiamante remoto. Tramite questo monitoraggio, il chiamante indica, ad esempio, che sta per essere inviato un fax. Altri modi in cui il chiamante può controllare le applicazioni locali sono i comandi ricevuti in altre connessioni dati e tramite messaggi di informazioni utente-utente ISDN.

Un handoff di chiamata avrà uno dei risultati seguenti:

-   La chiamata viene data a un'altra applicazione (SUCCESS).
-   L'applicazione di consegna è di per sé la destinazione (TARGETSELF).
-   La consegna ha esito negativo (TARGETNOTFOUND).

Se l'applicazione che riceve la chiamata con consegna ha già un handle di chiamata per la chiamata, viene usato questo handle di chiamata precedente. In caso contrario, viene creato un nuovo handle di chiamata. In entrambi i casi, l'applicazione finisce con i privilegi di proprietario per la chiamata. Ogni volta che l'applicazione di consegna non corrisponde all'applicazione di destinazione, la destinazione viene informata della consegna in un messaggio di stato sessione come se riceveva una nuova chiamata.

Se all'applicazione proprietaria corrente viene richiesta la modifica dei tipi di supporti, questa operazione viene consegni la chiamata a un'applicazione usata per il tipo di supporto di destinazione. I due tipi di handoff delle chiamate sono descritti in [Handoff diretti](#directed-handoffs) e [Handoff del tipo di supporto.](#media-type-handoffs)

Non tutti i provider di servizi supportano l'uso di questa operazione.

**TAPI 2.x:** Vedere [**lineHandoff**](/windows/win32/api/tapi/nf-tapi-linehandoff), con *lpszFileName* impostato sul nome dell'applicazione per un handoff diretto o *dwMediaMode* impostato su un tipo di supporto per un handoff indiretto.

**TAPI 3.x:** Vedere [**ITBasicCallControl::HandoffDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect), [**ITBasicCallControl::HandoffIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect).

## <a name="directed-handoffs"></a>Handoff diretti

Un *handoff diretto si* verifica quando l'applicazione di destinazione è nota per nome all'applicazione originale. Questa situazione si verifica, ad esempio, tra un set di applicazioni scritte dallo stesso fornitore. L'utente può in genere configurare il controllo dei consegnamenti diretti. Con tale consegna, la chiamata viene data all'applicazione specificata se ha aperto la riga in cui esiste la chiamata. Il tipo di supporto specificato al momento dell'apertura della riga da parte dell'applicazione viene ignorato. Un esempio comune è una chiamata vocale seguita da una trasmissione di fax nella stessa chiamata. La consegna diretta viene spesso usata dalle applicazioni dello stesso sviluppatore collegate anche in altri modi.

Il handoff diretto può essere usato anche nelle versioni future come parte del processo di arbitrazione di più applicazioni in attesa di chiamate in ingresso dello stesso tipo di supporto, con la selezione dell'applicazione per gestire la chiamata in base al collegamento dati o al rilevamento del protocollo di livello superiore anziché al tipo di supporto. Un esempio del suo utilizzo potrebbe essere una linea di modem dati in ingresso con applicazioni come acquisizione remota, bollettino, accesso alla rete remota e accesso remoto alla posta elettronica, tutti in attesa di chiamate contemporaneamente.

## <a name="media-type-handoffs"></a>Handoff del tipo di supporto

Un *handoff* del tipo di supporto si verifica quando è presente un nuovo tipo di supporto di destinazione, in genere quando l'applicazione proprietaria determina che il tipo di supporto necessario per la chiamata non è presente o sta per cambiare.

Il processo per un handoff dipendente dai supporti può essere un processo di probe se il tipo di supporto unknown bit è on. È responsabilità dell'applicazione proprietaria scorrere i tipi di supporti per trovare l'applicazione con la priorità più alta. TAPI esegue questo ciclo solo sulla chiamata in ingresso iniziale per trovare il primo proprietario. Non esegue questa operazione per un'operazione di consegna. In caso contrario, un handoff è praticamente uguale all'assegnazione iniziale di una chiamata a un'applicazione. La differenza è il fatto che è possibile impostare un solo tipo di supporto per una consegna indiretta (tipo di supporto).

Poiché è possibile specificare un solo bit del tipo di supporto, la chiamata viene data all'applicazione con la priorità più alta per tale tipo di supporto. Tuttavia, è possibile che più di un tipo di supporto sia da considerare per il handoff. In questo caso, l'applicazione di consegna deve specificare la priorità più alta dei possibili tipi di supporti come parametro.

Se un'applicazione specifica il bit UNKNOWN quando si esegue un handoff di tipo multimediale e il handoff ha esito negativo, significa che un'applicazione sconosciuta in grado di eseguire la determinazione del tipo di supporto non è attualmente in esecuzione. L'applicazione che si sta consegnando deve quindi provare a consegnarlo all'applicazione con priorità più alta registrata per il tipo di supporto di livello successivo.

L'applicazione ricevente è ora responsabile della chiamata. Viene ora ricercato il tipo di supporto effettivo della chiamata. Se l'applicazione è in grado di gestire il tipo di supporto della chiamata, deve assicurarsi che sia l'applicazione con la priorità più alta registrata per tale tipo di supporto. In tal caso, mantiene la chiamata e la elabora normalmente. In caso contrario, la chiamata viene traslata a un'altra applicazione registrata per quel tipo di supporto.

Se, tuttavia, il probe per il tipo di supporto ha esito negativo, l'applicazione tenta di eseguire nuovamente il probe, provando a eseguire le altre possibilità in modalità supporto. Deve prima disattivare il bit del tipo di supporto corrente, quindi provare un altro handoff con un tipo diverso.

Questo processo di probe e consegna continua e i tipi di supporti rimanenti vengono eliminati uno alla volta. Durante il processo, una delle applicazioni potrebbe vedere che il tipo di supporto gestito è nella chiamata e che il handoff ha esito positivo.

L'applicazione deve quindi impostare il tipo di supporto corretto e cancellare tutti gli altri bit del tipo di supporto. In questo modo si informano altre applicazioni interessate del tipo di supporto corretto. Queste altre applicazioni ricevono un messaggio di notifica degli eventi che informa che il tipo di supporto della chiamata è stato modificato.

 

 
