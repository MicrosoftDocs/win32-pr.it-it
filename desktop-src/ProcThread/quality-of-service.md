---
description: Quality of Service indica le prestazioni e l'efficienza dell'alimentazione di un thread, che possono influire sulla pianificazione dei thread e sulla gestione dell'alimentazione del processore.
title: QoS (Quality of Service)
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: ec4e92360d23a427d526a36a81bfdb0667c1cb6fb5f60ddcefd578c4918ba5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793465"
---
# <a name="quality-of-service"></a>QoS (Quality of Service)

La qualità del servizio (QoS) associata a un thread viene usata per indicare le prestazioni desiderate e l'efficienza dell'alimentazione. Ogni thread viene assegnato a un livello QoS. Anche se la priorità di pianificazione rimane la metrica principale in base alla quale il sistema determina il thread da pianificare successivamente, QoS può influire sulla selezione dei core e sulla gestione dell'alimentazione del processore. Nelle piattaforme con processori eterogenei, la QoS di un thread può limitare la pianificazione a un subset di processori o indicare una preferenza per una determinata classe di processori.

Gli sviluppatori possono già usare altre funzionalità per controllare quando eseguire, ad esempio quando l'utente non è presente, solo in ac/ricarica o a seconda del livello della batteria. QoS offre una funzionalità per influenzare la modalità di esecuzione. Questa funzionalità consente di migliorare l'efficienza della CPU e quindi di estendere la durata della batteria. Questo processo consente inoltre di ridurre il consumo di energia della CPU durante l'uso dell'alimentazione ca per ridurre l'output termico che può causare un rumore elevato della ventola o persino una limitazione termica.

## <a name="quality-of-service-levels"></a>Livelli di qualità del servizio

Il sistema mantiene più livelli QoS, ognuno con prestazioni differenziate ed efficienza dell'alimentazione. Windows impostazioni predefinite standard per la pianificazione e la gestione del risparmio energia del processore per ogni livello QoS. L'ottimizzazione precisa di ogni livello QoS per la gestione dell'alimentazione del processore e la pianificazione eterogenea può essere modificata tramite Windows provisioning. Per altre informazioni sull'ottimizzazione e il provisioning delle prestazioni, vedere Opzioni di risparmio energia [del processore](/windows-hardware/customize/power-settings/configure-processor-power-management-options).

| Livello QoS | Descrizione|Prestazioni e potenza | Versione |
| --- | --- | --- | --- |
| Alto | Applicazioni con finestre in primo piano e nello stato attivo o udibili e tag espliciti dei processi con [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) o thread [con SetThreadInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation) | Prestazioni elevate standard. |1709 |
| Medio | Applicazioni in finestra che possono essere visibili all'utente finale ma che non sono nello stato attivo. | Varia in base alla piattaforma, tra High e Low. | 1709 |
| Basso | Applicazioni in finestra non visibili o udibili per l'utente finale. | A batteria, seleziona la frequenza della CPU più efficiente e le pianificazioni per un core efficiente. | 1709 |
| Eco | Applicazioni che contrassegnano in modo esplicito i [processi con SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) o i thread [con SetThreadInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation). | Seleziona sempre la frequenza e le pianificazioni della CPU più efficienti in core efficienti. | Windows 11 |
| File multimediali | Thread contrassegnati in modo esplicito dal [servizio Utilità di pianificazione classi](/windows/desktop/procthread/multimedia-class-scheduler-service) multimediali per indicare il buffering batch multimediale. | Frequenza della CPU ridotta per un'elaborazione batch efficiente. | 2004 |
| Scadenza | Thread contrassegnati in modo esplicito dal [servizio Utilità di pianificazione](/windows/desktop/procthread/multimedia-class-scheduler-service) classi multimediali per indicare che i thread audio richiedono prestazioni per soddisfare le scadenze. | Prestazioni elevate per soddisfare le scadenze dei supporti. | 2004 |

## <a name="quality-of-service-classification"></a>Classificazione della qualità del servizio

La tabella seguente illustra le classificazioni QoS supportate.

| Source (Sorgente) | Descrizione |
| --- | --- |
| Base multimediale | Il [servizio Utilità di pianificazione classi multimediali](/windows/desktop/procthread/multimedia-class-scheduler-service) assegna la priorità alle risorse della CPU per gli scenari multimediali. Il servizio contrassegna thread specifici responsabili dell'elaborazione multimediale usando i livelli QoS Media e Deadline per garantire l'efficienza dell'alimentazione rispettando le scadenze delle prestazioni.  |
| API | [SetProcessInformation consente](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) agli sviluppatori di contrassegnare in modo esplicito un processo come HighQoS o EcoQoS attivando la `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` funzionalità in **ProcessPowerThrottling.**</br>[SetThreadInformation consente](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) agli sviluppatori di contrassegnare in modo esplicito un thread come HighQoS o EcoQoS attivando la funzionalità `THREAD_POWER_THROTTLING_EXECUTION_SPEED` in **ThreadPowerThrottling.**  |
| Udibile | I processi determinati per la riproduzione di audio sono HighQoS. |
| Visible | Ai processi proprietari direttamente di una finestra (o discendenti dei processi proprietari della finestra) viene assegnato un livello QoS in base alla visibilità e allo stato attivo:</br></br><table><tr><th>Stato della finestra</th><th>QoS (Quality of Service)</th></tr><tr><td>In stato attivo</td><td>Alto</td></tr><tr><td>Visible</td><td>Medio</td></tr><tr><td>Ridotta a icona o completamente occlusa</td><td>Basso</td></tr></table> |
| Euristico | Ai thread non classificati dalle origini precedenti viene assegnato automaticamente un livello QoS dal sistema. Queste euristiche includono (ma non solo) la priorità dei thread, in cui i thread in esecuzione con priorità di thread ridotta possono implicare un livello QoS inferiore. |
