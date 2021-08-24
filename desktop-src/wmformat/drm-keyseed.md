---
title: DRM_KeySeed
description: La proprietà DRM KeySeed contiene il valore di seed della chiave che verrà usato insieme a \_ KeyID per creare la chiave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed windows Media Format
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46766dc5754bde33c00af250f03a54caf3c12c607ec14da858ac638a70f79baf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658971"
---
# <a name="drm_keyseed"></a>DRM \_ KeySeed

La **proprietà DRM \_ KeySeed** contiene il valore di seed della chiave che verrà usato insieme a KeyID per creare la chiave.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ KeySeed

## <a name="data-type"></a>Tipo di dati

**STRINGA DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata [**usando IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Non è accessibile dall'oggetto reader.

Un valore di base della chiave viene in genere usato per proteggere più file o set di file, ad esempio tutti i file emessi da un server licenze o forse tutti i file di un determinato artista. KeyID, tuttavia, è univoco per ogni file.

Il valore di seed della chiave deve rimanere un segreto condiviso solo tra l'autore del contenuto e il distributore di licenze. Questo valore non viene archiviato nell'intestazione DRM e non è necessario né accessibile alle applicazioni lettore DRM.

È possibile generare un nuovo valore di seed della chiave usando il metodo [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) o con qualsiasi altro metodo appropriato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




