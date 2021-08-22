---
description: A partire da Windows 2000 provider di servizi di telefonia che negoziano una versione 3.0 o successiva devono avere un provider di servizi multimediali corrispondente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicazione con il provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3797d02c67fc86ebfb44ff9e0e7b2c85cd1604206a58f1d8f5c3ca293599e92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404821"
---
# <a name="media-service-provider-communication"></a>Comunicazione con il provider di servizi multimediali

A partire da Windows 2000 provider di servizi di telefonia che negoziano una versione 3.0 o successiva devono avere un provider di servizi multimediali corrispondente. La suddivisione precisa delle responsabilità operative dipende dall'implementazione. Ad esempio, un provider di servizi di configurazione potrebbe usare il provider di servizi di configurazione corrispondente per eseguire la determinazione del tipo di supporto in una sessione in ingresso. Tuttavia, il TSP deve essere conforme al TSPI, ovvero ottenere tale determinazione dal provider di servizi di configurazione e segnalarlo a TAPI.

TSPI fornisce le funzioni e i messaggi seguenti per consentire una connessione virtuale tra un provider di servizi di configurazione e un provider di servizi di configurazione:

-   [**Riga \_ TSPICloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**Riga \_ TSPICreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**Riga \_ TSPIMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**LINE \_ QOSINFO**](line-qosinfo.md)
-   [**LINE \_ SENDMSPDATA**](line-sendmspdata.md)

 

 
