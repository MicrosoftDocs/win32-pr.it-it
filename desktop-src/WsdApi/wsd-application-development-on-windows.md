---
description: Informazioni su come usare l'API WSD (Microsoft Web Services on Devices) per implementare dispositivi e servizi controllati dal client e host dei dispositivi conformi a DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Sviluppo di applicazioni WSD in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405784"
---
# <a name="wsd-application-development-on-windows"></a>Sviluppo di applicazioni WSD in Windows

L'API Servizi Web Microsoft nei dispositivi (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e di host di dispositivi conformi al profilo dispositivi per i servizi [Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI può essere usato per lo sviluppo di implementazioni client e server (dispositivo).

Molto spesso il codice WSDAPI per queste applicazioni viene generato [usando WsdCodeGen.](web-services-for-devices-code-generator.md) Alcune funzioni e metodi WSDAPI devono essere chiamati solo dal codice generato. La documentazione di riferimento dell'API indica quando una funzione o un metodo deve essere usato o implementato solo dal codice generato.

Il Windows SDK include alcuni file WSDL di esempio, file di configurazione WsdCodeGen e codice generato. Per altre informazioni, vedere [Esempi di WSDAPI.](wsdapi-samples.md)

Se si desidera enumerare i dispositivi usando il protocollo WSD ed eseguire query sui metadati dei dispositivi WSD, è possibile usare l'API [di individuazione delle](/previous-versions/windows/desktop/fundisc/fd-portal) funzioni.

Se si vuole implementare un dispositivo WSD che non esegue Windows, vedere [Sviluppo di dispositivi WSD.](wsd-device-development.md)
