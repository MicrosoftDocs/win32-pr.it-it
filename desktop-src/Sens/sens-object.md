---
description: Il servizio di notifica eventi di sistema (SENS) definisce la coclasse SENS come parte della libreria dei tipi SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Oggetto SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316626"
---
# <a name="sens-object"></a>Oggetto SENS

Il servizio di notifica eventi di sistema (SENS) definisce la coclasse SENS come parte della libreria dei tipi SENS.

## <a name="implementation"></a>Implementazione

L'implementazione dell'oggetto SENS viene fornita dal sistema operativo.

## <a name="creationaccess-functions"></a>Funzioni di creazione/accesso



| Funzione                                      | Descrizione                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Crea un'istanza dell'oggetto SENS utilizzando il relativo CLSID. |



 

## <a name="interfaces"></a>Interfacce



| Interfaccia                            | Descrizione                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Valore predefinito. Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore. Disponibile con Windows XP. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[Informazioni sul servizio di notifica eventi di sistema](about-system-event-notification-service.md)
</dt> </dl>

 

 
