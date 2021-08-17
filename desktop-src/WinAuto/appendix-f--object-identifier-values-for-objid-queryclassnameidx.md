---
title: Appendice F Object Identifier Values for OBJID_QUERYCLASSNAMEIDX
description: Quando OLEACC invia un messaggio WM GETOBJECT con il parametro lParam impostato su \_ OBJIDQUERYCLASSNAMEIDX, molti controlli COMUNI o USER standard restituiscono uno dei valori seguenti.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22368f15fa40e30f909f9ad838cb478ed1e9a9c9ff25929f63bb91ec99e99b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134034"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Appendice F: Valori degli identificatori di oggetto per \_ OBJID QUERYCLASSNAMEIDX

Quando OLEACC invia un messaggio [**WM \_ GETOBJECT**](wm-getobject.md) con il parametro *lParam* impostato su OBJIDQUERYCLASSNAMEIDX, molti controlli COMUNI o USER standard restituiscono uno dei valori seguenti.



| USER o controllo comune | Valore restituito |
|------------------------|--------------|
| Listbox                | 65536+0      |
| Button                 | 65536+2      |
| Statica                 | 65536+3      |
| Modifica                   | 65536+4      |
| Combobox               | 65536+5      |
| Barra di scorrimento              | 65536+10     |
| Stato                 | 65536+11     |
| Barra degli strumenti                | 65536+12     |
| Avanzamento               | 65536+13     |
| Animare                | 65536+14     |
| Scheda                    | 65536+15     |
| Tasto di scelta rapida                 | 65536+16     |
| Intestazione                 | 65536+17     |
| Trackbar               | 65536+18     |
| Listview               | 65536+19     |
| Updown                 | 65536+22     |
| Le descrizioni comandi               | 65536+24     |
| Treeview               | 65536+25     |
| RichEdit               | 65536+28     |



 

Solo USER e Windows comuni (COMCTL) restituiranno uno dei valori della tabella. Se una finestra restituisce 0 in risposta a questo messaggio, la finestra può essere una delle seguenti:

-   Controllo personalizzato
-   Controllo diverso da uno dei controlli nella tabella precedente
-   Una versione precedente di un controllo di sistema che non riconosce il [**messaggio WM \_ GETOBJECT**](wm-getobject.md)

Se una finestra restituisce 0, i client potrebbero dover usare [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) o [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname). È possibile usare queste funzioni per determinare il tipo di controllo in base al nome della classe.

In generale, i client possono utilizzare le informazioni fornite da OLEACC.

 

 