---
description: Specifica il tempo necessario per riprodurre un file con estensione ASF (Advanced Systems Format), in unità da 100 nanosecondi.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: Attributo MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967945"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a>\_ \_ \_ \_ Attributo Duration del gioco FileProperties ASF di MF PD \_

Specifica il tempo necessario per riprodurre un file con estensione ASF (Advanced Systems Format), in unità da 100 nanosecondi.

Questo valore include il tempo di preiscrizione. Per recuperare la durata effettiva della riproduzione, ottenere il valore dell'attributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) . Tuttavia, se il valore di preroll è maggiore della durata della riproduzione, il valore di **MF \_ PD \_ Duration** è zero.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




