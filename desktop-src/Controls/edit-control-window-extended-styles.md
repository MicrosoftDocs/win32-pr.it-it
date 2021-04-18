---
title: Modificare gli stili estesi del controllo (CommCtrl. h)
description: Questa sezione elenca gli stili estesi usati per la creazione di controlli di modifica. Il valore degli stili estesi è una combinazione bit per bit di questi stili.
ms.assetid: 44ef7cbf-6d90-4ea0-8e23-cd84aacd5506
topic_type:
- apiref
api_name:
- ES_EX_ALLOWEOL_CR
- ES_EX_ALLOWEOL_LF
- ES_EX_ALLOWEOL_ALL
- ES_EX_CONVERT_EOL_ON_PASTE
- ES_EX_ZOOMABLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 912a13b0e05d7b12e5058435221b821b50eddf2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327244"
---
# <a name="edit-control-extended-styles"></a>Modificare gli stili estesi del controllo

Questa sezione elenca gli stili estesi usati per la creazione di controlli di modifica. Il valore degli stili estesi è una combinazione bit per bit di questi stili.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl> <dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e versioni successive](common-control-versions.md). Abilita il supporto per i caratteri di fine riga (CR) di ritorno a capo per le linee di interruzioni.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl> <dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e versioni successive](common-control-versions.md). Abilita il supporto per i caratteri di fine riga di avanzamento riga (LF) per interrompere le righe.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl> <dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e versioni successive](common-control-versions.md). Abilita il supporto per i caratteri di fine riga (CR) e di avanzamento riga (LF) a capo per le righe.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl> <dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e versioni successive](common-control-versions.md). Converte i caratteri di fine riga abilitati per questo controllo di modifica nel contenuto incollato in modo che corrisponda al carattere di fine riga utilizzato dal documento corrente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl> <dt><strong>ES_EX_ZOOMABLE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e versioni successive](common-control-versions.md). Abilita lo zoom usando Ctrl + MouseWheel [**e i messaggi di zoom \_**](em-getzoom.md)em getzoom / [**\_ em**](em-setzoom.md) .<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





