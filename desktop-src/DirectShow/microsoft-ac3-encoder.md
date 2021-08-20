---
description: Il filtro Microsoft AC-3 Encoder codifica l'audio PCM stereo in un flusso di bit Dolby Digital.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Codificatore Microsoft AC-3 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35984975fc5a56b043f1b2ceda56505ee6fe74038034fb35deb09b6a5f6a0f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153169"
---
# <a name="microsoft-ac-3-encoder"></a>Codificatore Microsoft AC-3

Il filtro Microsoft AC-3 Encoder codifica l'audio PCM stereo in un flusso di bit Dolby Digital.

> [!Note]  
> L'implementazione Microsoft della tecnologia Dolby Digital è limitata alle condizioni del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.

 

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 



Filtrare le informazioni

Interfacce di filtro

[**Filtro IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Tipi di supporti pin di input

**MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ PCM**<br/> Il tipo di input deve essere stereo a 48 kHz, 16 bit per campione.<br/>

Interfacce pin di input

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

**MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/> **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/>

Interfacce pin di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID del filtro

**CLSID \_ CMSAC3Enc** (dichiarato in wmcodecdsp.h)

File eseguibile

msac3enc.dll

[Merito](merit.md)

**NON \_ \_ USARE \_**

[Categoria filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Commenti

Questo filtro non è disponibile per l'uso da parte di applicazioni di terze parti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




