---
title: Come impostare gli Stati del giorno
description: In questo argomento viene illustrato come impostare le informazioni sullo stato del giorno. Il controllo calendario mensile usa le informazioni sullo stato del giorno per determinare come vengono disegnati giorni specifici all'interno del controllo.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963599"
---
# <a name="how-to-set-day-states"></a>Come impostare gli Stati del giorno

In questo argomento viene illustrato come impostare le informazioni sullo stato del giorno. Il controllo calendario mensile usa le informazioni sullo stato del giorno per determinare come vengono disegnati giorni specifici all'interno del controllo.

Controlli di calendario mensile che usano gli Stati del giorno del supporto di tipo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) . Le informazioni sullo stato del giorno sono espresse come tipo di dati a 32 bit, [**MONTHDAYSTATE**](monthdaystate.md). Ogni bit in un bit **MONTHDAYSTATE** (da 0 a 30) specifica lo stato di un giorno in un mese. Se un bit è acceso, il giorno corrispondente viene visualizzato in grassetto.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Un'applicazione può impostare in modo esplicito le informazioni sullo stato del giorno inviando il messaggio [**\_ SETDAYSTATE MCM**](mcm-setdaystate.md) o usando la macro corrispondente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Tuttavia, le informazioni sullo stato del giorno vengono in genere impostate in risposta al codice di notifica [ \_ GETDAYSTATE di MCN](mcn-getdaystate.md) , che viene inviato ogni volta che è necessario aggiornare il controllo perché, ad esempio, è stato eseguito lo scorrimento nella visualizzazione di un mese diverso.

Nell'esempio di codice seguente viene illustrato come elaborare il codice di notifica [ \_ GETDAYSTATE di MCN](mcn-getdaystate.md) in un gestore di messaggi di [**\_ notifica WM**](wm-notify.md) . Elabora MCN \_ GETDAYSTATE specificando che il primo e il quindicesimo giorno di ogni mese visibile devono essere evidenziati. Il membro **cDayState** della struttura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) specifica il numero di valori [**MONTHDAYSTATE**](monthdaystate.md) necessari nella matrice, a cui viene assegnata una dimensione massima arbitraria. Il codice esegue quindi il ciclo per impostare i bit appropriati in ogni elemento valido della matrice, usando la macro **BOLDDAY** definita dall'applicazione.



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo calendario mensile](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informazioni sui controlli calendario mensile](month-calendar-controls.md)
</dt> <dt>

[Utilizzo di controlli calendario mensile](using-month-calendar-controls.md)
</dt> </dl>

 

 




