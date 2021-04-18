---
description: Questi flag specificano come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Flag di ridimensionamento (qedit. h)
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
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330781"
---
# <a name="resize-flags"></a>Ridimensiona flag

\[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

Questi flag specificano come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.



| Costante/valore                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**REsizef \_ ESTENSIONE**</dt> <dt>0</dt> </dl>                                                                          | L'immagine viene adattata in base alle dimensioni del frame di destinazione in entrambe le dimensioni, senza mantenere le proporzioni.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**REsizef \_ Ritaglio**</dt> <dt>1</dt> </dl>                                                                                   | L'immagine non viene ridimensionata. Se l'immagine è più piccola del frame di destinazione, l'area circostante è nera. Se l'immagine è più grande del frame di destinazione, l'immagine viene ritagliata.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**REsizef \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | L'immagine viene ridimensionata per adattarsi al frame di destinazione lungo una dimensione, mantenendo le proporzioni. Se il rapporto tra larghezza e altezza nell'immagine non corrisponde al rapporto nel frame di destinazione, viene creata una letterbox.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**REsizef \_ PRESERVEASPECTRATIO \_ noletterbox**</dt> <dt>3</dt> </dl> | L'immagine viene ridimensionata per riempire l'intero frame di destinazione mantenendo le proporzioni. Anziché creare una letterbox, questa modalità Ritaglia l'immagine, lungo i lati o nella parte superiore e inferiore.<br/>                 |



## <a name="remarks"></a>Commenti

Le immagini seguenti mostrano gli effetti di questi flag.

![Ridimensiona flag](images/stretch14.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimelineSrc::GetStretchMode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




