---
description: Il sistema trasmette un messaggio a tutte le applicazioni e a tutti i driver installabili ogni volta che si verifica un evento di risparmio energia.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7997f6c9bed6b4d46068c9974f4ff3571a9617ba2bf09adc6b98bb33facb3d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032691"
---
# <a name="wm_powerbroadcast-messages"></a>Messaggi \_ WM POWERBROADCAST

Il sistema trasmette un messaggio a tutte le applicazioni e a tutti i driver installabili ogni volta che si verifica un evento di risparmio energia. Il sistema trasmette questi eventi tramite il [**messaggio WM \_ POWERBROADCAST,**](wm-powerbroadcast.md) impostando il *parametro wParam* sull'evento di risparmio energia appropriato. Ad esempio, [l'evento PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica una modifica dello stato di alimentazione del sistema. È necessario assicurarsi che l'applicazione risponda correttamente al **messaggio WM \_ POWERBROADCAST.**

Il sistema trasmette un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) immediatamente prima della sospensione dell'operazione. In questo modo le applicazioni e i driver hanno un'ultima possibilità di prepararsi per l'evento. In molti casi, il sistema trasmette questi messaggi senza richiedere l'autorizzazione a tale scopo. Ciò si verifica, ad esempio, se un'applicazione forza la sospensione con la [**funzione SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

Il sistema trasmette l'evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) o [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) quando l'operazione di sistema è stata ripristinata. Se un'applicazione ha ricevuto un evento [ \_ PBT APMSUSPEND](pbt-apmsuspend.md) prima della sospensione del computer, riceverà l'evento PBT \_ APMRESUMESUSPEND. In caso contrario, riceverà l'evento \_ PBT APMRESUMECRITICAL.

Il sistema invia un [evento \_ POWERSETTINGCHANGE PBT](pbt-powersettingchange.md) alle applicazioni registrate per l'evento specifico usando [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification). Per altre informazioni, vedere [Registrazione per power events](registering-for-power-events.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Risparmio energia](about-power-management.md)
</dt> </dl>

 

 



