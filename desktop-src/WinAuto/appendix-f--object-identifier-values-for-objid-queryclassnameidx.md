---
title: Appendice F valori identificatore oggetto per OBJID_QUERYCLASSNAMEIDX
description: Quando OLEACC Invia un \_ messaggio WM GetObject con il parametro lParam impostato su OBJIDQUERYCLASSNAMEIDX, molti controlli comuni o utente standard (COMCTL) restituiscono uno dei valori seguenti.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300185"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Appendice F: valori identificatore oggetto per OBJID \_ QUERYCLASSNAMEIDX

Quando OLEACC Invia un messaggio [**WM \_ GetObject**](wm-getobject.md) con il parametro *lParam* impostato su OBJIDQUERYCLASSNAMEIDX, molti controlli comuni o utente standard (COMCTL) restituiscono uno dei valori seguenti.



| UTENTE o controllo comune | Valore restituito |
|------------------------|--------------|
| ListBox                | 65536 + 0      |
| Pulsante                 | 65536 + 2      |
| Static                 | 65536 + 3      |
| Modifica                   | 65536 + 4      |
| Combobox               | 65536 + 5      |
| Barra di scorrimento              | 65536 + 10     |
| Stato                 | 65536 + 11     |
| Barra degli strumenti                | 65536 + 12     |
| Avanzamento               | 65536 + 13     |
| Animare                | 65536 + 14     |
| Scheda                    | 65536 + 15     |
| Tasto di scelta rapida                 | 65536 + 16     |
| Intestazione                 | 65536 + 17     |
| TrackBar               | 65536 + 18     |
| ListView               | 65536 + 19     |
| UpDown                 | 65536 + 22     |
| Descrizioni comandi               | 65536 + 24     |
| TreeView               | 65536 + 25     |
| RichEdit               | 65536 + 28     |



 

Solo gli utenti e i controlli comuni di Windows (COMCTL) restituiranno uno dei valori della tabella. Se una finestra restituisce 0 in risposta a questo messaggio, la finestra può essere una delle seguenti:

-   Un controllo personalizzato
-   Controllo diverso da uno dei controlli della tabella precedente
-   Una versione precedente di un controllo di sistema che non riconosce il messaggio [**WM \_ GetObject**](wm-getobject.md)

Se una finestra restituisce 0, è possibile che i client debbano usare [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) o [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname). È possibile utilizzare queste funzioni per determinare il tipo di controllo in base al nome della classe.

In generale, i client possono usare le informazioni fornite da OLEACC.

 

 