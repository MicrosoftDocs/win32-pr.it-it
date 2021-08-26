---
title: Pacchetto di gestione della memoria RpcSs
description: La coppia allocatore/deallocatore predefinita usata dagli stub e dalla fase di esecuzione quando si alloca memoria per conto dell'applicazione è midl \_ user \_ allocate/midl \_ user \_ free.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93648b56ed47eb98a83b27a39b606fa2a51de9bf5791ad1b732e7169ef5dfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018181"
---
# <a name="rpcss-memory-management-package"></a>Pacchetto di gestione della memoria RpcSs

La coppia allocatore/deallocatore predefinita usata dagli stub e dalla fase di esecuzione durante l'allocazione della memoria per conto dell'applicazione è **midl \_ user \_ allocate** / **midl \_ user \_ free**. Tuttavia, è possibile scegliere il pacchetto RpcSs anziché il valore predefinito usando l'attributo ACF **\[ enable \_ \] allocare**. Il pacchetto RpcSs è costituito da funzioni RPC che iniziano con il prefisso **RpcSs** o **RpcSm**. Il pacchetto RpcSs non è consigliato per Windows applicazioni.

> [!Note]  
> Il pacchetto di gestione della memoria Rpcss è obsoleto. È consigliabile usare [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1) al suo posto.

 

In **modalità /osf** il pacchetto RpcSs viene abilitato automaticamente per gli stub generati da MIDL quando vengono usati puntatori completi, quando gli argomenti richiedono l'allocazione di memoria o come risultato dell'uso dell'attributo **\[ enable \_ allocate. \]** Nella modalità predefinita (estesa Microsoft) il pacchetto RpcSs è abilitato solo quando viene usato l'attributo **\[ enable \_ \] allocate.** **\[ L'attributo enable \_ allocate \]** abilita l'ambiente RpcSs dagli stub sul lato server. Il lato client viene avvisato della possibilità che il pacchetto RpcSs possa essere abilitato. In **modalità /osf,** il lato client non è interessato.

Quando il pacchetto RpcSs è abilitato, l'allocazione della memoria sul lato server viene eseguita con la coppia privata di allocatore di gestione della memoria RpcSs e deallocatore. È possibile allocare memoria usando lo stesso meccanismo chiamando [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (o [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)). Al ritorno dallo stub del server, tutta la memoria allocata dal pacchetto RpcSs viene liberata automaticamente. L'esempio seguente illustra come abilitare il pacchetto RpcSs:

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

L'applicazione può liberare memoria in modo esplicito richiamando la [**funzione RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) [**o RpcSmFree.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) Si noti che queste funzioni non liberano effettivamente memoria. Lo contrassegnano per l'eliminazione. La libreria RPC rilascia la memoria quando il programma chiama [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) o [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).

È anche possibile abilitare l'ambiente di gestione della memoria per l'applicazione chiamando la routine [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) ed è possibile disabilitarla chiamando la routine [**RpcSmDisableAllocate.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) Dopo l'allocazione, il codice dell'applicazione può allocare e deallocare la memoria chiamando funzioni dal pacchetto RpcSs.

 

 