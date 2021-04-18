---
description: Un provider di servizi multimediali (MSP) consente a un'applicazione di controllare i supporti per un meccanismo di trasporto specifico.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320600"
---
# <a name="media-service-providers"></a>Provider di servizi multimediali

## <a name="purpose"></a>Scopo

Un provider di servizi multimediali (MSP) consente a un'applicazione di controllare i supporti per un meccanismo di trasporto specifico. Un MSP è sempre associato a un provider di servizi di telefonia (TSP).

Media Service Provider Interface (MSPI) è un set di interfacce e metodi implementati da un MSP per consentire a un'applicazione di controllare il trasporto multimediale durante una sessione di comunicazione. Un MSP gestisce i meccanismi specifici del dispositivo e specifici del protocollo necessari per applicare questi controlli e comunica con il relativo TSP associato o un'applicazione tramite l'uso dei metodi forniti in MSPI.

## <a name="developer-audience"></a>Sviluppatori

È necessaria una certa familiarità con COM. L'esperienza di sviluppo con le telecomunicazioni o altre applicazioni di telefonia è utile, ma non necessaria.

## <a name="run-time-requirements"></a>Requisiti di runtime

MSPI consente lo sviluppo di provider di servizi multimediali per determinati protocolli o dispositivi in esecuzione su sistemi operativi Windows Server 2003, Windows XP e Windows 2000.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Overview](about-the-media-service-provider-msp-.md)<br/>            | Informazioni generali sull'architettura e i componenti MSP.<br/> |
| [Riferimento](media-service-provider-interface-mspi-reference.md)<br/> | Documentazione per le interfacce MSPI.<br/>                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica della telefonia Microsoft](microsoft-telephony-overview.md)
</dt> <dt>

[TAPI 3,1](tapi-3-1-start-page.md)
</dt> <dt>

[Provider di servizi di telefonia](./telephony-service-providers-start-page.md)
</dt> </dl>

 

