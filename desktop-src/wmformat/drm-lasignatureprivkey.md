---
title: DRM_LASignaturePrivKey
description: La proprietà \_ DRM LASignaturePrivKey contiene la chiave privata usata per crittografare l'intestazione DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey windows Media Format
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9354cc652bfce22183370b1183062d6cf7f27ce60b3681862f150f565d444a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704325"
---
# <a name="drm_lasignatureprivkey"></a>DRM \_ LASignaturePrivKey

La **proprietà \_ DRM LASignaturePrivKey** contiene la chiave privata usata per crittografare l'intestazione DRM.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Questa proprietà può essere generata usando il [**metodo IWMDRMWriter::GenerateSigningKeyPair.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) Questa proprietà deve rimanere un segreto noto solo all'autore del contenuto. Questa proprietà può essere impostata con [**il metodo IWMDRMWriter::SetDRMAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) Non è accessibile all'oggetto reader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




