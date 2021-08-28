---
title: Stili casella combinata (CommCtrl.h)
description: Per creare una casella combinata usando la funzione CreateWindow o CreateWindowEx, specificare la classe COMBOBOX, le costanti di stile della finestra appropriate e una combinazione degli stili della casella combinata seguenti.
ms.assetid: 4dc347b2-7da7-4aa0-b61f-781acf652d84
topic_type:
- apiref
api_name:
- CBS_AUTOHSCROLL
- CBS_DISABLENOSCROLL
- CBS_DROPDOWN
- CBS_DROPDOWNLIST
- CBS_HASSTRINGS
- CBS_LOWERCASE
- CBS_NOINTEGRALHEIGHT
- CBS_OEMCONVERT
- CBS_OWNERDRAWFIXED
- CBS_OWNERDRAWVARIABLE
- CBS_SIMPLE
- CBS_SORT
- CBS_UPPERCASE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652a6392cf8ce50f01efa215e8d6472d1fd1ff344b35fb36d72f0e5dc3c48c68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968501"
---
# <a name="combo-box-styles"></a>Stili delle caselle combinate

Per creare una casella combinata usando la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificare la classe COMBOBOX, le costanti di stile della finestra appropriate e una combinazione degli stili della casella combinata seguenti.



| Costante                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**AUTOHSCROLL di \_ CBS**</dt> </dl>                   | Scorre automaticamente il testo in un controllo di modifica verso destra quando l'utente ha immesso un carattere alla fine della riga. Se non si imposta questo stile, è consentito solo il testo che si adatta al limite rettangolare.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**DISABLENOSCROLL di CBS \_**</dt> </dl>       | Mostra una barra di scorrimento verticale disabilitata nella casella di riepilogo quando la casella non contiene elementi sufficienti per lo scorrimento. Senza questo stile, la barra di scorrimento viene nascosta quando la casella di riepilogo non contiene sufficienti elementi.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**ELENCO A DISCESA \_ CBS**</dt> </dl>                            | Simile a CBS SIMPLE, ad eccezione del fatto che la casella di riepilogo non viene visualizzata a meno che l'utente non seleziona \_ un'icona accanto al controllo di modifica.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**ELENCO A DISCESA CBS \_**</dt> </dl>                | Simile a CBS DROPDOWN, ad eccezione del fatto che il controllo di modifica viene sostituito da un elemento di testo statico che visualizza la \_ selezione corrente nella casella di riepilogo.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**CBS \_ HASSTRINGS**</dt> </dl>                      | Specifica che una casella combinata disegnata dal proprietario contiene elementi costituiti da stringhe. La casella combinata mantiene la memoria e l'indirizzo per le stringhe in modo che l'applicazione possa usare il messaggio [**\_ GETLBTEXT CB**](cb-getlbtext.md) per recuperare il testo per un particolare elemento.<br/> Per problemi di accessibilità, vedere [Esposizione di Owner-Drawn casella combinata](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**CBS \_ MINUSCOLA**</dt> </dl>                         | Converte in lettere minuscole tutto il testo nel campo di selezione e nell'elenco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**CBS \_ NOINTEGRALHEIGHT**</dt> </dl>    | Specifica che le dimensioni della casella combinata sono esattamente le dimensioni specificate dall'applicazione al momento della creazione della casella combinata. In genere, il sistema ridimensiona una casella combinata in modo che non visualizza elementi parziali.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**CBS \_ OEMCONVERT**</dt> </dl>                      | Converte il testo immesso nel controllo di modifica della casella combinata dal set di caratteri Windows al set di caratteri OEM e quindi al set Windows set di caratteri. Ciò garantisce la conversione corretta dei caratteri quando l'applicazione chiama la funzione [**CharToOem**](/windows/desktop/api/winuser/nf-winuser-chartooema) per convertire una Windows stringa nella casella combinata in caratteri OEM. Questo stile è particolarmente utile per le caselle combinate che contengono nomi di file e si applica solo alle caselle combinate create con lo stile \_ CBS SIMPLE o CBS \_ DROPDOWN.<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**PROPRIETARIO \_ CBSDRAWFIXED**</dt> </dl>          | Specifica che il proprietario della casella di riepilogo è responsabile del disegno del contenuto e che gli elementi nella casella di riepilogo hanno la stessa altezza. La finestra proprietaria riceve un [**messaggio WM \_ MEASUREITEM**](wm-measureitem.md) quando viene creata la casella combinata e un messaggio [**WM \_ DRAWITEM**](wm-drawitem.md) quando viene modificato un aspetto visivo della casella combinata.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**PROPRIETARIO \_ CBSDRAWVARIABLE**</dt> </dl> | Specifica che il proprietario della casella di riepilogo è responsabile del disegno del contenuto e che gli elementi nella casella di riepilogo sono variabili in altezza. La finestra proprietaria riceve un [**messaggio WM \_ MEASUREITEM**](wm-measureitem.md) per ogni elemento della casella combinata quando si crea la casella combinata e un messaggio [**WM \_ DRAWITEM**](wm-drawitem.md) quando viene modificato un aspetto visivo della casella combinata.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ SIMPLE**</dt> </dl>                                  | Visualizza sempre la casella di riepilogo. La selezione corrente nella casella di riepilogo viene visualizzata nel controllo di modifica.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**ORDINAMENTO \_ CBS**</dt> </dl>                                        | Ordina automaticamente le stringhe aggiunte alla casella di riepilogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**CBS \_ MAIUSCOLA**</dt> </dl>                         | Converte in maiuscolo tutto il testo sia nel campo di selezione che nell'elenco.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

