---
title: Visualizzazione degli attributi dei file protetti
description: Visualizzazione degli attributi dei file protetti
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK, visualizzazione degli attributi dei file protetti
- Windows Media Format SDK, attributi dei file protetti
- Windows Media Format SDK, file protetti
- Formato di sistemi avanzati (ASF), visualizzazione degli attributi dei file protetti
- ASF (Advanced Systems Format), visualizzazione degli attributi dei file protetti
- ASF (Advanced Systems Format), attributi dei file protetti
- ASF (Advanced Systems Format), attributi dei file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Digital Rights Management (DRM), visualizzazione degli attributi dei file protetti
- DRM (Digital Rights Management), visualizzazione degli attributi dei file protetti
- Digital Rights Management (DRM), attributi dei file protetti
- DRM (Digital Rights Management), attributi dei file protetti
- Digital Rights Management (DRM), file protetti
- DRM (Digital Rights Management), file protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723398"
---
# <a name="viewing-attributes-of-protected-files"></a>Visualizzazione degli attributi dei file protetti

In alcuni scenari potrebbe essere necessario recuperare determinati attributi DRM in un file senza accedere effettivamente al contenuto del file. Questa funzionalità è utile, ad esempio, nelle applicazioni che elaborano batch di file in modi diversi in base alle informazioni contenute nell'intestazione del file. Nelle versioni precedenti di Windows Media Format SDK, le applicazioni erano necessarie per il collegamento alla libreria statica DRM per poter aprire qualsiasi file protetto. Le applicazioni che non hanno la libreria DRM possono usare l'interfaccia [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) nell'oggetto editor dei metadati per esaminare alcuni attributi DRM.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaccia IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




