---
title: Barra di scorrimento flat
description: Questa sezione contiene informazioni sugli elementi di programmazione usati per controllare le barre di scorrimento flat.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf1c1d49bf4b54d65adbe784d1e4da62adfe35c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466598"
---
# <a name="flat-scroll-bar"></a>Barra di scorrimento flat

Questa sezione contiene informazioni sugli elementi di programmazione usati per controllare le barre di scorrimento flat.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                    | Contenuto                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barre di scorrimento flat](flat-scroll-bars.md) | Microsoft Internet Explorer 4.0 ha introdotto una nuova tecnologia visiva denominata barre di scorrimento flat. Dal punto di vista funzionale, le barre di scorrimento flat si comportano esattamente come le barre di scorrimento standard. La differenza è che è possibile personalizzarne l'aspetto in misura maggiore rispetto alle barre di scorrimento standard.<br/> |



 

### <a name="functions"></a>Funzioni




| Argomento | Contenuto | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a> | Abilita o disabilita uno o entrambi i pulsanti di direzione della barra di scorrimento flat. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a> | Ottiene le informazioni per una barra di scorrimento semplice. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>funzione GetScrollInfo</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a> | Ottiene la posizione della casella di scorrimento in una barra di scorrimento semplice. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>funzione GetScrollPos</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a> | Ottiene le proprietà per una barra di scorrimento semplice. Questa funzione può essere usata anche per determinare se è stato chiamato <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> per questa finestra. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a> | Ottiene le proprietà per una barra di scorrimento semplice. Questa funzione può essere usata anche per determinare se è stato chiamato <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> per questa finestra.<blockquote>[!Note]<br />È identico a <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a> | Ottiene l'intervallo di scorrimento per una barra di scorrimento semplice. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>funzione GetScrollRange</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a> | Imposta le informazioni per una barra di scorrimento semplice. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>funzione SetScrollInfo</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a> | Imposta la posizione corrente della casella di scorrimento in una barra di scorrimento semplice. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>funzione SetScrollPos</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a> | Imposta le proprietà per una barra di scorrimento semplice. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a> | Imposta l'intervallo di scorrimento di una barra di scorrimento semplice. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>funzione SetScrollRange</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a> | Mostra o nasconde una barra di scorrimento semplice. Se le barre di scorrimento flat non vengono inizializzate per la finestra, questa funzione chiama la <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>funzione ShowScrollBar</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> | Inizializza le barre di scorrimento flat per una determinata finestra. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a> | Annulla l'inizializzazione delle barre di scorrimento flat per una determinata finestra. La finestra specificata verrà ripristinata alle barre di scorrimento standard. <br /> | 




 

 

 





