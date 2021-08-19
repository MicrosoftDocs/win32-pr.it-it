---
description: Requisiti generali per lo sviluppo di applicazioni
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisiti generali per lo sviluppo di applicazioni (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad1ed207774494102f673bd7fb4f92acbdcb4629542d238613637d9509336c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430880"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Requisiti generali per lo sviluppo di applicazioni (API WPD)

Per creare un Windows di dispositivi portatili, è necessario che nel computer sia installato [Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads) Le intestazioni e le librerie necessarie vengono visualizzate nell'elenco seguente.

-   PortableDeviceGuids.lib
-   PortableDevice.h
-   PortableDeviceTypes.h
-   PortableDeviceApi.h
-   Qualsiasi altra libreria e intestazione richiesta dall'applicazione per utilizzare o eseguire il rendering di file multimediali.

Se l'applicazione supporta le nuove interfacce di Servizi di dispositivo, includerà anche uno o più dei file di intestazione seguenti.

-   AnchorSyncDeviceService.h
-   BridgeDeviceService.h
-   CalendarDeviceService.h
-   ContactDeviceService.h
-   DeviceServices.h
-   FullEnumSyncDeviceService.h
-   HintsDeviceService.h
-   MessageDeviceService.h
-   MetadataDeviceService.h
-   NotesDeviceService.h
-   RingtoneDeviceService.h
-   StatusDeviceService.h
-   SyncDeviceService.h
-   TaskDeviceService.h

Tra i file nell'elenco precedente, BridgeDeviceService.h e DeviceService.h sono necessari per quasi tutte le applicazioni che supportano Servizi di dispositivo. Gli altri file definiscono tipi diversi di servizi del dispositivo e vengono inclusi in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Dispositivi portatili**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
