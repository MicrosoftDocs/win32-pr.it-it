---
title: Informazioni sul working set
description: Il working set di un processo è la quantità di memoria mappata fisicamente al contesto del processo. PSAPI consente di creare snapshot del working set o di monitorare l'working set.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3942796ec1150dee411d6074b13f9ee2be4a22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118270"
---
# <a name="working-set-information"></a>Informazioni sul working set

Il working set di un processo è la quantità di memoria mappata fisicamente al contesto del processo. PSAPI consente di creare snapshot del working set o di monitorare l'working set.

La funzione [**QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) o [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) inserisce un buffer con uno snapshot delle informazioni per ogni pagina della working set corrente del processo specificato. La funzione segnala solo le pagine fisicamente presenti nel momento esatto in cui viene chiamato.

È possibile usare working set monitoraggio per determinare la quantità di RAM aggiuntiva necessaria per un'operazione specifica, ad esempio il salvataggio di un file. Per iniziare a monitorare il working set, chiamare la funzione [**InitializeProcessForWsWatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) . Non tutti i processi consentono di leggere le informazioni di working set, quindi assicurarsi che la funzione restituisca un valore diverso da zero prima di continuare. Chiamare quindi la funzione [**GetWsChanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) . Questa funzione segnala solo le pagine che sono state caricate in memoria dall'inizio del monitoraggio del working set. La funzione restituisce i dati in una matrice di strutture di [**\_ informazioni di \_ controllo \_ PSAPI WS**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) , una struttura per ogni nuova pagina aggiunta all'working set del processo. La struttura indica le pagine che si trovano in memoria e il modo in cui il sistema li ha sottopaginati.

La funzione [**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) accetta un handle di processo. Rimuove il maggior numero possibile di pagine dal processo working set. Questa operazione è utile principalmente per i test e l'ottimizzazione. Si noti che la funzione [**SetProcessWorkingSetSize**](/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize) esegue la stessa operazione se si passa il valore-1 per le dimensioni minime e massime.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Working Set](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 