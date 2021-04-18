---
description: L'API Microsoft Web Services on Devices (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e degli host di dispositivi conformi al profilo dei dispositivi per i servizi Web (DPWS).
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Sviluppo di applicazioni WSD in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312664"
---
# <a name="wsd-application-development-on-windows"></a>Sviluppo di applicazioni WSD in Windows

L'API Microsoft Web Services on Devices (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e degli host di dispositivi conformi al [profilo dei dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI può essere usato per lo sviluppo di implementazioni di client e server (dispositivo).

Abbastanza spesso, il codice WSDAPI per queste applicazioni viene generato usando [WsdCodeGen](web-services-for-devices-code-generator.md). Alcune funzioni e metodi WSDAPI sono progettati per essere chiamati solo dal codice generato. La documentazione di riferimento dell'API indica quando una funzione o un metodo deve essere utilizzato o implementato solo dal codice generato.

Il Windows SDK include alcuni file WSDL di esempio, i file di configurazione WsdCodeGen e il codice generato. Per ulteriori informazioni, vedere [WSDAPI Samples](wsdapi-samples.md).

Se si desidera enumerare i dispositivi utilizzando il protocollo WSD ed eseguire query su metadati del dispositivo WSD, è possibile utilizzare l'API di [individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) .

Se si desidera implementare un dispositivo WSD che non esegue Windows, vedere [WSD Device Development](wsd-device-development.md).
