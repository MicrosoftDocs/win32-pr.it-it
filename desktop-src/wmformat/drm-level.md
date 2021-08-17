---
title: DRM_Level
description: Livello DRM è un attributo di licenza impostato da Windows Media Format SDK quando crea una licenza locale per i file protetti \_ con DRM versione 1.
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level windows Media Format
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4767f839c5d21610e7e425aea4a20a52c3cb0d8658848f578a33ca403f4ad60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848684"
---
# <a name="drm_level"></a>Livello \_ DRM

**DRM \_ Level** è un attributo di licenza impostato Windows Media Format SDK quando crea una licenza locale per i file protetti con DRM versione 1. Contiene il livello di sicurezza che l'applicazione chiamante deve avere per accedere al contenuto nel file. Il valore predefinito è 150.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ Level

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Il livello di sicurezza DRM di un'applicazione è determinato dalla particolare libreria wmstubdrm a cui si collega in fase di compilazione. Per altre informazioni su questi livelli di sicurezza, vedere [Recupero della libreria DRM richiesta.](obtaining-the-required-drm-library.md) Usare [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà quando si proteggono i file ASF con DRM versione 1.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




