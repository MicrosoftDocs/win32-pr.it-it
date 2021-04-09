---
description: Il server pipe specifica le modalità di accesso alla pipe, sovrapposizione e scrittura nel parametro dwOpenMode della funzione CreateNamedPipe. I client pipe possono specificare queste modalità aperte per i rispettivi handle di pipe utilizzando la funzione CreateFile.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Modalità di apertura named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f51d41ea98a47a269634b06ccdad869bd649fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968426"
---
# <a name="named-pipe-open-modes"></a>Modalità di apertura named pipe

Il server pipe specifica le modalità di accesso alla pipe, sovrapposizione e scrittura nel parametro *dwOpenMode* della funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . I client pipe possono specificare queste modalità aperte per i rispettivi handle di pipe utilizzando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="access-mode"></a>Modalità di accesso

L'impostazione della modalità di accesso alla pipe equivale a specificare l'accesso in lettura o scrittura associato agli handle del server pipe. La tabella seguente illustra il diritto di accesso generico equivalente per ogni modalità di accesso che è possibile specificare con [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).



| Modalità di accesso            | Diritto di accesso generico equivalente |
|------------------------|---------------------------------|
| accesso PIPE in \_ \_ ingresso  | lettura GENERIca \_                   |
| accesso PIPE in \_ \_ uscita | scrittura GENERIca \_                  |
| accesso tramite PIPE \_ \_ duplex   | \_ \| scrittura generica di lettura generica \_ |



 

Se il server pipe crea una pipe con accesso PIPE in \_ \_ ingresso, la pipe è di sola lettura per il server pipe e per il client pipe. Se il server pipe crea una pipe con accesso tramite PIPE in \_ \_ uscita, la pipe è di sola scrittura per il server pipe e di sola lettura per il client pipe. Una pipe creata con accesso tramite PIPE \_ \_ duplex è in lettura/scrittura sia per il server pipe che per il client pipe.

I client pipe che usano [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per connettersi a un named pipe devono specificare un diritto di accesso nel parametro *dwDesiredAccess* compatibile con la modalità di accesso specificata dal server pipe. Un client, ad esempio, deve specificare \_ l'accesso in lettura generico per aprire un handle per una pipe creata dal server pipe con accesso tramite pipe in \_ \_ uscita. Le modalità di accesso devono essere le stesse per tutte le istanze di una pipe.

Per leggere gli attributi della pipe, ad esempio la modalità di lettura o di blocco, l'handle della pipe deve avere il \_ \_ diritto di accesso per gli attributi di lettura del file. per scrivere gli attributi della pipe, l'handle della pipe deve avere il diritto di accesso per gli \_ attributi di scrittura file \_ Questi diritti di accesso possono essere combinati con il diritto di accesso generico appropriato per la pipe: \_ lettura generica \_ con \_ attributi di scrittura di file per una pipe di sola lettura o scrittura generica \_ con \_ attributi di lettura del file \_ per una pipe di sola scrittura. La restrizione dei diritti di accesso in questo modo garantisce una migliore sicurezza per la pipe.

## <a name="overlapped-mode"></a>Modalità sovrapposta

In modalità sovrapposta, le funzioni che eseguono operazioni di lettura, scrittura e connessione lunghe possono restituire immediatamente un risultato. Ciò consente al thread di eseguire altre operazioni mentre è in esecuzione un'operazione che richiede molto tempo. Per specificare la modalità sovrapposta, usare \_ il \_ flag file sovrapposto. Per altre informazioni, vedere [input e output sincroni e sovrapposti](synchronous-and-overlapped-input-and-output.md).

La funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) consente al client pipe di impostare la modalità sovrapposta ( \_ flag file \_ sovrapposto) per gli handle di pipe utilizzando il parametro *dwFlagsAndAttributes* .

## <a name="write-through-mode"></a>Modalità Write-Through

Consente di specificare la modalità Write-through con la scrittura del flag di FILE \_ \_ \_ . Questa modalità influiscono solo sulle operazioni di scrittura in pipe di tipo byte tra client pipe e server pipe in computer diversi. In modalità Write-through le funzioni che scrivono in un named pipe non vengono restituite fino a quando i dati non vengono trasmessi attraverso la rete e nel buffer della pipe nel computer remoto. La modalità Write-through è utile per le applicazioni che richiedono la sincronizzazione per ogni operazione di scrittura.

Se la modalità Write-through non è abilitata, il sistema ottimizza l'efficienza delle operazioni di rete mediante il buffering dei dati fino a quando non viene accumulato un numero minimo di byte o fino a quando non è trascorso un periodo di tempo massimo. Il buffering consente al sistema di combinare più operazioni di scrittura in una singola trasmissione di rete. Ciò significa che un'operazione di scrittura può essere completata correttamente dopo che il sistema inserisce i dati nel buffer in uscita, ma prima che il sistema lo trasmetta attraverso la rete.

La funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) consente al client pipe di impostare la modalità Write-through ( \_ scrittura del flag di file \_ \_ tramite) per gli handle di pipe utilizzando il parametro *dwFlagsAndAttributes* . La modalità Write-through di un handle di pipe non può essere modificata dopo la creazione dell'handle della pipe. La modalità Write-through può essere diversa per gli handle server e client per la stessa istanza di pipe.

Un client pipe può usare la funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per controllare il numero di byte e il periodo di timeout prima della trasmissione per una pipe in cui la modalità Write-through è disabilitata. Per una pipe di sola lettura, è necessario aprire l'handle della pipe con i \_ diritti di accesso di lettura e scrittura di file generici \_ \_ .

 

 
