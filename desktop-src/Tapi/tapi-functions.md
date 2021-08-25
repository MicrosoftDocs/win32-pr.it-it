---
description: Le sezioni seguenti contengono un elenco alfabetico di funzioni raggruppate per area. Le informazioni per ogni funzione includono un elenco degli stati di chiamata validi all'ingresso della funzione e transizioni di stato di chiamata tipiche al termine della richiesta.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funzioni TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27ec2383f826efe5620ea44d3a643e46a90b08c7820548733238290bff26512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872911"
---
# <a name="tapi-functions"></a>Funzioni TAPI

Le sezioni seguenti contengono un elenco alfabetico di funzioni raggruppate per area. Le informazioni per ogni funzione includono un elenco degli stati di chiamata validi all'ingresso della funzione e transizioni di stato di chiamata tipiche al termine della richiesta.

-   [Funzioni di telefonia assistita](assisted-telephony-functions.md)
-   [Funzioni del call center](call-center-functions.md)
-   [Funzioni del dispositivo Line](line-device-functions.md)
-   [Telefono Funzioni del dispositivo](phone-device-functions.md)

Per le funzioni TAPI classificate in base al livello di servizio e all'attività, vedere [Riferimento rapido alle funzioni TAPI.](tapi-quick-function-reference.md)

Si noti che possono esistere limitazioni del provider di servizi relativamente agli stati effettivi in cui è possibile eseguire una funzione. Le applicazioni devono controllare il membro **dwCallFeatures** nella struttura [**LINECALLSTATUS,**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) il membro **dwAddressFeatures** nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) e il membro **dwLineFeatures** nella struttura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) per determinare se una funzione è consentita o meno all'interno dello stato di chiamata corrente.

 

 



