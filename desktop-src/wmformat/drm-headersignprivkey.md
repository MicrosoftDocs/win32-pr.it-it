---
title: DRM_HeaderSignPrivKey
description: La proprietà DRM \_ HeaderSignPrivKey contiene la chiave privata usata per firmare l'intestazione ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey windows Media Format
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7f8cc90e509294d9de9d3577ad5a2d56b61eb3a471f9b493e555c0f1ecf824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547611"
---
# <a name="drm_headersignprivkey"></a>Intestazione \_ DRMSignPrivKey

La **proprietà DRM \_ HeaderSignPrivKey** contiene la chiave privata usata per firmare l'intestazione ASF.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Tipo di dati

**STRINGA DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Questa proprietà viene generata usando [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Mantenere il segreto della chiave e condividere la chiave pubblica solo con il servizio licenze. Dopo aver impostato questa chiave, il componente DRM la userà per firmare l'intestazione del file ASF (non l'intestazione DRM firmata con i valori dell'oggetto firma digitale, ad esempio DRM \_ LASignaturePrivKey). Ovviamente, **DRM \_ HeaderSignPrivKey** non è incluso nell'intestazione del file.

Questa proprietà non è accessibile dall'oggetto reader. Può essere impostato dall'oggetto writer usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




