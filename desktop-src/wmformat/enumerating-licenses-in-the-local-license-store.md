---
title: Enumerazione delle licenze nell'archivio licenze locale
description: Enumerazione delle licenze nell'archivio licenze locale
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK, enumerazione delle licenze
- Windows Media Format SDK, licenze
- Windows Media Format SDK, archivio licenze locale
- Digital Rights Management (DRM), enumerazione delle licenze
- DRM (Digital Rights Management), enumerazione delle licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), archivio licenze locale
- DRM (Digital Rights Management), archivio licenze locale
- API estese del client DRM, enumerazione delle licenze
- API estese client, enumerazione delle licenze
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, archivio licenze locale
- API estese client, archivio licenze locale
- licenze, enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395619"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Enumerazione delle licenze nell'archivio licenze locale

L'enumerazione è un processo che consente di ottenere informazioni sulle licenze nell'archivio licenze locale, eseguendone un'istruzione alla volta. È possibile creare un'enumerazione delle licenze chiamando [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).

Il motivo più comune per l'enumerazione delle licenze nell'archivio è quello di trovare una licenza particolare per la decrittografia di alcuni contenuti.

L'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) funge da portale per i singoli risultati della licenza e come enumeratore. Quando viene creata l'enumerazione delle licenze, la prima licenza nell'elenco viene caricata nell'interfaccia **IWMDRMLicense** . La maggior parte dei metodi di **IWMDRMLicense** consente di ottenere informazioni sulla licenza o creare oggetti per crittografare o decrittografare il contenuto in base alla licenza. Esistono tuttavia due metodi che controllano l'enumerazione: [**GetNext**](iwmdrmlicense-getnext.md) e [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md). **GetNext** carica la licenza successiva nell'elenco nell'interfaccia. **ResetEnumeration** restituisce l'enumerazione allo stato in cui si trovava al momento della creazione. Quando l'enumerazione viene reimpostata, la prima licenza nell'elenco viene ricaricata nell'interfaccia **IWMDRMLicense** .

Una volta raggiunta l'ultima licenza nell'elenco, la chiamata successiva a **GetNext** restituisce l'errore \_ non \_ più \_ elementi.

Se l'applicazione esegue un'azione con il contenuto coperto da DRM, è necessario controllare le licenze nell'archivio licenze locale per i diritti e per altri fattori di limitazione, ad esempio i livelli di protezione dell'output (OPLs).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero di informazioni dalle licenze nell'archivio licenze locale**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




