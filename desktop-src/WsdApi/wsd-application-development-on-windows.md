---
description: Informazioni su come usare l'API WSD (Web Services on Devices) Microsoft per implementare dispositivi e servizi controllati dal client e host dei dispositivi conformi a DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Sviluppo di applicazioni WSD in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d02810f55cc7ae450323543d7a0ee88f055b247fed589057e7d77710f4f86d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639351"
---
# <a name="wsd-application-development-on-windows"></a>Sviluppo di applicazioni WSD in Windows

L'API Servizi Web microsoft nei dispositivi (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e di host di dispositivi conformi al profilo dispositivi per i servizi [Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI può essere usato per lo sviluppo di implementazioni client e server (dispositivo).

Molto spesso il codice WSDAPI per queste applicazioni viene generato [usando WsdCodeGen.](web-services-for-devices-code-generator.md) Alcune funzioni e metodi WSDAPI devono essere chiamati solo dal codice generato. La documentazione di riferimento dell'API indica quando una funzione o un metodo deve essere usato o implementato solo dal codice generato.

L Windows SDK include alcuni file WSDL di esempio, file di configurazione WsdCodeGen e codice generato. Per altre informazioni, vedere [Esempi di WSDAPI.](wsdapi-samples.md)

Se si vuole enumerare i dispositivi usando il protocollo WSD ed eseguire query sui metadati dei dispositivi WSD, è possibile usare l'API [di individuazione delle](/previous-versions/windows/desktop/fundisc/fd-portal) funzioni.

Se si vuole implementare un dispositivo WSD che non esegue Windows, vedere Sviluppo di dispositivi [WSD.](wsd-device-development.md)
