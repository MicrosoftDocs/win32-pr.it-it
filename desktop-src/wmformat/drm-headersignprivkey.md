---
title: DRM_HeaderSignPrivKey
description: La \_ Proprietà DRM HeaderSignPrivKey contiene la chiave privata usata per firmare l'intestazione ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey formato Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723487"
---
# <a name="drm_headersignprivkey"></a>\_HEADERSIGNPRIVKEY DRM

La proprietà **DRM \_ HeaderSignPrivKey** contiene la chiave privata usata per firmare l'intestazione ASF.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questa proprietà viene generata utilizzando [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Mantieni questo segreto chiave e Condividi la chiave pubblica solo con il servizio licenze. Dopo aver impostato questa chiave, il componente DRM lo utilizzerà per firmare l'intestazione del file ASF (non l'intestazione DRM firmata con i valori dell'oggetto firma digitale, ad esempio DRM \_ LASignaturePrivKey). Ovviamente, **DRM \_ HeaderSignPrivKey** non è incluso nell'intestazione del file.

Questa proprietà non è accessibile dall'oggetto Reader. Può essere impostata dall'oggetto writer usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




