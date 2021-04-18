---
description: Il sistema trasmette un messaggio a tutte le applicazioni e i driver installabili ogni volta che si verifica un evento di risparmio energia.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: Messaggi di WM_POWERBROADCAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312004"
---
# <a name="wm_powerbroadcast-messages"></a>\_Messaggi WM POWERBROADCAST

Il sistema trasmette un messaggio a tutte le applicazioni e i driver installabili ogni volta che si verifica un evento di risparmio energia. Il sistema trasmette questi eventi tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , impostando il parametro *wParam* sull'evento di risparmio energia appropriato. Ad esempio, l'evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica una modifica dello stato di alimentazione del sistema. È necessario assicurarsi che l'applicazione risponda correttamente al messaggio **WM \_ POWERBROADCAST** .

Il sistema trasmette un evento [ \_ APMSUSPEND PBT](pbt-apmsuspend.md) immediatamente prima di sospendere l'operazione. In questo modo, le applicazioni e i driver potranno prepararsi per l'evento. In molti casi, il sistema trasmette questi messaggi senza richiedere l'autorizzazione. Ciò si verifica, ad esempio, se un'applicazione forza la sospensione con la funzione [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

Il sistema trasmette l'evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) o [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) quando l'operazione di sistema è stata ripristinata. Se un'applicazione ha ricevuto un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) prima della sospensione del computer, riceverà l' \_ evento PBT APMRESUMESUSPEND. In caso contrario, riceverà l' \_ evento PBT APMRESUMECRITICAL.

Il sistema invia un evento [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) alle applicazioni registrate per l'evento specifico usando [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification). Per ulteriori informazioni, vedere [la pagina relativa alla registrazione per gli eventi di alimentazione](registering-for-power-events.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> </dl>

 

 



