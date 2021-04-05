---
title: Casella combinata (riferimento all'elemento MSAA UI)
description: Una casella combinata è un casella di riepilogo combinata con un controllo statico o un controllo di modifica che visualizza l'elemento attualmente selezionato nel componente casella di riepilogo della casella combinata.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce42bb3b0316b0fb2668fed23564b8f904fc793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711098"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Casella combinata (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti **casella combinata** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti **casella combinata** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Una casella combinata è un casella di riepilogo combinata con un controllo statico o un controllo di modifica che visualizza l'elemento attualmente selezionato nel componente casella di riepilogo della casella combinata. La parte della casella di riepilogo del controllo viene visualizzata in qualsiasi momento o solo quando l'utente seleziona la freccia a discesa (ovvero un pulsante di comando) accanto al controllo. Se il campo di selezione è un controllo di modifica, l'utente può immettere informazioni non presenti nell'elenco. in caso contrario, l'utente può solo selezionare gli elementi nell'elenco.

Il nome della classe della finestra per una casella combinata è "COMBOBOX".

Il contenuto delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dipende da quale delle parti seguenti della casella combinata viene sottoposta a query dal client:

-   Finestra della casella combinata
-   Controllo di modifica o controllo testo statico
-   Freccia a discesa (che è un pulsante di push)
-   Casella di riepilogo
-   Voci dell'elenco nella casella di riepilogo

## <a name="iaccessible-methods"></a>Metodi IAccessible

Le caselle combinate supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Le caselle combinate supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): nella tabella seguente viene illustrato il valore del conteggio figlio per parti diverse della casella combinata. 

    | Parte della casella combinata   | ChildCount               |
    |------------------|--------------------------|
    | Casella combinata | 3                        |
    | Controllo Edit     | 0                        |
    | Freccia a discesa  | 0                        |
    | Casella di riepilogo         | Numero di elementi dell'elenco |
    | Elemento elenco        | 0                        |

    

     

-   [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): nella tabella seguente viene illustrata la proprietà **DefaultAction** per le diverse parti di una casella combinata. 

    | Parte della casella combinata   | DefaultAction                                                  |
    |------------------|----------------------------------------------------------------|
    | Casella combinata | nessuno                                                           |
    | Controllo Edit     | nessuno                                                           |
    | Freccia a discesa  | "Open" o "close" a seconda dello stato dell'elenco a discesa |
    | Casella di riepilogo         | nessuno                                                           |
    | Elemento elenco        | "Doppio clic"                                                 |

    

     

-   [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): nella tabella seguente viene illustrata la proprietà **KeyboardShortcut** per le diverse parti di una casella combinata. 

    | Parte della casella combinata   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Casella combinata | Chiave di accesso dell'etichetta associata |
    | Controllo Edit     | nessuno                           |
    | Freccia a discesa  | "ALT + freccia giù"               |
    | Casella di riepilogo         | nessuno                           |
    | Elemento elenco        | nessuno                           |

    

     

    La chiave di accesso per una casella combinata è il carattere sottolineato nel testo di un controllo testo statico associato che etichetta la casella combinata. Ad esempio, in una finestra di dialogo Apri standard in cui si aprono i file, ad esempio in Microsoft WordPad, la casella combinata con etichetta "file di tipo:" ha **KeyboardShortcut** "Alt + t".

-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): nella tabella seguente viene illustrata la proprietà **Name** per le diverse parti di una casella combinata. 

    | Parte della casella combinata   | Nome                                                           |
    |------------------|----------------------------------------------------------------|
    | Casella combinata | Controllo testo statico utilizzato come etichetta                            |
    | Controllo Edit     | Controllo testo statico utilizzato come etichetta                            |
    | Freccia a discesa  | "Open" o "close" a seconda dello stato dell'elenco a discesa |
    | Casella di riepilogo         | Etichetta associata                                               |
    | Elemento elenco        | Testo dell'elemento dell'elenco                                          |

    

     

    La proprietà **Name** di una casella combinata, il relativo controllo di modifica figlio e la relativa casella di riepilogo figlio è il testo di un controllo testo statico associato che etichetta la casella combinata. Ad esempio, in una finestra di dialogo Apri standard che apre file, ad esempio in WordPad, le proprietà **nome** per le due caselle combinate sono "Cerca in:" e "file di tipo:".

-   [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la tabella seguente illustra il valore padre per le diverse parti di una casella combinata. 

    | Parte della casella combinata                        | Padre                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Casella combinata                      | Finestra con la proprietà **Role** della [**finestra del \_ sistema \_ dei ruoli**](object-roles.md) che racchiude la casella combinata e ha la stessa proprietà **Name** e il nome della classe di finestra della casella combinata. |
    | Modifica controllo (o controllo testo statico) | Finestra della casella combinata.                                                                                                                                                                                          |
    | Freccia a discesa                       | Finestra della casella combinata.                                                                                                                                                                                          |
    | Finestra padre casella di riepilogo                | Finestra della casella combinata. Questa finestra racchiude la casella di riepilogo.                                                                                                                                                      |
    | Casella di riepilogo                              | Finestra padre della casella di riepilogo.                                                                                                                                                                                    |
    | Elemento elenco                             | Casella di riepilogo.                                                                                                                                                                                                  |

    

     

-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): nella tabella seguente viene illustrata la proprietà **Role** per le diverse parti di una casella combinata. 

    | Parte della casella combinata                        | [Ruolo](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Casella combinata                      | [**\_ \_ casella combinata sistema ruolo**](object-roles.md)                                                                    |
    | Modifica controllo (o controllo testo statico) | [**Ruolo \_ di \_Testo del sistema**](object-roles.md) o [ **sistema del ruolo \_ \_ STATICTEXT**](object-roles.md) |
    | Freccia a discesa                       | [**\_pulsante sistema \_ ruolo**](object-roles.md)                                                                |
    | Casella di riepilogo                              | [**\_elenco sistema \_ ruoli**](object-roles.md)                                                                            |
    | Elemento elenco                             | [**\_ListItem del sistema di ruolo \_**](object-roles.md)                                                                    |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): nella tabella seguente viene illustrata la proprietà **state** per le diverse parti di una casella combinata. 

    | Parte della casella combinata   | [Stati possibili](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Casella combinata | [**Stato \_ di sistema stato \_ invisibile**](object-state-constants.md) al sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato \| attivo [**\_ \_**](object-state-constants.md) sistema stato stato \| [**\_ \_ attivo**](object-state-constants.md) sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ espanso**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema stato compresso |
    | Controllo Edit     | [**Stato \_ di sistema stato \_ invisibile**](object-state-constants.md) al sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema                                                                                                                                                                         |
    | Freccia a discesa  | 0, che indica che il pulsante è visibile e non è premuto; sistema di stato [**\_ \_ premutato**](object-state-constants.md) sistema di stato \| [**\_ \_ invisibile**](object-state-constants.md) al sistema di stato \| \_ \_                                                                                                                                                                                                                                                                                                                                                    |
    | Casella di riepilogo         | [**Stato \_ di sistema stato \_ invisibile**](object-state-constants.md) al sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema stato stato attivo sistema                                                                                      |
    | Elemento elenco        | [**Stato \_ di sistema \_ stato**](object-state-constants.md) attivo sistema di stato stato attivo sistema di stato stato \| [**\_ \_ attivo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ selezionabile**](object-state-constants.md) dal sistema di stato selezionato sistema stato \| [**\_ \_ selezionato**](object-state-constants.md) \| [**\_ \_ normale**](object-state-constants.md)                                                                                        |

    

     

-   [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): nella tabella seguente viene illustrata la proprietà **value** per le diverse parti di una casella combinata. 

    | Parte della casella combinata   | Valore                                |
    |------------------|--------------------------------------|
    | Casella combinata | Testo dell'elemento elenco attualmente selezionato |
    | Controllo Edit     | Testo dell'elemento elenco attualmente selezionato |
    | Freccia a discesa  | nessuno                                 |
    | Casella di riepilogo         | nessuno                                 |
    | Elemento elenco        | nessuno                                 |

    

     

## <a name="notes"></a>Note

-   Quando [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) viene chiamato con il [**flag \_ successivo NAVDIR**](navigation-constants.md) nella casella di riepilogo di una casella combinata, si sposta in modo errato sulla finestra della barra delle applicazioni quando deve restituire un **VT \_ vuoto**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




