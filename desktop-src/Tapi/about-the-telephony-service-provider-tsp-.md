---
description: Un provider di servizi di telefonia TAPI (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Informazioni sul provider di servizi di telefonia (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750791"
---
# <a name="about-the-telephony-service-provider-tsp"></a>Informazioni sul provider di servizi di telefonia (TSP)

\[ H323 e IPConf TSPs non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Un provider di servizi di telefonia TAPI (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate. Un'applicazione TAPI USA comandi standardizzati, TAPI passa alla formazione per il provider di servizi di telefonia e il TSP gestisce i comandi specifici che devono essere scambiati con il dispositivo.

Le sezioni seguenti descrivono brevemente le TSPs fornite con Microsoft Windows:

-   [H323 TSP](h323-tsp.md)
-   [IPConf TSP](ipconf-tsp.md)
-   [Driver di dispositivo in modalità kernel (TSP)](kernel-mode-device-driver-tsp.md)
-   [TSP proxy NDIS](ndis-proxy-tsp.md)
-   [TSP remoto](remote-tsp.md)
-   [TSP di terze parti](third-party-tsp.md)
-   [TSP Unimodem](unimodem-tsp.md)

Per informazioni dettagliate, vedere il Resource Kit per il sistema operativo di destinazione. TSPs di terze parti per i dispositivi di comunicazione specializzati verranno in genere forniti dal produttore e verranno installati con il dispositivo.

Negli argomenti seguenti viene descritto come creare un TSP che funzionerà correttamente nell'ambiente di telefonia Microsoft e come creare una coppia TSP/MSP:

-   [Interfaccia del provider di servizi di telefonia (TSPI)](telephony-service-provider-interface-tspi-.md)
-   [Riferimento a TSPI](tspi-reference.md)
-   [Provider di servizi multimediali](./media-service-providers-start-page.md)

> [!Note]  
> Un TSP è una DLL creata dall'utente. Se si sta creando un TSP per una piattaforma Windows a 64 bit, è necessario compilarlo come DLL o DLL a 64 bit.

 

 

 
