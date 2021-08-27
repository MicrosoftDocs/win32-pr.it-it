---
title: Stili estesi della barra degli strumenti (CommCtrl.h)
description: Questa sezione elenca gli stili estesi supportati dai controlli barra degli strumenti.
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
ms.openlocfilehash: 71e242426269d4049b913a41910d325c360886f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476783"
---
# <a name="toolbar-extended-styles"></a>Stili estesi della barra degli strumenti

Questa sezione elenca gli stili estesi supportati dai controlli barra degli strumenti.




| Costante | Descrizione | 
|----------|-------------|
| <span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt></dl> | <a href="common-control-versions.md">Versione 4.71</a>. Questo stile consente ai pulsanti di avere una freccia a discesa separata. I pulsanti con <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> stile personalizzato verranno disegnati con una freccia a discesa in una sezione separata, a destra del pulsante. Se si fa clic sulla <a href="tbn-dropdown.md">freccia,</a> solo la parte della freccia del pulsante sarà deprimente e il controllo barra degli strumenti invierà un codice di notifica TBN_DROPDOWN per richiedere all'applicazione di visualizzare il menu a discesa. Se si fa clic sulla parte principale del pulsante, il controllo barra degli strumenti invia WM_COMMAND messaggio con l'ID del pulsante. L'applicazione risponde in genere avviando il primo comando nel menu.<br /> Esistono molte situazioni in cui può essere necessario avere solo alcuni pulsanti a discesa su una barra degli strumenti con frecce separate. A tale scopo, impostare lo stile TBSTYLE_EX_DRAWDDARROWS esteso. Assegnare a questi pulsanti che non avranno frecce separate BTNS_WHOLEDROPDOWN <a href="toolbar-control-and-button-styles.md"><strong>stile.</strong></a> I pulsanti con questo stile avranno una freccia visualizzata accanto all'immagine. Tuttavia, la freccia non sarà separata e quando viene fatto clic su qualsiasi parte del pulsante, il controllo barra degli strumenti invierà un TBN_DROPDOWN <a href="tbn-dropdown.md">di</a> notifica. Per evitare problemi di ridisegno, questo stile deve essere impostato prima che il controllo barra degli strumenti diventi visibile.<br /> | 
| <span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Versione 5.81</a>. Questo stile nasconde i pulsanti parzialmente ritagliati. L'uso più comune di questo stile è per le barre degli strumenti che fanno parte di un controllo rebar. Se una banda adiacente copre parte di un pulsante, il pulsante non verrà visualizzato. Tuttavia, se la banda <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong></strong></a> rebar ha lo stile RBBS_USECHEVRON, il pulsante verrà visualizzato nel menu a discesa della freccia di sospensione. <br /> | 
| <span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Versione 6</a>. Questo stile richiede che la barra degli strumenti sia memorizzata nel doppio buffer. Il doppio buffering è un meccanismo che rileva quando la barra degli strumenti è stata modificata. <br /><blockquote>[!Note]<br />Comctl32.dll versione 6 non è ridistribuibile, ma è incluso in Windows o versioni successive. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</blockquote><br /> | 
| <span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Versione 5.81</a>. Questo stile consente di impostare il testo per tutti i pulsanti, ma di visualizzarlo solo per i pulsanti con lo <a href="toolbar-control-and-button-styles.md"><strong>stile</strong></a> BTNS_SHOWTEXT pulsante. È <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> deve essere impostato anche lo stile di configurazione. In genere, quando un pulsante non visualizza testo, l'applicazione deve gestire TBN_GETINFOTIP <a href="tbn-getinfotip.md">o</a> <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> visualizzare una descrizione comando. Con lo TBSTYLE_EX_MIXEDBUTTONS stile esteso, il testo impostato ma non visualizzato in un pulsante verrà usato automaticamente come testo della descrizione comando del pulsante. L'applicazione deve gestire solo TBN_GETINFOTIP o TTN_GETDISPINFO se è necessaria una maggiore flessibilità per specificare il testo della descrizione comando. <br /> | 
| <span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt></dl> | <a href="common-control-versions.md">Versione 5.82</a>. <strong>Destinato all'uso interno; non consigliato per l'uso nelle applicazioni.</strong> Questo stile offre alla barra degli strumenti un orientamento verticale e organizza i pulsanti della barra degli strumenti in colonne. I pulsanti scorrono verso il basso verticalmente fino a quando un pulsante non supera l'altezza di delimitazione della barra degli strumenti (vedere <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) e quindi viene creata una nuova colonna. La barra degli strumenti scorre i pulsanti in questo modo fino a quando non vengono posizionati tutti i pulsanti. Per usare questo stile, è TBSTYLE_EX_VERTICAL deve essere impostato anche lo stile predefinito. <br /><blockquote>[!Note]<br />Questo stile potrebbe non essere supportato nelle versioni future di Comctl32.dll. Inoltre, questo stile non è definito in commctrl.h. Aggiungere la definizione seguente ai file di origine dell'applicazione per usare questo stile: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code></blockquote><br /> | 
| <span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Versione 5.82</a>. <strong>Destinato all'uso interno; non consigliato per l'uso nelle applicazioni.</strong> Questo stile offre alla barra degli strumenti un orientamento verticale. I pulsanti della barra degli strumenti vengono visualizzati dall'alto verso il basso anziché orizzontalmente. <br /><blockquote>[!Note]<br />Questo stile potrebbe non essere supportato nelle versioni future di Comctl32.dll. Inoltre, questo stile non è definito in commctrl.h. Aggiungere la definizione seguente ai file di origine dell'applicazione per usare questo stile: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code></blockquote><br /> | 




## <a name="remarks"></a>Commenti

Per impostare uno stile esteso, inviare al controllo della barra degli strumenti [**un messaggio TB \_ SETEXTENDEDSTYLE.**](tb-setextendedstyle.md) Per determinare quali stili estesi sono attualmente impostati, inviare un messaggio [**\_ TB GETEXTENDEDSTYLE.**](tb-getextendedstyle.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





