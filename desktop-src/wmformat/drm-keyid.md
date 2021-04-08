---
title: DRM_KeyID
description: L' \_ attributo keyId di DRM contiene l'identificatore di chiave.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046340"
---
# <a name="drm_keyid"></a>\_KEYID DRM

L' **attributo \_ keyId di DRM** contiene l'identificatore di chiave.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ keyId

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo per il contenuto DRM versione 7. Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Lo stesso attributo file può essere recuperato usando [**DRM \_ DRMHeader \_ keyId**](drm-drmheader-keyid.md).

L'ID chiave viene usato in combinazione con il valore di inizializzazione chiave per creare la chiave simmetrica usata per crittografare e decrittografare il file. L'applicazione Writer usa l'ID chiave per crittografare il file e quindi archivia l'ID chiave nell'intestazione del file. Quando un'applicazione lettore richiede una licenza per un file, il componente DRM invia l'ID chiave (insieme al resto dell'intestazione DRM) al server licenze. Il server licenze, che ha il valore di inizializzazione chiave privata, lo usa e l'ID chiave per creare una chiave per il file, che viene quindi inserita in una licenza insieme ai vari diritti che verranno applicati al file.

In genere, un valore di inizializzazione chiave viene utilizzato con molti ID chiave. Il valore di inizializzazione chiave è un segreto condiviso solo dall'autore del contenuto e dal server di distribuzione delle licenze. L'ID chiave viene usato dalle applicazioni client DRM e viene archiviato nell'intestazione DRM in chiaro.

Questo attributo è identico a quello di [**DRM \_ DRMHeader \_ keyId**](drm-drmheader-keyid.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




