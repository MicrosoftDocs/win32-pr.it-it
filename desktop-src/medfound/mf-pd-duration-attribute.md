---
description: Specifica la durata di una presentazione, in unità di 100 nanosecondi.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: Attributo MF_PD_DURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314540"
---
# <a name="mf_pd_duration-attribute"></a>\_ \_ Attributo durata MF PD

Specifica la durata di una presentazione, in unità di 100 nanosecondi.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come valore **LONGLONG** .

## <a name="remarks"></a>Commenti

Le origini supporto possono impostare questo attributo su un descrittore di presentazione per indicare la durata della presentazione.

Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**. Tuttavia, l'attributo non deve mai contenere un valore negativo.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come ottenere la durata della presentazione da un'origine multimediale.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




