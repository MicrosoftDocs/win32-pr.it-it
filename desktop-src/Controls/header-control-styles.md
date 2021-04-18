---
title: Stili del controllo intestazione (CommCtrl. h)
description: I controlli Header hanno diversi stili, descritti in questa sezione, che determinano l'aspetto e il comportamento del controllo. È possibile impostare gli stili iniziali durante la creazione del controllo intestazione.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327241"
---
# <a name="header-control-styles"></a>Stili del controllo intestazione

I controlli Header hanno diversi stili, descritti in questa sezione, che determinano l'aspetto e il comportamento del controllo. È possibile impostare gli stili iniziali durante la creazione del controllo intestazione.



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
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <dt><strong>HDS_BUTTONS</strong></dt> </dl></td>
<td style="text-align: left;">Ogni elemento nel controllo appare e si comporta come un pulsante di push. Questo stile è utile se un'applicazione esegue un'attività quando l'utente fa clic su un elemento nel controllo intestazione. Ad esempio, un'applicazione può ordinare le informazioni nelle colonne in modo diverso a seconda dell'elemento selezionato dall'utente. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <dt><strong>HDS_DRAGDROP</strong></dt> </dl></td>
<td style="text-align: left;">Consente il riordinamento del trascinamento della selezione degli elementi di intestazione. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <dt><strong>HDS_FILTERBAR</strong></dt> </dl></td>
<td style="text-align: left;">Includere una barra dei filtri come parte del controllo intestazione standard. Questa barra consente agli utenti di applicare comodamente un filtro alla visualizzazione. Le chiamate a <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> produrranno nuove dimensioni per il controllo e comporteranno l'aggiornamento della visualizzazione elenco. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <dt><strong>HDS_FLAT</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 6,0 e successive</a>. Determina il disegno del controllo intestazione come flat quando il sistema operativo è in esecuzione in modalità classica. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll versione 6 non è ridistribuibile ma è incluso in Windows. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <dt><strong>HDS_FULLDRAG</strong></dt> </dl></td>
<td style="text-align: left;">Consente al controllo intestazione di visualizzare il contenuto della colonna anche quando l'utente ridimensiona una colonna. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <dt><strong>HDS_HIDDEN</strong></dt> </dl></td>
<td style="text-align: left;">Indica un controllo intestazione che deve essere nascosto. Questo stile non nasconde il controllo. Al contrario, quando si invia il messaggio di <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> a un controllo intestazione con lo stile HDS_HIDDEN, il controllo restituisce zero nel membro <strong>CY</strong> della struttura <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> . Il controllo viene quindi nascosto impostando l'altezza su zero. Questa operazione può essere utile quando si desidera utilizzare il controllo come contenitore di informazioni anziché come controllo visivo. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <dt><strong>HDS_HORZ</strong></dt> </dl></td>
<td style="text-align: left;">Crea un controllo intestazione con orientamento orizzontale. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <dt><strong>HDS_HOTTRACK</strong></dt> </dl></td>
<td style="text-align: left;">Abilita il rilevamento a caldo. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <dt><strong>HDS_CHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 6,00 e successive</a>. Consente l'inserimento di caselle di controllo sugli elementi di intestazione. Per ulteriori informazioni, vedere il membro <strong>FMT</strong> di <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <dt><strong>HDS_NOSIZING</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 6,00 e successive</a>. L'utente non può trascinare il divisore sul controllo intestazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <dt><strong>HDS_OVERFLOW</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 6,00 e successive</a>. Quando non è possibile visualizzare tutti gli elementi all'interno del rettangolo del controllo intestazione, viene visualizzato un pulsante. Quando si fa clic su questo pulsante, viene inviato un <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notifica.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per recuperare e modificare gli stili dopo aver creato il controllo, usare le funzioni [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



