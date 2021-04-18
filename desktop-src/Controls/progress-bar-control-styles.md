---
title: Stili del controllo indicatore di stato (CommCtrl. h)
description: Gli stili di controllo seguenti sono supportati dai controlli indicatore di stato
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327859"
---
# <a name="progress-bar-control-styles"></a>Stili del controllo indicatore di stato

Gli stili di controllo seguenti sono supportati dai controlli [indicatore di stato](progress-bar-control.md) :



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
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <dt><strong>PBS_MARQUEE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 6,0</a> o successiva. L'indicatore di stato non aumenta di dimensione ma si sposta ripetutamente lungo la lunghezza della barra, indicando l'attività senza specificare quale percentuale dello stato di avanzamento è completa. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll versione 6 non è ridistribuibile ma è incluso in Windows o versioni successive. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <dt><strong>PBS_SMOOTH</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 4,70</a> o successiva. L'indicatore di stato Visualizza lo stato di avanzamento in una barra di scorrimento uniforme anziché nella barra segmentata predefinita. <br/>
<blockquote>
[!Note]<br />
Questo stile è supportato solo nel tema classico di Windows. Tutti gli altri temi eseguono l'override di questo stile.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <dt><strong>PBS_SMOOTHREVERSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 6,0</a> o successiva e <strong>Windows Vista.</strong> Determina il comportamento dell'animazione che l'indicatore di stato deve usare quando si esegue lo scorrimento indietro (da un valore più elevato a un valore più basso). Se è impostato, si verificherà &quot; una &quot; transizione uniforme, in caso contrario il controllo passerà &quot; &quot; al valore più basso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <dt><strong>PBS_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 4,70</a> o successiva. L'indicatore di stato Visualizza lo stato di avanzamento verticalmente, dal basso verso l'alto.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

È possibile impostare gli stili dell'indicatore di stato, nello stesso modo degli altri controlli comuni, con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

