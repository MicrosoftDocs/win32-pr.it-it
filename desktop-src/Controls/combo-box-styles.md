---
title: Stili casella combinata (CommCtrl. h)
description: Per creare una casella combinata usando la funzione CreateWindow o CreateWindowEx, specificare la classe COMBOBOX, le costanti di stile della finestra appropriate e una combinazione degli stili delle caselle combinate seguenti.
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
ms.openlocfilehash: 74f531b93725f3aa92778a42bae3dd3fd972534e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327683"
---
# <a name="combo-box-styles"></a>Stili casella combinata

Per creare una casella combinata usando la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificare la classe ComboBox, le costanti di stile della finestra appropriate e una combinazione degli stili delle caselle combinate seguenti.



| Costante                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**\_AUTOHSCROLL CBS**</dt> </dl>                   | Scorre automaticamente il testo in un controllo di modifica a destra quando l'utente digita un carattere alla fine della riga. Se non si imposta questo stile, è consentito solo il testo che si adatta al limite rettangolare.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL CBS**</dt> </dl>       | Mostra una barra di scorrimento verticale disabilitata nella casella di riepilogo quando la casella non contiene un numero sufficiente di elementi da scorrere. Senza questo stile, la barra di scorrimento viene nascosta quando la casella di riepilogo non contiene sufficienti elementi.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**\_elenco a discesa CBS**</dt> </dl>                            | Simile a CBS \_ Simple, ad eccezione del fatto che la casella di riepilogo non viene visualizzata a meno che l'utente non selezioni un'icona accanto al controllo di modifica.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**\_DropDownList CBS**</dt> </dl>                | Simile all' \_ elenco a discesa CBS, ad eccezione del fatto che il controllo di modifica viene sostituito da un elemento di testo statico che visualizza la selezione corrente nella casella di riepilogo.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**\_HASSTRINGS CBS**</dt> </dl>                      | Specifica che una casella combinata creata dal proprietario contiene elementi costituiti da stringhe. La casella combinata gestisce la memoria e l'indirizzo per le stringhe in modo che l'applicazione possa usare il messaggio [**CB \_ GETLBTEXT**](cb-getlbtext.md) per recuperare il testo di un particolare elemento.<br/> Per problemi di accessibilità, vedere [esposizione di Owner-Drawn elementi della casella combinata](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**\_minuscolo CBS**</dt> </dl>                         | Converte in minuscolo tutto il testo nel campo di selezione e nell'elenco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**\_NOINTEGRALHEIGHT CBS**</dt> </dl>    | Specifica che la dimensione della casella combinata è esattamente quella specificata dall'applicazione al momento della creazione della casella combinata. In genere, il sistema ridimensiona una casella combinata in modo da non visualizzare elementi parziali.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**\_OEMCONVERT CBS**</dt> </dl>                      | Converte il testo immesso nel controllo di modifica della casella combinata dal set di caratteri di Windows al set di caratteri OEM e quindi di nuovo al set di caratteri di Windows. Ciò assicura la corretta conversione dei caratteri quando l'applicazione chiama la funzione [**CharToOem**](/windows/desktop/api/winuser/nf-winuser-chartooema) per convertire una stringa di Windows nella casella combinata in caratteri OEM. Questo stile è particolarmente utile per le caselle combinate che contengono nomi file e si applica solo alle caselle combinate create con lo \_ stile a discesa CBS Simple o CBS \_ .<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**\_OwnerDrawFixed CBS**</dt> </dl>          | Specifica che il proprietario della casella di riepilogo è responsabile del disegno del contenuto e che gli elementi nella casella di riepilogo sono tutti della stessa altezza. La finestra proprietaria riceve un messaggio [**WM \_ MeasureItem**](wm-measureitem.md) al momento della creazione della casella combinata e un messaggio [**WM \_ DrawItem**](wm-drawitem.md) quando viene modificato un aspetto visivo della casella combinata.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**\_OwnerDrawVariable CBS**</dt> </dl> | Specifica che il proprietario della casella di riepilogo è responsabile del disegno del contenuto e che gli elementi nella casella di riepilogo siano variabili in altezza. La finestra proprietaria riceve un messaggio [**WM \_ MeasureItem**](wm-measureitem.md) per ogni elemento nella casella combinata quando si creano la casella combinata e un messaggio [**WM \_ DrawItem**](wm-drawitem.md) quando viene modificato un aspetto visivo della casella combinata.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**\_semplice CBS**</dt> </dl>                                  | Visualizza sempre la casella di riepilogo. La selezione corrente nella casella di riepilogo viene visualizzata nel controllo di modifica.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**\_ordinamento CBS**</dt> </dl>                                        | Ordina automaticamente le stringhe aggiunte alla casella di riepilogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**\_lettere maiuscole CBS**</dt> </dl>                         | Converte in maiuscolo tutto il testo nel campo di selezione e nell'elenco.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

