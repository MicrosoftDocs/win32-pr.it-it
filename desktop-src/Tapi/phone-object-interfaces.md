---
description: L Telefono o object è l'entità che rappresenta il dispositivo telefonico effettivo e tutti i relativi controlli.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Telefono Interfacce di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e146910b8184f35057843f20ad663e2be21d2c4844852e7cca3939e1e979d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873271"
---
# <a name="phone-object-interfaces"></a>Telefono Interfacce di oggetti

L Telefono o object è l'entità che rappresenta il dispositivo telefonico effettivo e tutti i relativi controlli.

Le [**interfacce ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) non sono esposte direttamente nell'oggetto Telefono, ma sono strettamente correlate e sono elencate qui per praticità di riferimento.



| Interfaccia                                                  | Descrizione                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Consente l'accesso al dispositivo telefonico a un livello simile a quello disponibile con TAPI 2. *x* API C.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Fornisce metodi per il controllo automatizzato dei toni e degli anelli di un telefono e per la gestione automatizzata delle chiamate in base allo stato del hookswitch di un telefono. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descrizione degli eventi del telefono.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumera [**ITPhone.**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                                                                                    |



 

 

 



