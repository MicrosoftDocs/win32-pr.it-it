---
description: Specifica un elenco di velocità in bit e finestre del buffer corrispondenti per un file ASF (Advanced Systems Format) VBR (Variable Bit Rate).
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9444292ad437551622e1f418a6f21198ecd8341f01e4e5bda0a2047f847cfd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740749"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a>Attributo MF \_ PD \_ ASF \_ METADATA \_ LEAKY \_ BUCKET \_ PAIRS

Specifica un elenco di velocità in bit e finestre del buffer corrispondenti per un file ASF (Advanced Systems Format) VBR (Variable Bit Rate).

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto di ASF.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo che si applica al descrittore di presentazione per il contenuto asf.

Il valore dell'attributo ha il formato seguente:

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

La **struttura WM \_ LEAKY BUCKET \_ \_ PAIR** è definita come segue:

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

Per ogni velocità in bit, il **membro msBufferWindow** indica la quantità di contenuto memorizzata nel buffer prima dell'inizio della riproduzione, in millisecondi. La dimensione del buffer in byte è uguale **a msBufferWinow** x **dwBitrate** / 8000.

> [!Note]  
> Questo attributo corrisponde **all'attributo ASFLeakyBucketPairs** in Windows Media Format SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto Intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




