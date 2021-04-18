---
title: Stili estesi barra degli strumenti (CommCtrl. h)
description: Questa sezione elenca gli stili estesi supportati dai controlli della barra degli strumenti.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326844"
---
# <a name="toolbar-extended-styles"></a>Stili estesi della barra degli strumenti

Questa sezione elenca gli stili estesi supportati dai controlli della barra degli strumenti.



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
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 4,71</a>. Questo stile consente ai pulsanti di avere una freccia a discesa separata. I pulsanti con lo stile <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> verranno disegnati con una freccia a discesa in una sezione separata, a destra del pulsante. Se si fa clic sulla freccia, solo la parte freccia del pulsante verrà deselezionata e il controllo Toolbar invierà un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> codice di notifica per richiedere all'applicazione di visualizzare il menu a discesa. Se si fa clic sulla parte principale del pulsante, il controllo Toolbar invia un messaggio di WM_COMMAND con l'ID del pulsante. L'applicazione risponde normalmente avviando il primo comando nel menu.<br/> In molti casi è possibile che si desideri disporre solo di alcuni pulsanti a discesa su una barra degli strumenti con frecce separate. A tale scopo, impostare il TBSTYLE_EX_DRAWDDARROWS stile esteso. Assegnare a questi pulsanti le frecce separate dallo stile <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> . Ai pulsanti con questo stile sarà visualizzata una freccia accanto all'immagine. Tuttavia, la freccia non sarà separata e quando si fa clic su una parte del pulsante, il controllo Toolbar invierà un codice di notifica <a href="tbn-dropdown.md">TBN_DROPDOWN</a> . Per evitare problemi di ridisegno, questo stile deve essere impostato prima che il controllo Toolbar diventi visibile.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 5,81</a>. Questo stile nasconde i pulsanti parzialmente ritagliati. L'uso più comune di questo stile è per le barre degli strumenti che fanno parte di un controllo Rebar. Se una banda adiacente copre parte di un pulsante, il pulsante non verrà visualizzato. Tuttavia, se la banda del controllo Rebar ha lo stile <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , il pulsante verrà visualizzato nel menu a discesa della freccia di espansione. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 6</a>. Questo stile richiede il doppio buffer della barra degli strumenti. Il doppio buffering è un meccanismo che rileva quando la barra degli strumenti è stata modificata. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll versione 6 non è ridistribuibile ma è incluso in Windows o versioni successive. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 5,81</a>. Questo stile consente di impostare il testo per tutti i pulsanti, ma di visualizzarlo solo per i pulsanti con lo stile del pulsante <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> . È necessario impostare anche lo stile del <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> . In genere, quando un pulsante non Visualizza il testo, l'applicazione deve gestire <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> o <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> per visualizzare una descrizione comando. Con il TBSTYLE_EX_MIXEDBUTTONS stile esteso, il testo impostato ma non visualizzato in un pulsante verrà usato automaticamente come testo della descrizione comando del pulsante. L'applicazione deve gestire solo TBN_GETINFOTIP o o TTN_GETDISPINFO se è necessaria una maggiore flessibilità nella specifica del testo della descrizione comando. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 5,82</a>. <strong>Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</strong> Questo stile assegna alla barra degli strumenti un orientamento verticale e organizza i pulsanti della barra degli strumenti in colonne. I pulsanti scorrono verticalmente fino a quando un pulsante non ha superato l'altezza di delimitazione della barra degli strumenti (vedere <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) e quindi viene creata una nuova colonna. La barra degli strumenti scorre i pulsanti in questo modo finché non vengono posizionati tutti i pulsanti. Per utilizzare questo stile, è necessario impostare anche lo stile del TBSTYLE_EX_VERTICAL. <br/>
<blockquote>
[!Note]<br />
Questo stile potrebbe non essere supportato nelle versioni future di Comctl32.dll. Questo stile, inoltre, non è definito in commctrl. h. Aggiungere la definizione seguente ai file di origine dell'applicazione per usare questo stile: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versione 5,82</a>. <strong>Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</strong> Questo stile fornisce un orientamento verticale alla barra degli strumenti. I pulsanti della barra degli strumenti scorrono dall'alto verso il basso anziché orizzontalmente. <br/>
<blockquote>
[!Note]<br />
Questo stile potrebbe non essere supportato nelle versioni future di Comctl32.dll. Questo stile, inoltre, non è definito in commctrl. h. Aggiungere la definizione seguente ai file di origine dell'applicazione per usare questo stile: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per impostare uno stile esteso, inviare il controllo barra degli strumenti di un messaggio [**\_ SETEXTENDEDSTYLE TB**](tb-setextendedstyle.md) . Per determinare gli stili estesi attualmente impostati, inviare un messaggio [**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





