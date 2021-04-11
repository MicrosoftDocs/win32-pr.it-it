---
title: DRM_Level
description: '\_Il livello DRM è un attributo di licenza impostato da Windows Media Format SDK quando crea una licenza locale per i file protetti con la versione 1 di DRM.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336426"
---
# <a name="drm_level"></a>\_Livello DRM

**DRM \_ Level** è un attributo di licenza impostato da Windows Media Format SDK quando crea una licenza locale per i file protetti con la versione 1 di DRM. Contiene il livello di sicurezza che l'applicazione chiamante deve avere per accedere al contenuto del file. Il valore predefinito è 150.

## <a name="global-constant"></a>Costante globale

\_livello g wszWMDRM \_

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Il livello di sicurezza DRM di un'applicazione è determinato dalla particolare libreria WMStubDRM a cui si collega in fase di compilazione. Per ulteriori informazioni su questi livelli di sicurezza, vedere [ottenere la libreria DRM necessaria](obtaining-the-required-drm-library.md). Usare [**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà quando si proteggono i file ASF con DRM versione 1.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




