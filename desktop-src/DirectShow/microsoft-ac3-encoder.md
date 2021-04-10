---
description: Il filtro del codificatore Microsoft AC-3 codifica l'audio PCM stereo in un bitstream Digital bitstream.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Microsoft AC-3 encoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124518"
---
# <a name="microsoft-ac-3-encoder"></a>Codificatore Microsoft AC-3

Il filtro del codificatore Microsoft AC-3 codifica l'audio PCM stereo in un bitstream Digital bitstream.

> [!Note]  
> L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.

 

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 



Informazioni sul filtro

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Tipi di supporti pin di input

**MEDIATYPE \_ Audio**, **\_ PCM MEDIASUBTYPE**<br/> Il tipo di input deve essere stereo a 48 kHz, a 16 bit per campione.<br/>

Interfacce pin di input

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/>

Interfacce del PIN di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID filtro

**CLSID \_ CMSAC3Enc** (dichiarata in wmcodecdsp. h)

File eseguibile

msac3enc.dll

[Merito](merit.md)

**il merito non viene \_ \_ \_ utilizzato**

[Categoria filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Commenti

Questo filtro non è disponibile per l'uso da parte di applicazioni di terze parti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




