---
title: Regole di gestione della memoria
description: Regole di gestione della memoria
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e7ad2483b794ec5c2e9c325bca8e469ff4ae0b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118550"
---
# <a name="memory-management-rules"></a>Regole di gestione della memoria

La durata dei puntatori alle interfacce viene sempre gestita tramite i metodi [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su ogni interfaccia com. Per ulteriori informazioni, vedere [regole per la gestione dei conteggi dei riferimenti](rules-for-managing-reference-counts.md).

Per tutti gli altri parametri, è importante rispettare determinate regole per la gestione della memoria. Le regole seguenti si applicano a tutti i parametri di Interface methodsâ ", incluso il valore restituito valueâ €", che non vengono passati per valore:

-   I parametri in devono essere allocati e liberati dal chiamante.
-   I parametri out devono essere allocati da uno chiamato; vengono liberati dal chiamante utilizzando l'allocatore di memoria delle attività COM standard. Per ulteriori informazioni, vedere [l'allocatore di memoria OLE](the-ole-memory-allocator.md) .
-   I parametri in/out vengono inizialmente allocati dal chiamante e quindi liberati e riallocati da quello denominato, se necessario. Come è vero per i parametri out, il chiamante è responsabile della liberazione del valore finale restituito. È necessario usare l'allocatore di memoria COM standard.

Negli ultimi due casi, in cui un frammento di codice consente di allocare la memoria e una parte diversa del codice la libera, l'uso dell'allocatore COM garantisce che le due parti di codice utilizzino gli stessi metodi di allocazione.

Un'altra area che richiede particolare attenzione è il trattamento di parametri out e out in condizioni di errore. Se una funzione restituisce un codice di errore, il chiamante non ha in genere alcun modo per pulire i parametri out o out. Ciò comporta le regole aggiuntive seguenti:

-   In caso di condizione di errore, i parametri devono essere sempre impostati in modo affidabile su un valore che verrà pulito senza alcuna azione da parte del chiamante.
-   Tutti i parametri del puntatore out devono essere impostati in modo esplicito su **null**. Questi vengono in genere passati in un parametro puntatore a puntatore, ma possono anche essere passati come membri di una struttura allocata dal chiamante e il codice chiamato riempie. Il modo più semplice per assicurarsi che sia (in parte) impostare questi valori su **null** nella voce di funzione. Questa regola è importante perché promuove l'interoperabilità di applicazioni più affidabili.
-   In condizioni di errore, tutti i parametri in uscita devono essere lasciati da solo dal codice chiamato (rimanendo così in corrispondenza del valore a cui sono stati inizializzati dal chiamante) o essere impostati in modo esplicito, come nel caso di errore del parametro out.

Tenere presente che le convenzioni di gestione della memoria per le applicazioni COM si applicano solo tra le interfacce pubbliche e APIsâ "non è necessario che l'allocazione di memoria strettamente interna a un'applicazione COM venga eseguita usando questi meccanismi.

COM utilizza internamente RPC (Remote Procedure Call) per la comunicazione tra client e server. Per ulteriori informazioni sulla gestione della memoria negli stub del server RPC, vedere l'argomento relativo alla [gestione della memoria dei stub server](../rpc/server-stub-memory-management.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dell'allocazione di memoria](managing-memory-allocation.md)
</dt> </dl>

 

 