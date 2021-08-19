---
title: EM_GETEDITSTYLEEX messaggio (Richedit.h)
description: Recupera i flag di stile di modifica estesi correnti.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX di controllo Windows messaggio
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
ms.openlocfilehash: ad3c011a162bbf0a1822e68be6bd60f662551b3a22ecfca62c64ef8d01a605a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049311"
---
# <a name="em_geteditstyleex-message"></a>Messaggio \_ EM GETEDITSTYLEEX

Recupera i flag di stile di modifica estesi correnti.


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i flag di stile di modifica estesi, che possono includere uno o più dei valori seguenti.



| Codice restituito                                                                                                | Descrizione                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ EX \_ HANDLEFRIENDLYURL**</dt> </dl>  | Visualizza collegamenti con nome descrittivo con lo stesso colore del testo e sottolineatura dei collegamenti automatici, a condizione che la formattazione temporanea non sia usata o usi il colore automatico del testo (impostazione predefinita: 0).<br/>                                                                       |
| <dl> <dt>**SES \_ EX \_ MULTITOUCH**</dt> </dl>         | Abilitare il supporto del tocco in Rich Edit. Sono incluse la selezione, il posizionamento del caret e la chiamata al menu di scelta rapida. Quando questo flag non è impostato, il tocco viene emulato dai comandi del mouse, che non prendono in considerazione le specifiche della modalità tocco (impostazione predefinita: 0). <br/>      |
| <dl> <dt>**SES \_ EX \_ NOACETATESELECTION**</dt> </dl> | Visualizzare il testo selezionato usando i colori Windows testo e sfondo della selezione classica anziché il colore acetato di sfondo (impostazione predefinita: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ EX \_ NOMATH**</dt> </dl>             | Disabilitare l'inserimento di zone matematiche (impostazione predefinita: 1). Per abilitare la modifica matematica e la visualizzazione, inviare il messaggio [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) con *wParam* impostato su 0 e *lParam* impostato su **SES \_ EX \_ NOMATH**. <br/>                              |
| <dl> <dt>**SES \_ EX \_ NOTABLE**</dt> </dl>            | Disabilitare l'inserimento di tabelle. Il [**messaggio EM \_ INSERTTABLE**](em-inserttable.md) restituisce **E \_ FAIL** e le tabelle RTF vengono ignorate (impostazione predefinita: 0). <br/>                                                                                                  |
| <dl> <dt>**SES \_ EX \_ USESINGLELINE**</dt> </dl>      | Abilitare un controllo multilinea per agire come un controllo a riga singola con la possibilità di scorrere verticalmente quando l'altezza di una riga è maggiore dell'altezza della finestra (impostazione predefinita: 0). <br/>                                                                   |
| <dl> <dt>**SES \_ HIDETEMPFORMAT**</dt> </dl>         | Nascondere la formattazione temporanea creata quando viene chiamato [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) con **tomApplyTmp**. Ad esempio, tale formattazione viene usata dai correttori ortografici per visualizzare una sottolineatura ondulata con parole potenzialmente errate.<br/> |
| <dl> <dt>**SES \_ EX \_ USEMOUSEWPARAM**</dt> </dl>     | Usare *wParam quando* si gestisce il [**messaggio WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e non chiamare [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).<br/>                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md)
</dt> </dl>

 

