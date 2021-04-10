---
title: Interfaccia IWMDRMIndividualizationStatus
description: L'interfaccia IWMDRMIndividualizationStatus consente il recupero delle informazioni di stato avanzate sullo stato di avanzamento della singola. Questa interfaccia viene fornita con gli eventi MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Formato Windows Media Interface IWMDRMIndividualizationStatus
- Interfaccia IWMDRMIndividualizationStatus-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963333"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>Interfaccia IWMDRMIndividualizationStatus

L'interfaccia **IWMDRMIndividualizationStatus** consente il recupero delle informazioni di stato avanzate sullo stato di avanzamento della singola.

Questa interfaccia viene fornita con gli eventi MEWMDRMIndividualizationProgress. Molti di questi eventi vengono generati tra una chiamata a [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) e il completamento del processo di individualizzazione, segnalato dalla generazione di un evento **MEWMDRMIndividualizationCompleted** .

Per recuperare un puntatore a un'istanza dell'interfaccia **IWMDRMIndividualizationStatus** , è prima necessario chiamare il metodo **IMFMediaEvent:: GetValue** dell'evento Progress. Il valore recuperato dall'evento è un puntatore all'interfaccia **IUnknown** dell'oggetto che implementa l'interfaccia **IWMDRMIndividualizationStatus** .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMIndividualizationStatus** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMIndividualizationStatus** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMIndividualizationStatus** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Recupera informazioni dettagliate sulla individualizzazione.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> </dl>

 

