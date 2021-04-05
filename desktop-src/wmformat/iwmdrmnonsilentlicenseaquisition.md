---
title: Interfaccia IWMDRMNonSilentLicenseAquisition
description: L'interfaccia IWMDRMNonSilentLicenseAquisition fornisce metodi che consentono l'acquisizione di licenze che richiedono l'intervento dell'utente. Questa interfaccia può essere ottenuta eseguendo l'acquisizione di una licenza non invisibile all'utente.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Formato Windows Media Interface IWMDRMNonSilentLicenseAquisition
- Interfaccia IWMDRMNonSilentLicenseAquisition-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728711"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Interfaccia IWMDRMNonSilentLicenseAquisition

L'interfaccia **IWMDRMNonSilentLicenseAquisition** fornisce metodi che consentono l'acquisizione di licenze che richiedono l'intervento dell'utente.

Questa interfaccia può essere ottenuta eseguendo l'acquisizione di una licenza non invisibile all'utente. Dopo la chiamata a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , verrà generato un evento **MEWMDRMLicenseAcquisitionCompleted** . Chiamare il metodo **IMFMediaEvent:: GetValue** dell'evento per ottenere un puntatore a un'interfaccia **IUnknown** su cui è possibile eseguire una query per un puntatore a un'istanza di questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IWMDRMNonSilentLicenseAquisition** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNonSilentLicenseAquisition** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMNonSilentLicenseAquisition** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Getchallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Recupera la richiesta di licenza che deve essere inviata al server licenze.<br/> |
| [**GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Recupera l'URL a cui deve essere inviata la richiesta di licenza.<br/>           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**Acquisizione di licenza non invisibile all'utente**](non-silent-license-acquisition.md)
</dt> </dl>

 

