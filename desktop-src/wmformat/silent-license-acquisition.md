---
title: Acquisizione delle licenze invisibile all'utente
description: Acquisizione delle licenze invisibile all'utente
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media Format SDK, acquisizione di licenze invisibile all'utente
- Windows Media Format SDK, licenze
- digital rights management (DRM), acquisizione di licenze invisibile all'utente
- DRM (Digital Rights Management),acquisizione delle licenze invisibile all'utente
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- API estese del client DRM, acquisizione di licenze invisibile all'utente
- API client estese, acquisizione di licenze invisibile all'utente
- acquisizione di licenze invisibile all'utente
- licenze, acquisizione di licenze invisibile all'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eff454ce673230f0c7dbe6f64afbf46e9bbe8b5f948609f5fb67d647a4151ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197463"
---
# <a name="silent-license-acquisition"></a>Acquisizione delle licenze invisibile all'utente

L'acquisizione automatica delle licenze richiede una sola chiamata al metodo che gestisce tutte le comunicazioni di rete con il server licenze in modo asincrono.

Questo tipo di acquisizione della licenza viene in genere usato come risposta all'utente finale che tenta di accedere a contenuto protetto, ad esempio per riprodurre un file protetto in un'applicazione lettore multimediale. Poiché l'acquisizione automatica delle licenze ottiene la licenza con una singola chiamata, non può essere usata se è necessario un input aggiuntivo da parte dell'utente, ad esempio il pagamento del contenuto.

Per eseguire l'acquisizione automatica delle licenze, seguire questa procedura:

1.  Chiamare il [**metodo IWMDRMLicenseManagement::AcquireLicense.**](iwmdrmlicensemanagement-acquirelicense.md) Passare l'intestazione DRM dal file protetto come *parametro bstrHeaderData.* Specificare i diritti che la licenza deve concedere nel *parametro bstrActions.* Infine, impostare il *parametro dwFlags* su WMDRM \_ ACQUIRE LICENSE \_ \_ SILENT.
2.  Eventi trap per [**l'interfaccia IWMDRMLicenseManagement.**](iwmdrmlicensemanagement.md) Quando si riceve l'evento **MEWMDRMLicenseAcquisitionCompleted,** controllarne il codice restituito chiamando il metodo **IMFMediaEvent::GetStatus,** documentato nella documentazione di Media Foundation. Se il valore **HRESULT recuperato** è un codice di esito positivo, la licenza è stata scaricata correttamente e si trova nell'archivio licenze locale pronto per l'uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Acquisizione delle licenze**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modello Media Foundation eventi**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




