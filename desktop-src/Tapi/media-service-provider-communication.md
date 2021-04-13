---
description: A partire da provider di servizi di telefonia Windows 2000 che negoziano una versione di 3,0 o successiva deve avere un provider di servizi multimediali corrispondente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicazione del provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351476"
---
# <a name="media-service-provider-communication"></a>Comunicazione del provider di servizi multimediali

A partire da provider di servizi di telefonia Windows 2000 che negoziano una versione di 3,0 o successiva deve avere un provider di servizi multimediali corrispondente. La divisione precisa delle responsabilità operative è dipendente dall'implementazione. Un TSP potrebbe, ad esempio, utilizzare l'MSP corrispondente per eseguire la determinazione del tipo di supporto in una sessione in ingresso. Tuttavia, il TSP deve essere conforme al TSPI, il che significa ottenere tale determinazione dal MSP e segnalarlo a TAPI.

TSPI fornisce le funzioni e i messaggi seguenti per consentire una connessione virtuale tra un TSP e un MSP:

-   [**\_LINECLOSEMSPINSTANCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**\_LINECREATEMSPINSTANCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**\_LINEMSPIDENTIFY TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**\_LINERECEIVEMSPDATA TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**LINEA \_ QOSINFO**](line-qosinfo.md)
-   [**LINEA \_ SENDMSPDATA**](line-sendmspdata.md)

 

 
