---
title: Creazione di licenze localmente
description: Creazione di licenze localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows Media Format SDK, creazione di licenze localmente
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), creazione di licenze localmente
- DRM (Digital Rights Management), creazione di licenze localmente
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, creazione di licenze localmente
- API estese client, creazione di licenze localmente
- licenze, creazione di licenze in locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045333"
---
# <a name="creating-licenses-locally"></a>Creazione di licenze localmente

In alcuni casi, ad esempio durante l' [importazione di DRM](drm-import.md), è possibile creare licenze personalizzate. Le licenze DRM di Windows Media possono essere scritte in modi diversi, ma per creare una licenza personalizzata è necessario utilizzare lo schema binario XMR (Extensible Media Rights). Per ulteriori informazioni, vedere la pagina relativa alla [compilazione di una licenza XMR](building-an-xmr-license.md).

Quando si crea una licenza, è possibile aggiungerla all'archivio licenze locale chiamando il metodo [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Acquisizione di licenze**](acquiring-licenses.md)
</dt> <dt>

[**Creazione di una licenza XMR**](building-an-xmr-license.md)
</dt> </dl>

 

 




