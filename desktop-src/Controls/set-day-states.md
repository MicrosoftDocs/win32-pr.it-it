---
title: Come impostare gli stati del giorno
description: Questo argomento illustra come impostare le informazioni sullo stato del giorno. Il controllo calendario mensile usa le informazioni sullo stato del giorno per determinare la modalità di disegno di giorni specifici all'interno del controllo.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3ed2c99e6faf18f0e1d06ec06eaaf9a0d573faebe6f3697e43562603447571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078475"
---
# <a name="how-to-set-day-states"></a>Come impostare gli stati del giorno

Questo argomento illustra come impostare le informazioni sullo stato del giorno. Il controllo calendario mensile usa le informazioni sullo stato del giorno per determinare la modalità di disegno di giorni specifici all'interno del controllo.

I controlli calendario mensile che usano lo [**stile \_ DAYSTATE MCS**](month-calendar-control-styles.md) supportano gli stati dei giorni. Le informazioni sullo stato del giorno vengono espresse come tipo di dati a 32 bit, [**MONTHDAYSTATE.**](monthdaystate.md) Ogni bit in un campo di bit **MONTHDAYSTATE** (da 0 a 30) specifica lo stato di un giorno in un mese. Se un bit è on, il giorno corrispondente viene visualizzato in grassetto.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Un'applicazione può impostare in modo esplicito le informazioni sullo stato del giorno inviando il messaggio [**\_ MCM SETDAYSTATE**](mcm-setdaystate.md) o usando la macro corrispondente, [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Tuttavia, le informazioni sullo stato del giorno vengono in genere impostate in risposta al codice di notifica [ \_ MCN GETDAYSTATE,](mcn-getdaystate.md) che viene inviato ogni volta che il controllo deve essere aggiornato perché, ad esempio, un mese diverso è stato visualizzato.

Il codice di esempio seguente illustra come elaborare il codice di notifica [ \_ MCN GETDAYSTATE](mcn-getdaystate.md) in un gestore [**di messaggi WM \_ NOTIFY.**](wm-notify.md) Elabora MCN GETDAYSTATE specificando che il primo e il quindicesimo giorno di ogni mese visibile \_ devono essere evidenziati. Il **membro cDayState** della struttura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) specifica il numero di [**valori MONTHDAYSTATE**](monthdaystate.md) necessari nella matrice, a cui viene data una dimensione massima arbitraria. Il codice esegue quindi un ciclo per impostare i bit appropriati in ogni elemento valido della matrice, usando la macro **BOLDDAY** definita dall'applicazione.



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

[Informazioni di riferimento sul controllo Calendario mensile](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informazioni sui controlli calendario mensile](month-calendar-controls.md)
</dt> <dt>

[Uso dei controlli calendario mensile](using-month-calendar-controls.md)
</dt> </dl>

 

 




