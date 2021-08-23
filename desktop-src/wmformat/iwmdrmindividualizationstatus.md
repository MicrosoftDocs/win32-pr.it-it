---
title: Interfaccia IWMDRMIndividualizationStatus
description: L'interfaccia IWMDRMIndividualizationStatus consente il recupero di informazioni di stato avanzate sullo stato di avanzamento della individualizzazione. Questa interfaccia viene recapitata con gli eventi MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Interfaccia IWMDRMIndividualizationStatus windows Media Format
- Interfaccia IWMDRMIndividualizationStatus windows Media Format , descritta
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6242d2c66b165be8c750d71c61020e9a6acc66f68654d73898fd5000ace3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701470"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>Interfaccia IWMDRMIndividualizationStatus

**L'interfaccia IWMDRMIndividualizationStatus** consente il recupero di informazioni di stato avanzate sullo stato di avanzamento della individualizzazione.

Questa interfaccia viene recapitata con gli eventi MEWMDRMIndividualizationProgress. Molti eventi di questo tipo vengono generati tra una chiamata a [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) e il completamento del processo di individualizzazione, segnalato dalla generazione di un evento **MEWMDRMIndividualizationCompleted.**

Per recuperare un puntatore a un'istanza **dell'interfaccia IWMDRMIndividualizationStatus,** è innanzitutto necessario chiamare il metodo **IMFMediaEvent::GetValue** dell'evento di stato. Il valore recuperato dall'evento è un puntatore all'interfaccia **IUnknown** dell'oggetto che implementa **l'interfaccia IWMDRMIndividualizationStatus.**

## <a name="members"></a>Membri

**L'interfaccia IWMDRMIndividualizationStatus** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMIndividualizationStatus** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMDRMIndividualizationStatus** include questi metodi.



| Metodo                                                       | Descrizione                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Recupera informazioni dettagliate sulla individualizzazione.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> </dl>

 

