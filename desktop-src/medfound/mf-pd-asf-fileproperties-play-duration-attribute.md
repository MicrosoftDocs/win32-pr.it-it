---
description: Specifica il tempo necessario per riprodurre un file ASF (Advanced Systems Format), in unità da 100 nanosecondi.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0e4609f70fa96a0e08339e496b1d7ed6ac7004108ec56ff870ed6f4e7fcb6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104347"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a>Attributo MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PLAY \_ DURATION

Specifica il tempo necessario per riprodurre un file ASF (Advanced Systems Format), in unità da 100 nanosecondi.

Questo valore include il tempo di pre-registrazione. Per recuperare la durata effettiva della riproduzione, ottenere il valore [**dell'attributo \_ MF PD \_ DURATION.**](mf-pd-duration-attribute.md) Tuttavia, se il valore di preroll è maggiore della durata di riproduzione, il valore di **MF \_ PD \_ DURATION** è zero.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto asf.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.

## <a name="examples"></a>Esempio


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




