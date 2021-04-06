---
title: Acquisizione di una licenza invisibile all'utente
description: Acquisizione di una licenza invisibile all'utente
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media Format SDK, acquisizione di una licenza invisibile all'utente
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), acquisizione di licenze Silent
- DRM (Digital Rights Management), acquisizione di licenze Silent
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, acquisizione di licenze Silent
- API estese client, acquisizione di licenze Silent
- acquisizione di una licenza invisibile all'utente
- licenze, acquisizione di licenze Silent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045002"
---
# <a name="silent-license-acquisition"></a>Acquisizione di una licenza invisibile all'utente

L'acquisizione di una licenza invisibile all'utente richiede solo una singola chiamata al metodo che gestisce in modo asincrono tutte le comunicazioni di rete con il server licenze.

Questo tipo di acquisizione della licenza viene in genere usato come risposta all'utente finale che tenta di accedere al contenuto protetto, ad esempio, tentando di riprodurre un file protetto in un'applicazione di Media Player. Poiché l'acquisizione di una licenza invisibile all'utente ottiene la licenza con una singola chiamata, non può essere usata se è necessario un input aggiuntivo da parte dell'utente, ad esempio il pagamento per il contenuto.

Per eseguire l'acquisizione di una licenza invisibile all'utente, attenersi alla procedura seguente:

1.  Chiamare il metodo [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Passare l'intestazione DRM dal file protetto come parametro *bstrHeaderData* . Specificare i diritti che si desidera concedere alla licenza nel parametro *bstrActions* . Infine, impostare il parametro *dwFlags* su WMDRM \_ acquisisce \_ licenza invisibile all' \_ utente.
2.  Eventi trap per l'interfaccia [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) . Quando si riceve l'evento **MEWMDRMLicenseAcquisitionCompleted** , controllare il codice restituito chiamando il metodo **IMFMediaEvent:: GetStatus** , che è documentato nella documentazione di Media Foundation. Se il valore **HRESULT** recuperato è un codice di esito positivo, la licenza è stata scaricata correttamente e si trova nell'archivio licenze locale pronto per l'utilizzo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Acquisizione di licenze**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modello di eventi Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




