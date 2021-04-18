---
description: Le funzioni seguenti vengono usate dai provider di servizi temporali.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funzioni del provider Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316051"
---
# <a name="time-provider-functions"></a>Funzioni del provider Time

Le funzioni seguenti vengono usate dai provider di servizi temporali.



| Funzione                                                               | Descrizione                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Notifica al sistema che sono disponibili nuovi esempi.                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Recupera le informazioni sullo stato dell'ora di sistema.                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Registra un evento del provider di tempo nel registro eventi.                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Imposta le informazioni sullo stato del provider di tempo.                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Libera una struttura [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Funzione di callback chiamata da gestione provider del tempo per arrestare il provider di tempo.        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Funzione di callback chiamata dal gestore del provider di servizi temporali per inviare comandi al provider di servizi temporali. |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Funzione di callback chiamata dal gestore del provider di servizi temporali quando viene caricata la DLL del provider di servizi temporali.  |



 

 

 



