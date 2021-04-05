---
title: Messaggio di EM_GETEDITSTYLEEX (RichEdit. h)
description: Recupera i flag di stile di modifica estesa correnti.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- Controlli di Windows Message EM_GETEDITSTYLEEX
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873913"
---
# <a name="em_geteditstyleex-message"></a>\_Messaggio GETEDITSTYLEEX em

Recupera i flag di stile di modifica estesa correnti.


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i flag di stile di modifica estesa, che possono includere uno o più dei valori seguenti.



| Codice restituito                                                                                                | Descrizione                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ es \_ HANDLEFRIENDLYURL**</dt> </dl>  | Consente di visualizzare i collegamenti con nome descrittivo con lo stesso colore del testo e la sottostruttura dei collegamenti automatici, a condizione che la formattazione temporanea non sia usata o usi il colore automatico del testo (valore predefinito: 0).<br/>                                                                       |
| <dl> <dt>**\_multitouch es \_ .**</dt> </dl>         | Abilita il supporto tocco in Rich Edit. Sono incluse selezione, posizionamento del cursore e chiamata al menu di scelta rapida. Quando questo flag non è impostato, il tocco viene emulato dai comandi del mouse, che non prendono in considerazione le specifiche della modalità tocco (valore predefinito: 0). <br/>      |
| <dl> <dt>**SES \_ es \_ NOACETATESELECTION**</dt> </dl> | Visualizza il testo selezionato usando il testo di selezione di Windows classico e i colori di sfondo anziché il colore dell'acetato di sfondo (valore predefinito: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ ex \_ nomath**</dt> </dl>             | Disabilita l'inserimento di zone matematiche (impostazione predefinita: 1). Per abilitare la modifica e la visualizzazione della matematica, inviare il messaggio [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) con *wParam* impostato su 0 e *lParam* impostato su **ses \_ ex \_ nomath**. <br/>                              |
| <dl> <dt>**SES \_ es \_ notevole**</dt> </dl>            | Disabilitare l'inserimento di tabelle. Il [**messaggio \_ INSERTTABLE em**](em-inserttable.md) restituisce **e \_ non riesce** e le tabelle RTF vengono ignorate (valore predefinito: 0). <br/>                                                                                                  |
| <dl> <dt>**SES \_ es \_ USESINGLELINE**</dt> </dl>      | Consentire a un controllo su più righe di agire come un controllo a riga singola con la possibilità di scorrere verticalmente quando l'altezza a riga singola è maggiore dell'altezza della finestra (valore predefinito: 0). <br/>                                                                   |
| <dl> <dt>**\_HIDETEMPFORMAT ses**</dt> </dl>         | Nascondere la formattazione temporanea creata quando [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) viene chiamato con **tomApplyTmp**. Questa formattazione, ad esempio, viene usata dai selezionatori ortografici per visualizzare una sottolineatura ondulata sotto parole probabilmente errate.<br/> |
| <dl> <dt>**SES \_ es \_ USEMOUSEWPARAM**</dt> </dl>     | Usare *wParam* per gestire il messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e non chiamare [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).<br/>                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETEDITSTYLEEX em**](em-seteditstyleex.md)
</dt> </dl>

 

