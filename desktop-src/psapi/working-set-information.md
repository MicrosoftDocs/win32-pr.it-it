---
title: Informazioni sul working set
description: La working set di un processo è la quantità di memoria fisicamente mappata al relativo contesto di processo. PSAPI consente di creare snapshot del working set o di monitorare il working set.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56e1e4dc0a68a9d4507a94ad1f5356432f8488a
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549863"
---
# <a name="working-set-information"></a>Informazioni sul working set

La working set di un processo è la quantità di memoria fisicamente mappata al relativo contesto di processo. PSAPI consente di creare snapshot del working set o di monitorare il working set.

La [**funzione QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) o [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) riempie un buffer con uno snapshot delle informazioni per ogni pagina nel working set corrente del processo specificato. La funzione segnala solo le pagine fisicamente presenti nel momento esatto in cui viene chiamata.

È possibile usare working set monitoraggio per scoprire la quantità di RAM aggiuntiva richiesta da una determinata operazione, ad esempio il salvataggio di un file. Per iniziare a monitorare il working set, chiamare la [**funzione InitializeProcessForWsWatch.**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) Non tutti i processi consentono di leggere le working set, quindi assicurarsi che la funzione restituisca un valore diverso da zero prima di continuare. Chiamare quindi la [**funzione GetWsChanges.**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) Questa funzione segnala solo le pagine caricate in memoria dall'inizio del monitoraggio working set. La funzione restituisce i dati in una matrice di strutture [**PSAPI \_ WS \_ WATCH \_ INFORMATION,**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) una struttura per ogni nuova pagina aggiunta al working set del processo. La struttura indica quali pagine sono in memoria e cosa le ha causate dal sistema.

La [**funzione EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) accetta un handle di processo. Rimuove il maggior numero possibile di pagine dal processo working set. Questa operazione è utile principalmente per il test e l'ottimizzazione. Si noti che [**la funzione SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) esegue la stessa cosa se si passa -1 per le dimensioni minime e massime.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Working Set](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 