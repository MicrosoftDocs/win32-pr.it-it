---
title: Interfaccia IWMDRMNonSilentLicenseAquisition
description: L'interfaccia IWMDRMNonSilentLicenseAquisition fornisce metodi che consentono l'acquisizione delle licenze che richiedono l'intervento dell'utente. Questa interfaccia può essere ottenuta eseguendo l'acquisizione di licenze non invisibile all'utente.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Interfaccia IWMDRMNonSilentLicenseAquisition windows Media Format
- Interfaccia IWMDRMNonSilentLicenseAquisition windows Media Format , descritta
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c953588cb457e8afb21cca38e9daed08b2387ab9fb7871ecd6b17dae9dca152f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110351"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Interfaccia IWMDRMNonSilentLicenseAquisition

**L'interfaccia IWMDRMNonSilentLicenseAquisition** fornisce metodi che consentono l'acquisizione delle licenze che richiedono l'intervento dell'utente.

Questa interfaccia può essere ottenuta eseguendo l'acquisizione di licenze non invisibile all'utente. Dopo aver chiamato [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) verrà generato un evento **MEWMDRMLicenseAcquisitionCompleted.** Chiamare il **metodo IMFMediaEvent::GetValue** dell'evento per ottenere un puntatore a un'interfaccia **IUnknown** su cui è possibile eseguire query per un puntatore a un'istanza di questa interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IWMDRMNonSilentLicenseAquisition** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMNonSilentLicenseAquisition** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMDRMNonSilentLicenseAquisition** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Recupera la richiesta di licenza che deve essere pubblicata nel server licenze.<br/> |
| [**Geturl**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Recupera l'URL in cui deve essere pubblicata la richiesta di licenza.<br/>           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**Acquisizione di licenze non invisibile all'utente**](non-silent-license-acquisition.md)
</dt> </dl>

 

