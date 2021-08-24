---
description: Questi flag specificano il modo in cui viene eseguito il rendering di un'origine video se le dimensioni non corrispondono alle dimensioni di output.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Flag di ridimensionamento (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: c38f4b1913eb7676832374e57e4d65e14dc87831c13f3cdb0de96edf9b83ebec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747107"
---
# <a name="resize-flags"></a>Flag di ridimensionamento

\[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

Questi flag specificano il modo in cui viene eseguito il rendering di un'origine video se le dimensioni non corrispondono alle dimensioni di output.



| Costante/valore                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt> </dl>                                                                          | L'immagine viene estesa in modo da adattarla alle dimensioni del frame di destinazione in entrambe le dimensioni, senza mantenere le proporzioni.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**RESIZEF \_ RITAGLIO**</dt> <dt>1</dt> </dl>                                                                                   | L'immagine non viene ridimensionata. Se l'immagine è più piccola del frame di destinazione, l'area circostante è nera. Se l'immagine è più grande del frame di destinazione, l'immagine viene ritagliata.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | L'immagine viene ridimensionata per adattarla al frame di destinazione lungo una dimensione, mantenendo le proporzioni. Se il rapporto tra larghezza e altezza nell'immagine non corrisponde al rapporto nel frame di destinazione, viene creata una casella di lettere.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt> </dl> | L'immagine viene ridimensionata per riempire l'intero frame di destinazione mantenendo le proporzioni. Invece di creare una casella di lettere, questa modalità ritaglia l'immagine, lungo i lati o nella parte superiore e inferiore.<br/>                 |



## <a name="remarks"></a>Commenti

Le immagini seguenti mostrano gli effetti di questi flag.

![flag di ridimensionamento](images/stretch14.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimelineSrc::GetStretchMode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




