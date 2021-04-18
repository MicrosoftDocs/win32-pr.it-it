---
title: DRM_KeySeed
description: La \_ proprietà chiave di inizializzazione DRM contiene il valore di inizializzazione chiave che verrà usato insieme a keyId per creare la chiave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299445"
---
# <a name="drm_keyseed"></a>Valore di inizializzazione del valore DRM \_

La proprietà chiave di **\_ inizializzazione DRM** contiene il valore di inizializzazione chiave che verrà usato insieme a keyId per creare la chiave.

## <a name="global-constant"></a>Costante globale

valore \_ di \_ inizializzazione g wszWMDRM

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata utilizzando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Non è accessibile dall'oggetto Reader.

Un valore di inizializzazione chiave viene in genere usato per proteggere più file o set di file, ad esempio tutti i file emessi da un server licenze o forse tutti i file di un particolare artista. KeyID, tuttavia, è univoco per ogni file.

Il valore di inizializzazione chiave deve rimanere un segreto condiviso solo tra l'autore del contenuto e il server di distribuzione delle licenze. Questo valore non è archiviato nell'intestazione DRM e non è né necessario né accessibile per le applicazioni DRM Player.

Un nuovo valore di inizializzazione chiave può essere generato usando il metodo [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) o qualsiasi altro mezzo appropriato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




