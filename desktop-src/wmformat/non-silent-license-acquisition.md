---
title: Acquisizione di licenze non invisibile all'utente
description: Acquisizione di licenze non invisibile all'utente
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK, acquisizione di licenze non invisibile all'utente
- Windows Media Format SDK, licenze
- digital rights management (DRM), acquisizione di licenze non invisibile all'utente
- DRM (digital rights management), acquisizione di licenze non invisibile all'utente
- digital rights management (DRM), licenze
- DRM (digital rights management), licenze
- API estese del client DRM, acquisizione di licenze non invisibile all'utente
- API estese client, acquisizione di licenze non invisibile all'utente
- acquisizione di licenze non invisibile all'utente
- licenze, acquisizione di licenze non invisibile all'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92c9350e429a1fe4b6218878d2211b355c1569b39284161f9f3abceac1afc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846435"
---
# <a name="non-silent-license-acquisition"></a>Acquisizione di licenze non invisibile all'utente

L'acquisizione di licenze non invisibile all'utente consente al provider di licenze di interagire con l'utente finale tramite una pagina Web, come passaggio intermedio del processo di acquisizione della licenza. L'acquisizione di licenze non invisibile all'utente viene avviata in risposta a un utente che tenta di accedere al contenuto protetto.

Per eseguire l'acquisizione di licenze non invisibile all'utente, seguire questa procedura:

1.  Chiamare il [**metodo IWMDRMLicenseManagement::AcquireLicense.**](iwmdrmlicensemanagement-acquirelicense.md) Passare l'intestazione DRM dal file protetto come *parametro bstrHeaderData.* Specificare i diritti che la licenza deve concedere nel *parametro bstrActions.* Infine, impostare il *parametro dwFlags* su WMDRM \_ ACQUIRE LICENSE \_ \_ NONSILENT.
2.  Eventi trap per **l'interfaccia IWMDRMLicenseManagement.** Quando si riceve **l'evento MEWMDRMLicenseAcquisitionCompleted,** ottenere il valore associato chiamando **IMFMediaEvent::GetValue**. Il valore deve essere di tipo VT \_ UNKNOWN, un puntatore a **un'interfaccia IUnknown.**
3.  Chiamare il **metodo QueryInterface** dell'interfaccia **IUnknown** recuperato nel passaggio 2 per ottenere l'interfaccia [**IWMDRMNonSilentLicenseAquisition.**](iwmdrmnonsilentlicenseaquisition.md)
4.  Chiamare [**IWMDRMNonSilentLicenseAquisition::GetChallenge per**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) recuperare la richiesta di licenza. Chiamare anche [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) se non si ha già l'URL del server licenze.
5.  Inviare la richiesta di richiesta alla pagina Web specificata dall'URL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Acquisizione di licenze**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modello Media Foundation eventi**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




