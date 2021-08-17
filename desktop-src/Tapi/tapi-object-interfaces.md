---
description: L'oggetto TAPI è l'oggetto principale per TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfacce di oggetti TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1e49fe83a75c802b06ded953f309a157365d482d22d06c6bbedf97a5b8ac7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139854"
---
# <a name="tapi-object-interfaces"></a>Interfacce di oggetti TAPI

[L'oggetto TAPI](tapi-object.md) è l'oggetto principale per TAPI 3.

[**L'interfaccia ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) non è esposta direttamente nell'oggetto TAPI, ma è strettamente correlata ed è elencata qui per praticità di riferimento.



| Interfacce                                                 | Descrizione                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Interfaccia TAPI 3 primaria.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Deriva da [**ITTAPI;**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi) fornisce metodi aggiuntivi che supportano i dispositivi telefonici.                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Interfaccia in uscita usata per ricevere informazioni asincrone sugli eventi TAPI 3.                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Fornisce un'interfaccia di ingresso nei controlli call center.                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Fornisce metodi per recuperare informazioni relative agli eventi dell'oggetto TAPI.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Estende [**ITTAPIObjectEvent;**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) fornisce un metodo per recuperare un puntatore all'oggetto telefono che ha causato l'evento dell'oggetto TAPI. |



 

 

 
