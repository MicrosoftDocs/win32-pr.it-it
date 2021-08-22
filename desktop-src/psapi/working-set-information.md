---
title: Informazioni sul working set
description: La working set di un processo è la quantità di memoria mappata fisicamente al relativo contesto di processo. PSAPI consente di creare snapshot del working set o di monitorare il working set.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6003886d50cb47b128bfce92cba4c28950ee078dbe13499d8909676d938aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032979"
---
# <a name="working-set-information"></a>Informazioni sul working set

La working set di un processo è la quantità di memoria mappata fisicamente al relativo contesto di processo. PSAPI consente di creare snapshot del working set o di monitorare il working set.

La [**funzione QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) o [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) riempie un buffer con uno snapshot delle informazioni per ogni pagina nel working set corrente del processo specificato. La funzione segnala solo le pagine fisicamente presenti nel momento esatto in cui viene chiamata.

È possibile usare working set monitoraggio per scoprire la quantità di RAM aggiuntiva richiesta da una determinata operazione, ad esempio il salvataggio di un file. Per iniziare a monitorare working set, chiamare la [**funzione InitializeProcessForWsWatch.**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) Non tutti i processi consentono di leggere le informazioni working set, quindi assicurarsi che la funzione restituisca un valore diverso da zero prima di continuare. Chiamare quindi la [**funzione GetWsChanges.**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) Questa funzione segnala solo le pagine caricate in memoria dall'inizio del monitoraggio del working set. La funzione restituisce i dati in una matrice di strutture [**PSAPI \_ WS \_ WATCH \_ INFORMATION,**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) una struttura per ogni nuova pagina aggiunta al working set del processo. La struttura indica quali pagine sono in memoria e cosa le ha causate dal sistema.

La [**funzione EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) accetta un handle di processo. Rimuove il maggior numero possibile di pagine dal processo working set. Questa operazione è utile principalmente per il test e l'ottimizzazione. Si noti che [**la funzione SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) esegue la stessa cosa se si passa -1 per le dimensioni minima e massima.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Working Set](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 