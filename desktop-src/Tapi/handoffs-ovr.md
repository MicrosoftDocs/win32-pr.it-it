---
description: Quando un'applicazione dispone del privilegio proprietario per una sessione di comunicazione, l'applicazione può scegliere di passare la proprietà a un'altra applicazione.
ms.assetid: d6d188c9-9cbd-45af-93f0-b78850374919
title: Handoff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343815e35f1fc331c57c4aa2d9d311697cab7022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308613"
---
# <a name="handoffs"></a>Handoff

Quando un'applicazione dispone del [privilegio](privilege-ovr.md) proprietario per una sessione di comunicazione, l'applicazione può scegliere di passare la proprietà a un'altra applicazione. L'operazione di consegna viene in genere utilizzata per consentire la modifica del tipo di supporto della chiamata. L'applicazione con priorità più elevata per il nuovo tipo di supporto deve eseguire e gestire la chiamata. La modifica del tipo di supporto in genere viene eseguita per uno dei motivi seguenti.

**Comando utente:** Tramite un'interfaccia utente o i messaggi della finestra, l'applicazione apprende che l'utente locale desidera modificare il tipo di supporto. Ad esempio, l'utente ha comunicato alla nuova applicazione di destinazione, che non è ancora un proprietario, di ottenere una chiamata vocale esistente per la trasmissione dei dati. L'applicazione di destinazione deve ora assumere il controllo della chiamata. In questo caso, il proprietario corrente rileva il numero di proprietari che aumentano e quindi cede il controllo della chiamata. In alternativa, l'utente può indicare al proprietario corrente della chiamata di passarlo a un'applicazione in grado di gestire il nuovo tipo di supporto.

**Modifica del tipo di supporto:** Il provider di servizi può rilevare una modifica del tipo di supporto. Ad esempio, l'applicazione locale sta riproducendo un messaggio vocale registrato al chiamante. Durante questo messaggio, il chiamante decide spontaneamente di trasmettere un tono di chiamata fax e l'applicazione locale può rispondere di conseguenza modificando il tipo di supporto in fax e, se necessario, passando la chiamata a un'applicazione fax. Un altro modo per eseguire questa operazione è che un'applicazione di monitoraggio possa abilitare il monitoraggio del tipo di supporto e, quando il tipo di supporto di cui è interessato viene rilevato in una chiamata, può richiedere la proprietà della chiamata. Questo meccanismo rende superfluo per ogni applicazione monitorare ogni chiamata per ogni tipo di supporto.

**Comando entità remota:** La parte remota può indicare in modo interattivo una modifica nei tipi di supporto durante una chiamata esistente, ad esempio se l'applicazione locale monitora l'input DTMF da parte del chiamante remoto. Tramite questo monitoraggio, il chiamante indica, ad esempio, che è in corso l'invio di un fax. Gli altri modi in cui il chiamante può controllare le applicazioni locali sono i comandi ricevuti su altre connessioni dati e i messaggi informativi dell'utente ISDN.

Una chiamata di consegna avrà uno dei seguenti risultati:

-   La chiamata viene assegnata a un'altra applicazione (ESITo positivo).
-   L'applicazione di gestione è la destinazione (TARGETSELF).
-   La consegna ha esito negativo (TARGETNOTFOUND).

Se l'applicazione che riceve la chiamata gestita ha già un handle di chiamata alla chiamata, viene usato questo handle di chiamata precedente. In caso contrario, viene creato un nuovo handle di chiamata. In entrambi i casi, l'applicazione termina con privilegi di proprietario per la chiamata. Ogni volta che l'applicazione di destinazione non corrisponde all'applicazione di destinazione, la destinazione viene informata sulla consegna in un messaggio di stato della sessione come se ricevesse una nuova chiamata.

Se all'applicazione del proprietario corrente viene richiesto di modificare i tipi di supporti, viene eseguita la chiamata a un'applicazione utilizzata per il tipo di supporto di destinazione. I due tipi di chiamata handoff sono descritti in [handoff diretto](#directed-handoffs) e [Media Type handoff](#media-type-handoffs).

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**lineHandoff**](/windows/win32/api/tapi/nf-tapi-linehandoff), con *lpszFileName* impostato sul nome dell'applicazione per una consegna diretta o *dwMediaMode* impostato su un tipo di supporto per una consegna indiretta.

**TAPI 3. x:** Vedere [**ITBasicCallControl:: HandoffDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect), [**ITBasicCallControl:: HandoffIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect).

## <a name="directed-handoffs"></a>Handoff diretto

Una consegna *diretta* si verifica quando l'applicazione di destinazione è nota per nome all'applicazione originale. Questa situazione si verifica, ad esempio, tra un set di applicazioni scritte dallo stesso fornitore. L'utente può in genere configurare il controllo dei handoff diretti. Con tale operazione, la chiamata viene assegnata all'applicazione specificata se ha aperto la riga in cui è presente la chiamata. Il tipo di supporto specificato al momento dell'apertura dell'applicazione la riga viene ignorato. Un esempio comune è una chiamata vocale seguita da una trasmissione fax nella stessa chiamata. La consegna diretta verrà utilizzata più spesso dalle applicazioni dello stesso sviluppatore collegate anche in altri modi.

La consegna diretta può essere usata anche nelle versioni future come parte del processo di arbitrali di più applicazioni in attesa di chiamate in ingresso dello stesso tipo di supporto, con la selezione dell'applicazione per gestire la chiamata in base al rilevamento del protocollo di collegamento dati o di livello superiore anziché al tipo di supporto. Un esempio di utilizzo è costituito da una linea di modem dati in ingresso con applicazioni quali l'acquisizione remota, la bacheca, l'accesso alla rete remota e l'accesso remoto alla posta elettronica in attesa di chiamate simultanee.

## <a name="media-type-handoffs"></a>Tipo di supporto handoff

Una consegna del *tipo di supporto* si verifica quando è presente un nuovo tipo di supporto di destinazione, in genere quando l'applicazione proprietaria stabilisce che il tipo di supporto necessario per la chiamata non è presente o sta per essere modificato.

Il processo di una consegna dipendente dal supporto può essere un processo di sondaggio se il tipo di supporto è sconosciuto. È responsabilità dell'applicazione proprietario scorrere i tipi di supporto per trovare l'applicazione con priorità più elevata. TAPI esegue questa operazione in modo ciclico solo sulla chiamata iniziale in ingresso per trovare il primo proprietario. Questa operazione non viene eseguita per un'operazione di continuità. In caso contrario, la consegna è praticamente identica a quella dell'assegnazione iniziale di una chiamata a un'applicazione. La differenza consiste nel fatto che è possibile impostare un solo tipo di supporto per una consegna indiretta (tipo di supporto).

Poiché è possibile specificare un solo bit di tipo di supporto, la chiamata viene assegnata all'applicazione con priorità più elevata per quel tipo di supporto. Tuttavia, è possibile che più di un tipo di supporto debba essere considerato per la consegna. In questo caso, l'applicazione di gestione deve specificare la priorità più alta dei tipi di supporti possibili come parametro.

Se un'applicazione specifica il bit sconosciuto quando si esegue una consegna del tipo di supporto e la consegna ha esito negativo, significa che un'applicazione sconosciuta in grado di eseguire la determinazione del tipo di supporto non è attualmente in esecuzione. L'applicazione che viene gestita deve quindi provare a consegnare la chiamata all'applicazione con la priorità più alta registrata per il tipo di supporto successivo.

L'applicazione ricevente è ora responsabile della chiamata. Ora esegue il probe per il tipo di supporto effettivo della chiamata. Se l'applicazione è in grado di gestire il tipo di supporto della chiamata, è necessario assicurarsi che sia l'applicazione con priorità più elevata registrata per tale tipo di supporto. In tal caso, mantiene la chiamata e la elabora normalmente. In caso contrario, passa la chiamata a un'altra applicazione registrata per quel tipo di supporto.

Se, tuttavia, il probe per quel tipo di supporto ha esito negativo, l'applicazione esegue nuovamente il probe, tentando di eseguire le rimanenti opzioni della modalità supporto. Prima di tutto, è necessario disattivare il bit del tipo di supporto corrente, quindi provare a eseguire un'altra consegna con un tipo diverso.

Questo processo di probe e disattivazione continua e i restanti tipi di supporti vengono eliminati uno alla volta. Lungo il percorso, una delle applicazioni potrebbe vedere che il tipo di supporto che gestisce si trova nella chiamata e la consegna è riuscita.

L'applicazione deve quindi impostare il tipo di supporto corretto e deselezionare tutti gli altri bit del tipo di supporto. Ciò informa le altre applicazioni interessate del tipo di supporto corretto. Queste altre applicazioni ricevono un messaggio di notifica degli eventi che indica che il tipo di supporto della chiamata è stato modificato.

 

 
