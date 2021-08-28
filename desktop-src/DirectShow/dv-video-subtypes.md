---
description: Per il video DV sono definiti diversi sottotipi. Ognuno ha un codice FOURCC e un valore GUID corrispondente. Non tutti questi formati sono supportati. Per altre informazioni, vedere la sezione Osservazioni.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Sottotipi video DV (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ee08bad5970d016ada2bf129132bf34261be9ba856071d9f90f1e73de91978
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102951"
---
# <a name="dv-video-subtypes"></a>Sottotipi video DV

Per il video DV sono definiti diversi sottotipi. Ognuno ha un codice FOURCC e un valore GUID corrispondente. Non tutti questi formati sono supportati. Per altre informazioni, vedere la sezione Osservazioni.

## <a name="consumer-formats"></a>Formati consumer



| FOURCC | GUID               | Velocità dati | Descrizione                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | MEDIASUBTYPE \_ dvsl | 12,5 Mbps | SD-DVCR (525-60 o 625-50)   |
| 'dvsd' | MEDIASUBTYPE \_ dvsd | 25 Mbps   | SDL-DVCR (525-60 o 625-50)  |
| 'dvhd' | MEDIASUBTYPE \_ dvhd | 50 Mbps   | HD-DVCR (1125-60 o 1250-50) |



 

Per altre informazioni su questi formati, vedere IEC-61834.

## <a name="professional-formats"></a>Professional Formati



| FOURCC | GUID               | Velocità dati | Descrizione                                 |
|--------|--------------------|-----------|---------------------------------------------|
| 'dv25' | MEDIASUBTYPE \_ dv25 | 25 Mbps   | DVCPRO 25 (525-60 o 625-50).               |
| 'dv50' | MEDIASUBTYPE \_ dv50 | 50 Mbps   | DVCPRO 50 (525-60 o 625-50)                |
| 'dvh1' | MEDIASUBTYPE \_ dvh1 | 100 Mbps  | DVCPRO 100 (1080/60i, 1080/50i o 720/60P) |



 

Per altre informazioni su dv25 e dv50 e SMPTE 370M, vedere SMPTE 314M.

## <a name="miscellaneous"></a>Varie

Nel file di intestazione Uuids.h sono definiti due sottotipi DV aggiuntivi. Questi corrispondono ai codici FOURCC prodotti da determinati codec DV; non corrispondono ad alcun standard DV definito. Questi sottotipi sono obsoleti e non devono essere usati.



| FOURCC | GUID               |
|--------|--------------------|
| 'DVCS' | MEDIASUBTYPE \_ DVCS |
| 'DVSD' | MEDIASUBTYPE \_ DVSD |



 

## <a name="remarks"></a>Commenti

La tabella seguente illustra le velocità dei dati supportate, in megabit al secondo (Mbps), per i driver MSDV e UVC.



| Sistema operativo                                                                 | MSDV (IEEE 1394) Driver | UVC Driver    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 o versione precedente                                             | 12.5, 25                | Non disponibile |
| Windows XP Service Pack 2 o versione successiva, Windows Server 2003 Service Pack 1 o versione successiva. | 12.5, 25, 50, 100       | 12.5, 25      |



 

Per i flussi a 25 Mbps, il comportamento del driver MSDV è cambiato in Windows Vista prima di Windows Vista, il driver MSDV imposta sempre il tipo di supporto su MEDIASUBTYPE dvsd per flussi da 25 Mbps, indipendentemente dal fatto che l'origine sia \_ SDL-DVCR o DVCPRO 25. Il tipo di supporto 'dv25' non è stato usato. A partire Windows Vista, il driver MSDV ora distingue tra questi due formati. Per SDL-DVCR continua a usare il sottotipo 'dvsd'. Per DVCPRO 25, usa ora il sottotipo 'dv25'.

I DirectShow [DV Splitter](dv-splitter-filter.md) e [DV Video Decoder](dv-video-decoder-filter.md) supportano solo i formati SDL-DVCR. I dati possono essere PAL o NTSC. È possibile che siano disponibili filtri o codec di terze parti in grado di analizzare altri formati DV, purché la velocità dei dati sia supportata dal driver MSDV o UVC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[MSDV Driver](msdv-driver.md)
</dt> <dt>

[Sottotipi video](video-subtypes.md)
</dt> </dl>

 

 




