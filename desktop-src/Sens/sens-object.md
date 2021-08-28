---
description: System Event Notification Service (SENS) definisce la coclasse SENS come parte della libreria dei tipi SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Oggetto SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acdf70b5e2229051d569bd1f607ad8db5d3d567b4c0421464757f02bc6a8e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003949"
---
# <a name="sens-object"></a>Oggetto SENS

System Event Notification Service (SENS) definisce la coclasse SENS come parte della libreria dei tipi SENS.

## <a name="implementation"></a>Implementazione

L'implementazione dell'oggetto SENS viene fornita dal sistema operativo.

## <a name="creationaccess-functions"></a>Funzioni di creazione/accesso



| Funzione                                      | Descrizione                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Crea un'istanza dell'oggetto SENS usando il relativo CLSID. |



 

## <a name="interfaces"></a>Interfacce



| Interfaccia                            | Descrizione                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Valore predefinito. Interfaccia in uscita implementata dall'oggetto sink nell'applicazione sottoscrittore.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Interfaccia in uscita implementata dall'oggetto sink nell'applicazione sottoscrittore.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Interfaccia in uscita implementata dall'oggetto sink nell'applicazione sottoscrittore.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Interfaccia in uscita implementata dall'oggetto sink nell'applicazione sottoscrittore. Disponibile con Windows XP. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[Informazioni sul servizio di notifica degli eventi di sistema](about-system-event-notification-service.md)
</dt> </dl>

 

 
