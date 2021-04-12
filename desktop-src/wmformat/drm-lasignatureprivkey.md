---
title: DRM_LASignaturePrivKey
description: La \_ Proprietà DRM LASignaturePrivKey contiene la chiave privata usata per crittografare l'intestazione DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398620"
---
# <a name="drm_lasignatureprivkey"></a>\_LASIGNATUREPRIVKEY DRM

La proprietà **DRM \_ LASignaturePrivKey** contiene la chiave privata usata per crittografare l'intestazione DRM.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questa proprietà può essere generata usando il metodo [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) . Questa proprietà deve rimanere un segreto noto solo dall'autore del contenuto. Questa proprietà può essere impostata con il metodo [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) . Non è accessibile all'oggetto Reader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




