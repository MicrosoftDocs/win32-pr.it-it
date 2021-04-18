---
description: L'oggetto TAPI è l'oggetto principale per TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfacce di oggetti TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316021"
---
# <a name="tapi-object-interfaces"></a>Interfacce di oggetti TAPI

L' [oggetto TAPI](tapi-object.md) è l'oggetto principale per TAPI 3.

L'interfaccia [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) non è esposta direttamente nell'oggetto TAPI, ma è strettamente correlata e viene elencata qui per praticità di riferimento.



| Interfacce                                                 | Descrizione                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Interfaccia TAPI 3 primaria.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Deriva da [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); fornisce metodi aggiuntivi che supportano i dispositivi telefonici.                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Interfaccia in uscita utilizzata per ricevere informazioni asincrone sugli eventi TAPI 3.                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Fornisce un'interfaccia di ingresso nei controlli del Call Center.                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Fornisce metodi per recuperare le informazioni relative agli eventi degli oggetti TAPI.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Estende [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); fornisce un metodo per recuperare un puntatore all'oggetto Phone che ha causato l'evento dell'oggetto TAPI. |



 

 

 
