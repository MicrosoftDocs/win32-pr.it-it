---
description: Le funzioni seguenti vengono usate dai provider di tempo.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funzioni del provider di tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c0647574aaa807788e9cf510ce9293460c0394bcdaa794e243009ad6710bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884816"
---
# <a name="time-provider-functions"></a>Funzioni del provider di tempo

Le funzioni seguenti vengono usate dai provider di tempo.



| Funzione                                                               | Descrizione                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Notifica al sistema che sono disponibili nuovi esempi.                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Recupera le informazioni sullo stato dell'ora di sistema.                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Registra un evento del provider di tempo nel registro eventi.                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Imposta le informazioni sullo stato del provider di tempo.                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Libera una [**struttura SetProviderStatusInfo.**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo)                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Funzione di callback chiamata dal gestore del provider di tempo per arrestare il provider di tempo.        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Funzione di callback chiamata dal gestore del provider di tempo per inviare comandi al provider di tempo. |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Funzione di callback chiamata dal gestore del provider di tempo quando viene caricata la DLL del provider di tempo.  |



 

 

 



