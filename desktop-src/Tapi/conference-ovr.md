---
description: Per la conferenza avanzata con reti basate su IP è descritta la conferenza telefonia IP di TAPI 3 Rendezvous. Il materiale seguente si riferisce alle conferenze di base.
ms.assetid: f685097b-1b54-412b-999f-d9bdb3120ab9
title: Conferenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace4cb45bf74335298a3d4d262d064eb85c547f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308307"
---
# <a name="conference"></a>Conferenza

La conferenza avanzata con reti basate su IP è descritta nella conferenza di [telefonia IP Rendezvous](rendezvous-ip-telephony-conferencing.md)di TAPI 3. Il materiale seguente si riferisce alle conferenze di base.

Le sessioni di conferenza sono sessioni che includono più di due parti simultaneamente. Possono essere configurate usando un Bridge basato su server esterno o un Bridge di conferenze basato su switch.

Nelle sessioni di conferenze basate su server, tutte le parti partecipanti effettuano la connessione al server, che combina i flussi multimediali e invia ogni partecipante alla combinazione. Potrebbe non essere presente alcuna nozione di singole parti nella chiamata Conference, bensì solo quella di una singola chiamata tra l'applicazione e il server Bridge. Per TAPI, questo tipo di chiamata di conferenza sembra essere una normale connessione uno-a-uno.

Le conferenze basate su switch procedono in fasi, alcune delle quali possono essere combinate se il provider di servizi lo supporta:

1.  Avviare una sessione di comunicazione ordinaria.
2.  Creare una sessione di conferenza con il primo membro dell'entità che ha avviato la conferenza.
3.  Creare una sessione di consultazione della conferenza con l'entità all'altra estremità della connessione corrente.
4.  Aggiungere la sessione di consultazione alla conferenza.

Dopo che una sessione diventa un membro di una conferenza, lo stato del membro torna a CONFERENCED. Lo stato della sessione di conferenza viene in genere *connesso*. Gli identificatori di sessione per la conferenza e tutte le entità aggiunte rimangono validi. Gli eventi di stato possono essere ricevuti su tutte le chiamate. Se, ad esempio, uno dei membri si disconnette bloccando, un messaggio di stato appropriato può informare l'applicazione di questo fatto.

**TAPI 2. x:** Le applicazioni possono usare la funzionalità "nessuna conferenza di attesa" di PBX usando l' \_ opzione LINECALLPARAMFLAGS NOHOLDCONFERENCE. questa funzionalità consente a un altro dispositivo, ad esempio un supervisore o un dispositivo di registrazione, di essere collegato automaticamente alla riga.

Quando si annulla la sessione di consultazione per una conferenza o quando si rimuove la terza parte di una conferenza stabilita in precedenza, il provider di servizi può rilasciare la conferenza e ripristinare la sessione in una normale connessione a due parti. In tal caso, la sessione di conferenza passerà allo stato *inattivo* e l'unica sessione rimanente verrà trascinata da conferenced a stato *connesso* .

Non tutti i provider di servizi supportano la conferenza.

**TAPI 2. x:** La funzione [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference) accetta la chiamata a due parti originale come input, alloca una chiamata di conferenza, connette la chiamata originale alla conferenza e alloca una chiamata di consultazione il cui handle viene restituito all'applicazione.

Se l'applicazione aggiunge un altro membro alla conferenza, è possibile eseguire un'operazione di connessione alla chiamata di consultazione. L'handle di chiamata della conferenza e la connessione alla chiamata di consultazione vengono quindi usati nella funzione [**lineAddToConference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) . I membri della conferenza possono anche essere aggiunti tramite la funzione [**linePrepareAddToConference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) , se supportata dal provider di servizi.

I membri della conferenza vengono rimossi usando la funzione [**lineRemoveFromConference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) , se il provider di servizi lo supporta.

In alternativa, è possibile creare una conferenza utilizzando la funzione [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) , che restituisce un handle di chiamata di consultazione e la funzione [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) con l'opzione Conference, anziché l'opzione [Transfer](transfer-ovr.md) .

**TAPI 3. x:** Il metodo [**ITBasicCallControl:: Conference**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) accetta la sessione esistente come input e crea un [oggetto CallHub](callhub-object.md) se non ne esiste già uno. Il metodo [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) aggiunge la chiamata di consultazione a CallHub. È possibile creare sessioni di consultazione aggiuntive con [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)e aggiungerle usando i metodi **Conference** e **Finish** .

> [!Note]  
> Le funzionalità del dispositivo a linee interessate possono limitare il numero di entità che vengono contrattate in una singola chiamata e se una conferenza inizia con una normale chiamata a due parti.

 

 

 
