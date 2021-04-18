---
description: Per il video DV sono definiti diversi sottotipi. Ogni ha un codice FOURCC e un valore GUID corrispondente. Non tutti questi formati sono supportati. Per ulteriori informazioni, vedere la sezione Osservazioni.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Sottotipi video DV (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330828"
---
# <a name="dv-video-subtypes"></a>Sottotipi video DV

Per il video DV sono definiti diversi sottotipi. Ogni ha un codice FOURCC e un valore GUID corrispondente. Non tutti questi formati sono supportati. Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="consumer-formats"></a>Formati utente



| FOURCC | GUID               | Velocità dati | Descrizione                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | \_DVSL MEDIASUBTYPE | 12,5 Mbps | SD-DVCR (525-60 o 625-50)   |
| DVSD | \_DVSD MEDIASUBTYPE | 25 Mbps   | SDL-DVCR (525-60 o 625-50)  |
| 'dvhd' | \_DVHD MEDIASUBTYPE | 50 Mbps   | HD-DVCR (1125-60 o 1250-50) |



 

Per ulteriori informazioni su questi formati, vedere IEC-61834.

## <a name="professional-formats"></a>Formati professionali



| FOURCC | GUID               | Velocità dati | Descrizione                                 |
|--------|--------------------|-----------|---------------------------------------------|
| DV25 | \_DV25 MEDIASUBTYPE | 25 Mbps   | DVCPRO 25 (525-60 o 625-50).               |
| DV50 | \_DV50 MEDIASUBTYPE | 50 Mbps   | DVCPRO 50 (525-60 o 625-50)                |
| 'dvh1' | \_DVH1 MEDIASUBTYPE | 100 Mbps  | DVCPRO 100 (1080/60i, 1080/50i o 720/60P) |



 

Per ulteriori informazioni su dvh1, vedere SMPTE 314M per ulteriori informazioni su DV25 e DV50 e SMPTE 370M.

## <a name="miscellaneous"></a>Varie

Nel file di intestazione UUIDs. h sono definiti due sottotipi DV aggiuntivi. Questi corrispondono ai codici FOURCC prodotti da determinati codec DV; non corrispondono ad alcun standard DV definito. Questi sottotipi sono obsoleti e non devono essere usati.



| FOURCC | GUID               |
|--------|--------------------|
| DVCS | \_DVCS MEDIASUBTYPE |
| DVSD | \_DVSD MEDIASUBTYPE |



 

## <a name="remarks"></a>Commenti

La tabella seguente mostra le frequenze dati supportate, in megabit al secondo (Mbps), per i driver MSDV e UVC.



| Sistema operativo                                                                 | Driver MSDV (IEEE 1394) | Driver UVC    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 o versioni precedenti                                             | 12,5, 25                | Non disponibile |
| Windows XP Service Pack 2 o versione successiva, Windows Server 2003 Service Pack 1 o versione successiva. | 12,5, 25, 50, 100       | 12,5, 25      |



 

Per i flussi a 25 Mbps, il comportamento del driver MSDV è stato modificato in Windows Vista prima di Windows Vista, il driver MSDV imposta sempre il tipo di supporto su MEDIASUBTYPE \_ DVSD per i flussi a 25 Mbps, indipendentemente dal fatto che l'origine sia SDL-DVCR o DVCPRO 25. Il tipo di supporto ' DV25' non è stato usato. A partire da Windows Vista, il driver MSDV ora distingue tra questi due formati. Per SDL-DVCR, continua a usare il sottotipo ' DVSD '. Per DVCPRO 25 USA ora il sottotipo ' DV25'.

I filtri di [decodificatore](dv-video-decoder-filter.md) DirectShow [DV](dv-splitter-filter.md) e DV video supportano solo i formati SDL-DVCR. I dati possono essere PAL o NTSC. È possibile che siano disponibili filtri o codec di terze parti in grado di analizzare altri formati DV, purché la velocità dati sia supportata dal driver MSDV o UVC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Driver MSDV](msdv-driver.md)
</dt> <dt>

[Sottotipi video](video-subtypes.md)
</dt> </dl>

 

 




