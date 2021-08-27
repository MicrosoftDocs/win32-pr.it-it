---
title: Casella combinata (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: Una casella combinata è un casella di riepilogo combinata con un controllo statico o un controllo di modifica che visualizza l'elemento attualmente selezionato nel componente casella di riepilogo della casella combinata.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3a8d26fa5b8cb264c06e7aa64c672e0a80e8ada7e90a152b3b941ea207cade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071841"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Casella combinata (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Casella combinata ai** fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Casella combinata** in vari framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

Una casella combinata è un casella di riepilogo combinata con un controllo statico o un controllo di modifica che visualizza l'elemento attualmente selezionato nel componente casella di riepilogo della casella combinata. La parte della casella di riepilogo del controllo viene visualizzata in qualsiasi momento o solo a discesa quando l'utente seleziona la freccia a discesa (che è un pulsante di pressione) accanto al controllo. Se il campo di selezione è un controllo di modifica, l'utente può immettere informazioni non presenti nell'elenco. In caso contrario, l'utente può selezionare solo gli elementi nell'elenco.

Il nome della classe della finestra per una casella combinata è "COMBOBOX".

Il contenuto delle [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dipende da quale delle parti seguenti della casella combinata viene eseguita una query dal client:

-   Finestra della casella combinata
-   Controllo di modifica o controllo di testo statico
-   Freccia a discesa (che è un pulsante di pressione)
-   Casella di riepilogo
-   Elementi dell'elenco nella casella di riepilogo

## <a name="iaccessible-methods"></a>Metodi IAccessible

Le caselle combinate supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Le caselle combinate supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)la tabella seguente mostra il valore di conteggio figlio per le diverse parti della casella combinata. 

    | Parte della casella combinata   | ChildCount               |
    |------------------|--------------------------|
    | Finestra casella combinata | 3                        |
    | Controllo Edit     | 0                        |
    | Freccia a discesa  | 0                        |
    | Casella di riepilogo         | Numero di elementi dell'elenco |
    | Elemento elenco        | 0                        |

    

     

-   [**get \_ accDefaultAction:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)la tabella seguente mostra la **proprietà DefaultAction** per diverse parti di una casella combinata. 

    | Parte della casella combinata   | Defaultaction                                                  |
    |------------------|----------------------------------------------------------------|
    | Finestra casella combinata | Nessuno                                                           |
    | Controllo Edit     | Nessuno                                                           |
    | Freccia a discesa  | "Apri" o "Chiudi" a seconda dello stato dell'elenco a discesa |
    | Casella di riepilogo         | Nessuno                                                           |
    | Elemento elenco        | "Doppio clic"                                                 |

    

     

-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)la tabella seguente mostra la **proprietà KeyboardShortcut** per diverse parti di una casella combinata. 

    | Parte della casella combinata   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Finestra casella combinata | Chiave di accesso dell'etichetta associata |
    | Controllo Edit     | Nessuno                           |
    | Freccia a discesa  | "ALT+freccia GIÙ"               |
    | Casella di riepilogo         | Nessuno                           |
    | Elemento elenco        | Nessuno                           |

    

     

    Il tasto di scelta per una casella combinata è il carattere sottolineato nel testo di un controllo di testo statico associato che etichetta la casella combinata. Ad esempio, in una finestra di dialogo Apri standard che apre i file, ad esempio in Microsoft WordPad, la casella combinata con etichetta "File di tipo:" ha **KeyboardShortcut** "Alt+t".

-   [**get \_ accName:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)la tabella seguente mostra la **proprietà Name** per le diverse parti di una casella combinata. 

    | Parte della casella combinata   | Nome                                                           |
    |------------------|----------------------------------------------------------------|
    | Finestra casella combinata | Controllo testo statico usato come etichetta                            |
    | Controllo Edit     | Controllo testo statico usato come etichetta                            |
    | Freccia a discesa  | "Apri" o "Chiudi" a seconda dello stato dell'elenco a discesa |
    | Casella di riepilogo         | Etichetta associata                                               |
    | Elemento elenco        | Testo dell'elemento dell'elenco                                          |

    

     

    La **proprietà Name** di una casella combinata, il relativo controllo di modifica figlio e la relativa casella di riepilogo figlio sono il testo di un controllo di testo statico associato che etichetta la casella combinata. Ad esempio, in una finestra di dialogo Apri standard che  apre i file, ad esempio in WordPad, le proprietà Nome per le due caselle combinate sono "Cerca in:" e "File di tipo:".

-   [**get \_ accParent:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)la tabella seguente mostra il valore padre per le diverse parti di una casella combinata. 

    | Parte della casella combinata                        | Padre                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestra casella combinata                      | Finestra con la **proprietà Role** di ROLE [**SYSTEM \_ \_ WINDOW**](object-roles.md) che racchiude la casella combinata e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra della casella combinata. |
    | Controllo di modifica (o controllo di testo statico) | Finestra della casella combinata.                                                                                                                                                                                          |
    | Freccia a discesa                       | Finestra della casella combinata.                                                                                                                                                                                          |
    | Finestra padre della casella di riepilogo                | Finestra della casella combinata. Questa finestra racchiude la casella di riepilogo.                                                                                                                                                      |
    | Casella di riepilogo                              | Finestra padre della casella di riepilogo.                                                                                                                                                                                    |
    | Elemento elenco                             | Casella di riepilogo.                                                                                                                                                                                                  |

    

     

-   [**get \_ accRole:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)la tabella seguente mostra la **proprietà Role** per diverse parti di una casella combinata. 

    | Parte della casella combinata                        | [Ruolo](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Finestra casella combinata                      | [**CASELLA \_ COMBINATA SISTEMA \_ RUOLO**](object-roles.md)                                                                    |
    | Controllo di modifica (o controllo di testo statico) | [**ROLE \_ SYSTEM \_ TEXT o**](object-roles.md) ROLE SYSTEM [ **\_ \_ STATICTEXT**](object-roles.md) |
    | Freccia a discesa                       | [**PULSANTE \_ PUSH DEL SISTEMA DI \_ RUOLI**](object-roles.md)                                                                |
    | Casella di riepilogo                              | [**ELENCO \_ DI SISTEMI \_ RUOLO**](object-roles.md)                                                                            |
    | Elemento elenco                             | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)                                                                    |

    

     

-   [**get \_ accState:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)la tabella seguente mostra la **proprietà State** per le diverse parti di una casella combinata. 

    | Parte della casella combinata   | [Stati possibili](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestra casella combinata | [**STATE \_ SISTEMA \_ INVISIBILE AL**](object-state-constants.md) SISTEMA DI STATO \| [**\_ INVISIBILE \_ SISTEMA STATO**](object-state-constants.md) NON DISPONIBILE STATO ATTIVO SISTEMA STATO ATTIVO SISTEMA DI STATO NORMALE SISTEMA DI STATO ESPANSO SISTEMA DI STATO \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ ESPANSO COMPRESSO**](object-state-constants.md) |
    | Controllo Edit     | [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md)                                                                                                                                                                         |
    | Freccia a discesa  | 0, ovvero il pulsante è visibile e non premuto. o [**STATE \_ SYSTEM \_ PRESSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| STATE SYSTEM \_ \_ NORMAL                                                                                                                                                                                                                                                                                                                                                    |
    | Casella di riepilogo         | [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FLOATING**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)                                                                                      |
    | Elemento elenco        | [**STATE \_ SISTEMA \_ INVISIBILE STATO**](object-state-constants.md) \| [**\_ INVISIBILE SISTEMA STATO ATTIVO \_ SISTEMA**](object-state-constants.md) STATO ATTIVO SISTEMA \| [**\_ \_**](object-state-constants.md) STATO \| [**\_ \_ SELEZIONABILE**](object-state-constants.md) SISTEMA STATO \| [**SELEZIONATO \_ \_ NORMALE**](object-state-constants.md) \| [**SISTEMA DI \_ STATO \_**](object-state-constants.md)                                                                                        |

    

     

-   [**get \_ accValue:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)la tabella seguente mostra la **proprietà Value** per diverse parti di una casella combinata. 

    | Parte della casella combinata   | Valore                                |
    |------------------|--------------------------------------|
    | Finestra casella combinata | Testo dell'elemento dell'elenco attualmente selezionato |
    | Controllo Edit     | Testo dell'elemento dell'elenco attualmente selezionato |
    | Freccia a discesa  | Nessuno                                 |
    | Casella di riepilogo         | Nessuno                                 |
    | Elemento elenco        | Nessuno                                 |

    

     

## <a name="notes"></a>Note

-   Quando [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) viene chiamato con il flag [**NAVDIR \_ NEXT**](navigation-constants.md) nella parte casella di riepilogo di una casella combinata, passa erroneamente alla finestra della barra delle applicazioni quando deve restituire **VT \_ EMPTY.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




