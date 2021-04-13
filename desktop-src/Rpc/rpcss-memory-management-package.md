---
title: Pacchetto di gestione della memoria RpcSs
description: La coppia allocatore/deallocatore predefinita utilizzata dagli Stub e dalla fase di esecuzione durante l'allocazione della memoria per conto dell'applicazione è la versione \_ \_ gratuita dell'utente allocatore/MIDL dell'utente MIDL \_ \_ .
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473899"
---
# <a name="rpcss-memory-management-package"></a>Pacchetto di gestione della memoria RpcSs

La coppia allocatore/deallocatore predefinita utilizzata dagli Stub e dalla fase di esecuzione durante l'allocazione della memoria per conto dell'applicazione è l' **utente MIDL che \_ \_ alloca** l' / **\_ utente MIDL \_ gratuitamente**. Tuttavia, è possibile scegliere il pacchetto RpcSs anziché quello predefinito utilizzando l'attributo ACF **\[ enable \_ allocate \]**. Il pacchetto RpcSs è costituito da funzioni RPC che iniziano con il prefisso **RPCSS** o **RpcSm**. Il pacchetto RpcSs non è consigliato per le applicazioni Windows.

> [!Note]  
> Il pacchetto di gestione della memoria RPCSS è obsoleto. È consigliabile usare al suo posto l'utente [**MIDL \_ \_ allocato**](/windows/desktop/Midl/midl-user-allocate-1) e gli [**utenti di MIDL \_ \_ Free**](/windows/desktop/Midl/midl-user-free-1) .

 

In modalità **/OSF** , il pacchetto RPCSS è abilitato automaticamente per gli stub generati da MIDL quando vengono utilizzati i puntatori completi, quando gli argomenti richiedono l'allocazione di memoria o come risultato dell'utilizzo dell'attributo **\[ enable \_ allocate \]** . Nella modalità predefinita (Microsoft Extended) il pacchetto RpcSs viene abilitato solo quando si usa l'attributo **\[ enable \_ allocate \]** . L'attributo **\[ enable \_ allocate \]** Abilita l'ambiente RPCSS dagli Stub lato server. Il lato client viene avvisato in modo che sia possibile abilitare il pacchetto RpcSs. In modalità **/OSF** , il lato client non è interessato.

Quando il pacchetto RpcSs è abilitato, l'allocazione della memoria sul lato server viene eseguita con l'allocatore di gestione della memoria di RpcSs privato e la coppia di deallocatori. È possibile allocare memoria utilizzando lo stesso meccanismo chiamando [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (o [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)). Al ritorno dallo stub del server, tutta la memoria allocata dal pacchetto RpcSs viene liberata automaticamente. Nell'esempio seguente viene illustrato come abilitare il pacchetto RpcSs:

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

L'applicazione può liberare la memoria in modo esplicito richiamando la funzione [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) o [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) . Si noti che queste funzioni non liberano effettivamente la memoria. Il contrassegno viene contrassegnato per l'eliminazione. La libreria RPC rilascia la memoria quando il programma chiama [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) o [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).

È anche possibile abilitare l'ambiente di gestione della memoria per l'applicazione chiamando la routine [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (ed è possibile disabilitarla chiamando la routine [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ). Una volta abilitata, il codice dell'applicazione può allocare e deallocare memoria chiamando funzioni dal pacchetto RpcSs.

 

 