---
description: Requisiti generali per lo sviluppo di applicazioni
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisiti generali per lo sviluppo di applicazioni (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232308"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Requisiti generali per lo sviluppo di applicazioni (API WPD)

Per creare un'applicazione per dispositivi portatili Windows, è necessario che nel computer sia installato [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) . Le intestazioni e le librerie richieste sono incluse nell'elenco seguente.

-   PortableDeviceGuids. lib
-   PortableDevice. h
-   PortableDeviceTypes. h
-   PortableDeviceApi. h
-   Qualsiasi altra libreria e intestazione richiesta richiesta dall'applicazione per utilizzare o eseguire il rendering dei file multimediali.

Se l'applicazione supporta le nuove interfacce di servizi per dispositivi, includerà anche uno o più dei file di intestazione seguenti.

-   AnchorSyncDeviceService. h
-   BridgeDeviceService. h
-   CalendarDeviceService. h
-   ContactDeviceService. h
-   DeviceServices. h
-   FullEnumSyncDeviceService. h
-   HintsDeviceService. h
-   MessageDeviceService. h
-   MetadataDeviceService. h
-   NotesDeviceService. h
-   RingtoneDeviceService. h
-   StatusDeviceService. h
-   SyncDeviceService. h
-   TaskDeviceService. h

Dei file nell'elenco precedente, BridgeDeviceService. h e DeviceService. h sono necessari per quasi tutte le applicazioni che supportano i servizi dispositivo; gli altri file definiscono tipi diversi di servizi per dispositivi e verrebbero inclusi nel modo appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Dispositivi portatili Windows**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
