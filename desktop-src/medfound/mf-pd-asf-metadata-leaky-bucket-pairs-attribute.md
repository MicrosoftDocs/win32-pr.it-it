---
description: Specifica un elenco di velocità in bit e finestre del buffer corrispondenti per un file di formato ASF (Advanced Systems rate) a velocità in bit variabile.
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: Attributo MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314547"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a>\_Attributo delle \_ \_ coppie di \_ \_ bucket \_ per i metadati di MF PD ASF

Specifica un elenco di velocità in bit e finestre del buffer corrispondenti per un file di formato ASF (Advanced Systems rate) a velocità in bit variabile.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo che si applica al descrittore di presentazione per il contenuto ASF.

Il valore dell'attributo ha il formato seguente:

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

La struttura delle coppie di bucket a perdita di WM è definita nel modo seguente: **\_ \_ \_**

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

Per ogni velocità in bit, il membro **msBufferWindow** indica la quantità di contenuto memorizzato nel buffer prima che inizi la riproduzione, in millisecondi. La dimensione del buffer in byte equivale a **msBufferWinow** x **dwBitrate** /8000.

> [!Note]  
> Questo attributo corrisponde all'attributo **ASFLeakyBucketPairs** in Windows Media Format SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




