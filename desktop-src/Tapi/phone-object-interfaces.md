---
description: L'oggetto telefono è l'entità che rappresenta il dispositivo telefonico effettivo e tutti i relativi controlli.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Interfacce per oggetti telefono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315275"
---
# <a name="phone-object-interfaces"></a>Interfacce per oggetti telefono

L'oggetto telefono è l'entità che rappresenta il dispositivo telefonico effettivo e tutti i relativi controlli.

Le interfacce [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) non sono direttamente esposte sull'oggetto Phone, ma sono strettamente correlate e sono elencate di seguito per praticità di riferimento.



| Interfaccia                                                  | Descrizione                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Consente l'accesso al dispositivo telefonico a un livello paragonabile a quello disponibile con TAPI 2. API *x* C.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Fornisce metodi per il controllo automatizzato dei toni e degli anelli di un telefono e per la gestione automatica delle chiamate in base allo stato hookswitch del telefono. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descrizione degli eventi del telefono.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



