---
description: Le funzioni di telefonia estese sono elencate per categoria nelle tabelle seguenti.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Informazioni di riferimento sui servizi di telefonia estesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307194"
---
# <a name="extended-telephony-services-reference"></a>Informazioni di riferimento sui servizi di telefonia estesa

Le funzioni di telefonia estese sono elencate per categoria nelle tabelle seguenti.

## <a name="extended-telephony-functions-for-line-devices"></a>Funzioni di telefonia estese per dispositivi line



| Funzione                                                   | Descrizione                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | Consente a un'applicazione di negoziare una versione di estensione da usare con il dispositivo a linee specificato. Asincrona. |
| [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | Consente ai provider di servizi di accedere alle funzionalità specifiche del dispositivo non offerte da altre funzioni TAPI. Synchronous. |
| [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | Invia le funzionalità di commutazione specifiche del dispositivo al Commuter. Asincrona.                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a>Funzioni di telefonia estese per i dispositivi telefonici



| Funzione                                                     | Descrizione                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | Funzione di escape specifica del dispositivo per consentire le estensioni dipendenti dal fornitore. Asincrona.                          |
| [**PhoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Consente a un'applicazione di negoziare una versione di estensione da usare con il dispositivo telefonico specificato. Synchronous. |



 

 

 



