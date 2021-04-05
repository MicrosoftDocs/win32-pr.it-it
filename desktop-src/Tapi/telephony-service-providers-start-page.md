---
description: Un provider di servizi di telefonia (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884789"
---
# <a name="telephony-service-providers"></a>Provider di servizi di telefonia

## <a name="purpose"></a>Scopo

Un provider di servizi di telefonia (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate. Un'applicazione TAPI utilizza comandi standardizzati, TAPI passa informazioni al provider del servizio di telefonia e il TSP gestisce i comandi specifici che devono essere scambiati con il dispositivo.

Un TSP deve essere conforme all'interfaccia del provider di servizi di telefonia (TSPI) per fungere da provider di servizi nell'ambiente di telefonia Microsoft. TSPI definisce le funzioni esterne esposte da un provider di servizi di telefonia fornito con apparecchiature per le comunicazioni.

## <a name="developer-audience"></a>Sviluppatori

È possibile scrivere applicazioni abilitate per TAPI in molti linguaggi, tra cui Java, Visual Basic e C/C++. L'esperienza di sviluppo precedente con le telecomunicazioni o altre applicazioni di telefonia è utile ma non necessaria.

## <a name="run-time-requirements"></a>Requisiti di runtime

TSPI consente lo sviluppo di TSPs per tutte le versioni di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                | Descrizione                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Overview](about-the-telephony-service-provider-tsp-.md)<br/> | Informazioni generali sull'architettura e i componenti di TSPI.<br/> |
| [Riferimento](tspi-reference.md)<br/>                           | Documentazione per le interfacce TSPI.<br/>                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica della telefonia Microsoft](./microsoft-telephony-overview.md)
</dt> <dt>

[Provider di servizi multimediali](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2,2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3,1](./tapi-3-1-start-page.md)
</dt> </dl>

 

