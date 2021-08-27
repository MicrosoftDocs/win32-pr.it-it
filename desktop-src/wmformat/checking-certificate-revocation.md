---
title: Controllo della revoca dei certificati
description: Controllo della revoca dei certificati
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows SDK formato multimediale,importazione DRM
- Windows MEDIA Format SDK, importazione
- Windows MEDIA Format SDK, revoca del certificato
- Windows Media Format SDK, revoca dei certificati
- digital rights management (DRM), importazione
- DRM (Digital Rights Management),importazione
- digital rights management (DRM), revoca del certificato
- DRM (Digital Rights Management),revoca del certificato
- digital rights management (DRM), revoca dei certificati
- DRM (Digital Rights Management),revoca dei certificati
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, revoca del certificato
- API estese del client, revoca del certificato
- API estese del client DRM, revoca dei certificati
- API estese client, revoca dei certificati
- certificati, revoca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d9f8aaa299873513f88a2be258cf2ddd96147934e461cbde49630542fd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028069"
---
# <a name="checking-certificate-revocation"></a>Controllo della revoca dei certificati

Quando si importa contenuto in Windows Media DRM, è necessario assicurarsi che nessun certificato in una raccolta di certificati sia stato revocato verificando che nessun certificato nella raccolta sia presente nell'elenco di revoche. L'elenco di revoche viene estratto usando il [**metodo IWMDRMSecurity::GetRevocationData.**](iwmdrmsecurity-getrevocationdata.md)

Usare quindi il [**metodo IWMDRMSecurity::CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) per verificare che il certificato non sia revocato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Importazione DRM**](drm-import.md)
</dt> </dl>

 

 




