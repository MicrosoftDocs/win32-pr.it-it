---
title: Importazione del materiale della licenza e della chiave
description: Importazione del materiale della licenza e della chiave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), materiale della chiave
- DRM (Digital Rights Management), materiale della chiave
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, materiale della chiave
- API estese client, materiale della chiave
- licenze, importazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221975"
---
# <a name="importing-license-and-key-material"></a>Importazione del materiale della licenza e della chiave

Se si dispone di contenuto multimediale crittografato utilizzando un sistema di protezione del contenuto di terze parti e si desidera importare il materiale della licenza e della chiave in Windows Media DRM, attenersi alla procedura seguente:

1.  Recuperare la raccolta di certificati del computer Windows Media DRM chiamando il metodo [**IWMDRMSecurity:: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .
2.  Analizzare la raccolta di certificati, assicurandosi che sia firmato correttamente e che venga convalidato con una chiave pubblica radice Microsoft nota. La raccolta di certificati è conforme allo schema XMR. Per ulteriori informazioni, vedere la pagina relativa alla [compilazione di una licenza XMR](building-an-xmr-license.md).
3.  Facoltativo: estrarre l'elenco di revoche chiamando il metodo [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
4.  Facoltativo: assicurarsi che non sia stato revocato alcun certificato nella raccolta. Per ulteriori informazioni, vedere [controllo della revoca del certificato](checking-certificate-revocation.md).
5.  Generare una licenza nel formato XMR che rappresenta i requisiti dei criteri per il contenuto di importazione e contiene il materiale della chiave DRM di Windows Media appropriato. Per ulteriori informazioni, vedere l'argomento [compilazione di una licenza XMR](building-an-xmr-license.md).
6.  Passare la licenza XMR al sistema Windows Media DRM per l'elaborazione, usando il metodo [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

> [!Note]  
> Informazioni dettagliate sullo schema XMR verranno fornite quando si esegue la licenza di Windows Media DRM.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Verifica della revoca dei certificati**](checking-certificate-revocation.md)
</dt> <dt>

[**Creazione di una licenza XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importazione DRM**](drm-import.md)
</dt> </dl>

 

 




