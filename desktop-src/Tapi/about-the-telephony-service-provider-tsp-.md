---
description: Un provider di servizi di telefonia TAPI (TSP) è una libreria a collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni di servizio esportate.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Informazioni sul provider di servizi di telefonia (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab5f7d1d1631c1146bfb06223fa722bf27daa5cd6ec8e3f4f4b83d1d23c5554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949268"
---
# <a name="about-the-telephony-service-provider-tsp"></a>Informazioni sul provider di servizi di telefonia (TSP)

\[I TSP H323 e IPConf non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Un provider di servizi di telefonia TAPI (TSP) è una libreria a collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni di servizio esportate. Un'applicazione TAPI usa comandi standardizzati, TAPI passa al provider di servizi di telefonia e il TSP gestisce i comandi specifici che devono essere s scambiati con il dispositivo.

Le sezioni seguenti descrivono brevemente i TSP forniti con Microsoft Windows:

-   [H323 TSP](h323-tsp.md)
-   [Provider di servizi di configurazione IPConf](ipconf-tsp.md)
-   [Provider di servizi di configurazione del driver di dispositivo in modalità kernel](kernel-mode-device-driver-tsp.md)
-   [NDIS Proxy TSP](ndis-proxy-tsp.md)
-   [TSP remoto](remote-tsp.md)
-   [Provider di servizi di servizi di terze parti](third-party-tsp.md)
-   [Unimodem TSP](unimodem-tsp.md)

Per informazioni dettagliate, vedere il Resource Kit per il sistema operativo di destinazione. I TSP di terze parti per i dispositivi di comunicazione specializzati vengono in genere forniti dal produttore e vengono installati con il dispositivo.

Gli argomenti seguenti descrivono come creare un TSP che funzionerà correttamente all'interno dell'ambiente di telefonia Microsoft e come creare una coppia TSP/MSP:

-   [TSPI (Telefonia Service Provider Interface)](telephony-service-provider-interface-tspi-.md)
-   [Informazioni di riferimento su TSPI](tspi-reference.md)
-   [Provider di servizi multimediali](./media-service-providers-start-page.md)

> [!Note]  
> Un TSP è una DLL creata dall'utente. Se si sta creando un TSP per una piattaforma Windows a 64 bit, è necessario compilarlo come DLL o DLL a 64 bit.

 

 

 
