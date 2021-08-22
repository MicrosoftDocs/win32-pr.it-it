---
description: Il server pipe specifica le modalità di accesso, sovrapposizione e write-through della pipe nel parametro dwOpenMode della funzione CreateNamedPipe. I client pipe possono specificare queste modalità aperte per i relativi handle di pipe usando la funzione CreateFile.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Modalità di apertura named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7fe3f843a157e69d8b938630e5eb9efa95035960cb6578325be6bddd5d93c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451261"
---
# <a name="named-pipe-open-modes"></a>Modalità di apertura named pipe

Il server pipe specifica le modalità di accesso, sovrapposizione e write-through della pipe nel *parametro dwOpenMode* della [**funzione CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) I client pipe possono specificare queste modalità aperte per i relativi handle di pipe usando la [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

## <a name="access-mode"></a>Modalità di accesso

L'impostazione della modalità di accesso alla pipe equivale a specificare l'accesso in lettura o scrittura associato agli handle del server pipe. La tabella seguente illustra il diritto di accesso generico equivalente per ogni modalità di accesso che è possibile specificare con [**CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)



| Modalità di accesso            | Diritto di accesso generico equivalente |
|------------------------|---------------------------------|
| ACCESSO \_ ALLA PIPE IN \_ INGRESSO  | GENERIC \_ READ                   |
| ACCESSO ALLA PIPE \_ IN \_ USCITA | GENERIC \_ WRITE                  |
| PIPE \_ ACCESS \_ DUPLEX   | GENERIC \_ READ \| GENERIC \_ WRITE |



 

Se il server pipe crea una pipe con PIPE ACCESS INBOUND, la pipe è di sola lettura per il server pipe e di sola \_ scrittura per il client \_ pipe. Se il server pipe crea una pipe con PIPE ACCESS OUTBOUND, la pipe è di sola scrittura per il server pipe e di \_ sola lettura per il client \_ pipe. Una pipe creata con PIPE \_ ACCESS DUPLEX è di lettura/scrittura sia per il \_ server pipe che per il client pipe.

I client pipe che usano [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per connettersi a un named pipe devono specificare un diritto di accesso nel *parametro dwDesiredAccess* compatibile con la modalità di accesso specificata dal server pipe. Ad esempio, un client deve specificare l'accesso GENERIC READ per aprire un handle per una pipe creata dal \_ server pipe con PIPE ACCESS \_ \_ OUTBOUND. Le modalità di accesso devono essere le stesse per tutte le istanze di una pipe.

Per leggere gli attributi della pipe, ad esempio la modalità di lettura o di blocco, l'handle di pipe deve disporre del diritto di accesso FILE READ ATTRIBUTES. Per scrivere gli attributi della pipe, l'handle di pipe deve disporre del diritto di accesso \_ \_ FILE WRITE \_ \_ ATTRIBUTES. Questi diritti di accesso possono essere combinati con il diritto di accesso generico appropriato per la pipe: GENERIC READ con ATTRIBUTI DI SCRITTURA FILE per una pipe di sola lettura o GENERIC WRITE con ATTRIBUTI DI LETTURA FILE per una pipe di \_ \_ sola \_ \_ \_ \_ scrittura. La limitazione dei diritti di accesso in questo modo garantisce una maggiore sicurezza per la pipe.

## <a name="overlapped-mode"></a>Modalità sovrapposta

In modalità sovrapposta, le funzioni che eseguono operazioni di lettura, scrittura e connessione di lunga durata possono restituire immediatamente un valore. In questo modo il thread può eseguire altre operazioni mentre un'operazione dispendiosa in termini di tempo viene eseguita in background. Per specificare la modalità sovrapposta, usare il flag FILE \_ FLAG \_ OVERLAPPED. Per altre informazioni, vedere [Input e output sincroni e sovrapposti.](synchronous-and-overlapped-input-and-output.md)

La [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) consente al client di pipe di impostare la modalità sovrapposta (FILE FLAG OVERLAPPED) per i relativi handle di pipe usando il \_ parametro \_ *dwFlagsAndAttributes.*

## <a name="write-through-mode"></a>Write-Through predefinita

Specificare la modalità write-through con FILE \_ FLAG \_ WRITE \_ THROUGH. Questa modalità influisce solo sulle operazioni di scrittura su pipe di tipo byte tra client pipe e server pipe in computer diversi. In modalità write-through, le funzioni che scrivono in un named pipe non restituiscono fino a quando i dati non vengono trasmessi attraverso la rete e nel buffer della pipe nel computer remoto. La modalità write-through è utile per le applicazioni che richiedono la sincronizzazione per ogni operazione di scrittura.

Se la modalità write-through non è abilitata, il sistema migliora l'efficienza delle operazioni di rete tramite il buffering dei dati fino a quando non si accumula un numero minimo di byte o fino a quando non è trascorso un periodo di tempo massimo. Il buffering consente al sistema di combinare più operazioni di scrittura in una singola trasmissione di rete. Ciò significa che un'operazione di scrittura può essere completata correttamente dopo che il sistema inserisce i dati nel buffer in uscita, ma prima che il sistema li trasm in rete.

La [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) consente al client pipe di impostare la modalità write-through (FILE FLAG WRITE THROUGH) per i relativi handle di pipe usando il \_ parametro \_ \_ *dwFlagsAndAttributes.* La modalità write-through di un handle di pipe non può essere modificata dopo la creazione dell'handle di pipe. La modalità write-through può essere diversa per gli handle del server e del client per la stessa istanza della pipe.

Un client pipe può usare la funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per controllare il numero di byte e il periodo di timeout prima della trasmissione per una pipe in cui la modalità write-through è disabilitata. Per una pipe di sola lettura, l'handle di pipe deve essere aperto con i diritti di accesso GENERIC \_ READ e FILE WRITE \_ \_ ATTRIBUTES.

 

 
