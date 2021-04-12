---
description: Le sezioni seguenti contengono un elenco alfabetico di funzioni raggruppate per area. Le informazioni per ogni funzione includono un elenco degli Stati di chiamata validi all'immissione della funzione e le transizioni tipiche dello stato di chiamata al completamento della richiesta.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funzioni TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529214"
---
# <a name="tapi-functions"></a>Funzioni TAPI

Le sezioni seguenti contengono un elenco alfabetico di funzioni raggruppate per area. Le informazioni per ogni funzione includono un elenco degli Stati di chiamata validi all'immissione della funzione e le transizioni tipiche dello stato di chiamata al completamento della richiesta.

-   [Funzioni di telefonia assistita](assisted-telephony-functions.md)
-   [Funzioni Call Center](call-center-functions.md)
-   [Funzioni del dispositivo linea](line-device-functions.md)
-   [Funzioni del dispositivo telefonico](phone-device-functions.md)

Per le funzioni TAPI categorizzate in base al livello di servizio e all'attività, vedere informazioni di [riferimento sulle funzioni TAPI Quick](tapi-quick-function-reference.md).

Si noti che possono esistere limitazioni del provider di servizi riguardanti gli Stati effettivi in cui è possibile eseguire una funzione. Le applicazioni devono verificare il membro **dwCallFeatures** nella struttura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , il membro **dwAddressFeatures** nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) e il membro **dwLineFeatures** nella struttura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) per determinare se una funzione è consentita o meno nello stato di chiamata corrente.

 

 



