---
title: Stili del controllo Animation (CommCtrl. h)
description: Questa sezione elenca gli stili della finestra usati con i controlli di animazione.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327604"
---
# <a name="animation-control-styles"></a>Stili del controllo di animazione

Questa sezione elenca gli stili della finestra usati con i controlli di animazione.



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
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <dt><strong>ACS_AUTOPLAY</strong></dt> </dl></td>
<td style="text-align: left;">Avvia la riproduzione dell'animazione non appena viene aperto il clip AVI. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <dt><strong>ACS_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centra l'animazione nella finestra del controllo dell'animazione. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <dt><strong>ACS_TIMER</strong></dt> </dl></td>
<td style="text-align: left;">Per impostazione predefinita, il controllo Crea un thread per riprodurre il clip AVI. Se si imposta questo flag, il controllo riproduce il clip senza creare un thread. internamente il controllo Usa un timer Win32 per sincronizzare la riproduzione. <br/> <strong>Comctl32.dll versione 6 e successive:</strong> Questo stile non è supportato. Per impostazione predefinita, il controllo riproduce il clip AVI senza creare un thread.<br/>
<blockquote>
[!Note]<br />
Comctl32.dll versione 6 non è ridistribuibile. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <dt><strong>ACS_TRANSPARENT</strong></dt> </dl></td>
<td style="text-align: left;">Consente di associare il colore di sfondo di un'animazione a quello della finestra sottostante, creando uno &quot; &quot; sfondo trasparente. L'elemento padre del controllo animazione non deve avere lo stile WS_CLIPCHILDREN (vedere <a href="/windows/desktop/winmsg/window-styles">stili della finestra</a>). Il controllo Invia un messaggio di <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> al relativo elemento padre. Usare <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> per impostare il colore di sfondo per il contesto di dispositivo su un valore appropriato. Il controllo interpreta il pixel superiore sinistro del primo fotogramma come colore di sfondo predefinito dell'animazione. Verrà rimappato tutti i pixel con tale colore al valore fornito in risposta a WM_CTLCOLORSTATIC. <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



