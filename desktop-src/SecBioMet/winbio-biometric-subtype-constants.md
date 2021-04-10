---
title: Costanti WINBIO_BIOMETRIC_SUBTYPE (tipi WinBio \_ . h)
description: Fornire informazioni su una misura biometrica.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964442"
---
# <a name="winbio_biometric_subtype-constants"></a>\_Costanti SOTTOtipi BIOmetrici WINBIO \_

**WINBIO \_ Le costanti dei \_ SOTTOtipi BIOmetrici** vengono usate in tutta la Windows Biometric Framework per fornire informazioni aggiuntive su una misurazione biometrica. È possibile utilizzare le costanti seguenti quando non è richiesto alcun sottotipo o quando è necessario un sottotipo.



| Costante/valore                                                                                                                                                                                                                                                            | Descrizione                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ Sottotipo \_ senza \_ informazioni**</dt> <dt>0x00</dt> </dl> | Nessuna informazione sul sottotipo.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ Sottotipo \_ any**</dt> <dt>0xFF</dt> </dl>                                   | Qualsiasi sottotipo.<br/>            |



## <a name="remarks"></a>Commenti

Per trovare i sottotipi biometrici disponibili per un particolare tipo biometrico, usare la tabella seguente:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore <strong>WINBIO_BIOMETRIC_TYPE</strong></th>
<th>Argomenti per trovare i valori <strong>WINBIO_BIOMETRIC_SUBTYPE</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>Costanti WINBIO_ANSI_385_FACE</strong></a>
<blockquote>
[!Note]<br />
Questi valori si applicano solo a Windows 10 e versioni successive.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>Uno degli argomenti seguenti:
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>Costanti WINBIO_ANSI_381_FORMAT</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>Costanti WINBIO_ANSI_381_IMG</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>Costanti WINBIO_ANSI_381_IMG_ACQ</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>Costanti WINBIO_ANSI_381_IMP_TYPE</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>Costanti WINBIO_ANSI_381_PIXELS</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>Costanti impronta digitale WINBIO_ANSI_381_POS</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Costanti WINBIO_ANSI_381_POS_Palm</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>Costanti WINBIO_IRIS</strong></a>
<blockquote>
[!Note]<br />
Questi valori si applicano solo a Windows 10 e versioni successive.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Costanti WINBIO_VOICE</strong></a>
<blockquote>
[!Note]<br />
Questi valori si applicano solo a Windows 10 e versioni successive.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Per ulteriori informazioni, vedere [costanti dell'applicazione client](client-application-constants.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



 

 





