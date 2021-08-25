---
title: Funzioni client DRM di Microsoft Windows Media
description: Funzioni client DRM di Microsoft Windows Media
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK,funzioni
- digital rights management (DRM), funzioni
- DRM (digital rights management),funzioni
- API estese del client DRM, funzioni
- API estese client,funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aaf5f3c536027801a85f8d38120e6e14c5d366a6d727498a5bc1d1200cb041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931171"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Funzioni client DRM di Microsoft Windows Media

Le funzioni seguenti vengono implementate come parte delle API estese del client Microsoft Windows Media DRM.



| Funzione                                                             | Descrizione                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Crea un class factory che può creare gli altri oggetti DRM. Questa funzione non richiede una libreria stub da Microsoft e crea oggetti che non supportano le funzionalità DRM protette. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Crea un class factory che può creare gli altri oggetti DRM. Questa funzione richiede una libreria stub di Microsoft e crea oggetti che supportano le funzionalità DRM protette.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Rilascia le risorse usate dalle API.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Inizializza le risorse usate dalle API.                                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](drm-programming-reference.md)
</dt> </dl>

 

 




