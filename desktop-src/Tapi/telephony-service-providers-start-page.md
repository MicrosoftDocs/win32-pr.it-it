---
description: Un provider di servizi di telefonia (TSP) è una libreria a collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni di servizio esportate.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c1e7ff98bfbc898a419e385be07ebdae56d2067061d2ac7951b8c0aff42dcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872871"
---
# <a name="telephony-service-providers"></a>Provider di servizi di telefonia

## <a name="purpose"></a>Scopo

Un provider di servizi di telefonia (TSP) è una libreria a collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni di servizio esportate. Un'applicazione TAPI usa comandi standardizzati, TAPI passa le informazioni al provider di servizi di telefonia e il provider di servizi di telefonia gestisce i comandi specifici da scambiare con il dispositivo.

Un provider di servizi di telefonia deve essere conforme all'interfaccia TSPI (Telephony Service Provider Interface) per funzionare come provider di servizi all'interno dell'ambiente Di telefonia Microsoft. TSPI definisce le funzioni esterne esposte da un provider di servizi di telefonia fornito con apparecchiature di comunicazione.

## <a name="developer-audience"></a>Sviluppatori

È possibile scrivere applicazioni abilitate per TAPI in molti linguaggi, tra cui Java, Visual Basic e C/C++. L'esperienza di sviluppo precedente con le telecomunicazioni o altre applicazioni di telefonia è utile ma non necessaria.

## <a name="run-time-requirements"></a>Requisiti di runtime

TSPI consente lo sviluppo di TSP per tutte le versioni di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                | Descrizione                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Overview](about-the-telephony-service-provider-tsp-.md)<br/> | Informazioni generali sull'architettura e sui componenti di TSPI.<br/> |
| [Riferimento](tspi-reference.md)<br/>                           | Documentazione per le interfacce TSPI.<br/>                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica della telefonia Microsoft](./microsoft-telephony-overview.md)
</dt> <dt>

[Provider di servizi multimediali](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2.2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3.1](./tapi-3-1-start-page.md)
</dt> </dl>

 

