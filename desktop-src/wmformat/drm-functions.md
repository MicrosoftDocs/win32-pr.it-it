---
title: Funzioni client DRM di Microsoft Windows Media
description: Funzioni client DRM di Microsoft Windows Media
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK, funzioni
- Digital Rights Management (DRM), funzioni
- DRM (Digital Rights Management), funzioni
- API estese del client DRM, funzioni
- API estese client, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300796"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Funzioni client DRM di Microsoft Windows Media

Le funzioni seguenti sono implementate come parte delle API estese del client DRM di Microsoft Windows Media.



| Funzione                                                             | Descrizione                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Crea un class factory in grado di creare gli altri oggetti DRM. Questa funzione non richiede una libreria stub di Microsoft e crea oggetti che non supportano le funzionalità DRM protette. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Crea un class factory in grado di creare gli altri oggetti DRM. Questa funzione richiede una libreria stub di Microsoft e crea oggetti che supportano le funzionalità DRM protette.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Rilascia le risorse usate dalle API.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Inizializza le risorse usate dalle API.                                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](drm-programming-reference.md)
</dt> </dl>

 

 




