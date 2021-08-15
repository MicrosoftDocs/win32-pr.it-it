---
title: Importazione di licenze e materiale delle chiavi
description: Importazione di licenze e materiale delle chiavi
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows SDK formato multimediale,importazione DRM
- Windows MEDIA Format SDK, importazione
- Windows Media Format SDK, licenze
- digital rights management (DRM), importazione
- DRM (Digital Rights Management),importazione
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- digital rights management (DRM), materiale della chiave
- DRM (Digital Rights Management),materiale della chiave
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, licenze
- API client estese, licenze
- API estese del client DRM, materiale della chiave
- API client estese, materiale della chiave
- licenze, importazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9852102ab282c983488c2e5c35b7187bf0daccb62d347c312d1afb343b60f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702505"
---
# <a name="importing-license-and-key-material"></a>Importazione di licenze e materiale delle chiavi

Se si dispone di contenuto multimediale crittografato con un sistema di protezione del contenuto di terze parti e si vuole importare la licenza e il materiale della chiave in Windows Media DRM, seguire questa procedura:

1.  Recuperare la Windows di certificati del computer Media DRM chiamando il [**metodo IWMDRMSecurity::GetMachineCertificate.**](iwmdrmsecurity-getmachinecertificate.md)
2.  Analizzare la raccolta di certificati, verificando che sia firmata correttamente e convalidata in una chiave pubblica radice Microsoft nota. La raccolta di certificati è conforme allo schema XMR. Per altre informazioni, vedere [Building an XMR License (Creazione di una licenza XMR).](building-an-xmr-license.md)
3.  Facoltativo: estrarre l'elenco di revoche chiamando il [**metodo IWMDRMSecurity::GetRevocationData.**](iwmdrmsecurity-getrevocationdata.md)
4.  Facoltativo: assicura che nessun certificato nella raccolta sia revocato. Per altre informazioni, vedere [Controllo della revoca dei certificati.](checking-certificate-revocation.md)
5.  Generare una licenza nel formato XMR che rappresenta i requisiti dei criteri per il contenuto di importazione e contiene il materiale della chiave Windows Media DRM appropriato. Per altre informazioni, vedere l'argomento [Creazione di una licenza XMR.](building-an-xmr-license.md)
6.  Passare la licenza XMR al sistema Windows Media DRM per l'elaborazione, usando il metodo [**IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md)

> [!Note]  
> I dettagli sullo schema XMR verranno forniti all'utente quando si Windows Media DRM.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Controllo della revoca dei certificati**](checking-certificate-revocation.md)
</dt> <dt>

[**Creazione di una licenza XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importazione DRM**](drm-import.md)
</dt> </dl>

 

 




