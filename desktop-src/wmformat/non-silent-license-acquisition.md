---
title: Acquisizione di licenza non invisibile all'utente
description: Acquisizione di licenza non invisibile all'utente
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK, acquisizione di licenze non invisibile all'utente
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), acquisizione di licenze non invisibile all'utente
- DRM (Digital Rights Management), acquisizione di licenze non invisibile all'utente
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, acquisizione di licenze non invisibile all'utente
- API estese client, acquisizione di licenze non invisibile all'utente
- acquisizione di licenza non invisibile all'utente
- licenze, acquisizione di licenze non Silent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516057"
---
# <a name="non-silent-license-acquisition"></a>Acquisizione di licenza non invisibile all'utente

L'acquisizione di licenze non Silent consente al provider di licenze di interagire con l'utente finale tramite una pagina Web, come un passaggio intermedio del processo di acquisizione delle licenze. L'acquisizione di una licenza non invisibile all'utente viene avviata in risposta a un utente che tenta di accedere al contenuto protetto.

Per eseguire l'acquisizione di una licenza non invisibile all'utente, attenersi alla procedura seguente:

1.  Chiamare il metodo [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Passare l'intestazione DRM dal file protetto come parametro *bstrHeaderData* . Specificare i diritti che si desidera concedere alla licenza nel parametro *bstrActions* . Infine, impostare il parametro *dwFlags* su WMDRM \_ acquisisce \_ licenza non \_ invisibile.
2.  Eventi trap per l'interfaccia **IWMDRMLicenseManagement** . Quando si riceve l'evento **MEWMDRMLicenseAcquisitionCompleted** , ottenere il valore associato chiamando **IMFMediaEvent:: GetValue**. Il valore deve essere di tipo VT \_ Unknown, un puntatore a un'interfaccia **IUnknown** .
3.  Chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata nel passaggio 2 per ottenere l'interfaccia [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .
4.  Chiamare [**IWMDRMNonSilentLicenseAquisition:: getchallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) per recuperare la richiesta di licenza. Chiamare anche [**IWMDRMNonSilentLicenseAquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) se non si ha già l'URL del server licenze.
5.  Invia la richiesta di verifica alla pagina Web specificata dall'URL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Acquisizione di licenze**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modello di eventi Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




