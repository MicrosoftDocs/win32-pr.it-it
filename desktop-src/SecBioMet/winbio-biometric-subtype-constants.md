---
title: WINBIO_BIOMETRIC_SUBTYPE costanti (Winbio \_ types.h)
description: Fornire informazioni su una misurazione biometrica.
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
ms.openlocfilehash: 07e6dc285e1a19fab8e0363391fbd81429e931cd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630840"
---
# <a name="winbio_biometric_subtype-constants"></a>Costanti \_ SUBTYPE BIOMETRIC \_ WINBIO

**WINBIO \_ Le \_ costanti BIOMETRIC SUBTYPE** vengono usate in tutto il Windows Biometric Framework per fornire informazioni aggiuntive su una misurazione biometrica. Le costanti seguenti possono essere usate quando non è richiesto alcun sottotipo o quando è necessario un sottotipo.



| Costante/valore                                                                                                                                                                                                                                                            | Descrizione                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ SUBTYPE \_ NO \_ INFORMATION**</dt> <dt>0x00</dt> </dl> | Nessuna informazione sul sottotipo.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ SUBTYPE \_ ANY**</dt> <dt>0xFF</dt> </dl>                                   | Qualsiasi sottotipo.<br/>            |



## <a name="remarks"></a>Commenti

Per trovare i sottotipi biometrici disponibili per un particolare tipo biometrico, usare la tabella seguente:



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> valore</th>
<th>Argomenti per trovare i <strong>valori WINBIO_BIOMETRIC_SUBTYPE</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE costanti</strong></a>
<blockquote>
[!Note]<br />
Questi valori si applicano solo per Windows 10 e versioni successive.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>Uno degli argomenti seguenti:
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT costanti</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG costanti</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ costanti</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>costanti WINBIO_ANSI_381_IMP_TYPE</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS costanti</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS costanti di impronta digitale</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm costanti</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS costanti</strong></a>
<blockquote>
[!Note]<br />
Questi valori si applicano solo per Windows 10 e versioni successive.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>costanti WINBIO_VOICE</strong></a>
<blockquote>
[!Note]<br />
Questi valori si applicano solo per Windows 10 e versioni successive.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Per altre informazioni, vedere [Costanti dell'applicazione client.](client-application-constants.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



 

 





