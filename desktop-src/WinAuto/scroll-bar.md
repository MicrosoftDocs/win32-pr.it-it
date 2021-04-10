---
title: Barra di scorrimento (riferimento all'elemento dell'interfaccia utente MSAA)
description: Le barre di scorrimento consentono a un utente di scegliere la direzione e la distanza per scorrere le informazioni in una finestra o in una casella di riepilogo correlata. Il nome della classe della finestra per una barra di scorrimento è \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047305"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Barra di scorrimento (riferimento all'elemento dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **barra di scorrimento** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **barra di scorrimento** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Le barre di scorrimento consentono a un utente di scegliere la direzione e la distanza per scorrere le informazioni in una finestra o in una casella di riepilogo correlata. Il nome della classe della finestra per una barra di scorrimento è "SCROLLBAR".

Il contenuto delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varia a seconda che la barra di scorrimento sia verticale o orizzontale e su quale delle parti seguenti della barra di scorrimento venga eseguita una query da parte del client:

-   Barra di scorrimento stessa
-   Pulsante freccia in alto o a destra
-   Pulsante freccia in basso o a sinistra
-   Casella di scorrimento (Thumb)
-   Area in alto o a destra della pagina
-   La pagina verso il basso o l'area a sinistra della pagina

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una barra di scorrimento supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): l'oggetto barra di scorrimento e il cursore di scorrimento non supportano il metodo **accDoDefaultAction** .

    Per le altre parti della barra di scorrimento in una barra di scorrimento verticale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chiama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con il messaggio [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) con *wParam* impostato sui valori seguenti.

    

    | Pulsante/area       | Vaule        |
    |---------------------|--------------|
    | Pulsante freccia in alto    | \_lineup SB   |
    | Pulsante freccia in basso | \_LINEDOWN SB |
    | Area di paging      | \_PAGEUP SB   |
    | Area in basso    | \_PGGIÙ SB |

    

     

    Per le altre parti della barra di scorrimento in una barra di scorrimento orizzontale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chiama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con il messaggio [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) con *wParam* impostato sui valori seguenti.

    

    | Pulsante/area      | Valore         |
    |--------------------|---------------|
    | Pulsante freccia sinistra  | \_LINELEFT SB  |
    | Pulsante freccia destra | \_LINERIGHT SB |
    | Area a sinistra della pagina   | \_PAGELEFT SB  |
    | Area a destra della pagina  | \_PAGERIGHT SB |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una barra di scorrimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la proprietà **childCount** per l'oggetto barra di scorrimento è cinque. Per le altre parti della barra di scorrimento, la proprietà **childCount** è zero.
-   [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): l'oggetto barra di scorrimento e il cursore di scorrimento non supportano la proprietà **DefaultAction** . La proprietà **DefaultAction** per i pulsanti freccia e le aree ombreggiate su entrambi i lati del cursore di scorrimento è "premere".
-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription): la proprietà **Description** dipende dalla parte della barra di scorrimento su cui viene eseguita una query.

    Le parti di una barra di scorrimento verticale hanno le descrizioni seguenti.

    

    | Parte                | Descrizione                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Barra di scorrimento stessa   | "Usato per modificare l'area di visualizzazione verticale"                                          |
    | Pulsante freccia in alto    | "Sposta la posizione verticale verso l'alto di una riga"                                           |
    | Pulsante freccia in basso | "Sposta la posizione verticale verso il basso di una riga"                                         |
    | Cursore di scorrimento        | "Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente". |
    | Area di paging      | "Sposta la posizione verticale verso l'alto di un paio di righe"                                  |
    | Area in basso    | "Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente". |

    

     

    Le parti di una barra di scorrimento orizzontale hanno le descrizioni seguenti.

    

    | Parte               | Descrizione                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Barra di scorrimento stessa  | "Usato per modificare l'area di visualizzazione orizzontale"                                          |
    | Pulsante freccia sinistra  | "Sposta la posizione orizzontale a sinistra di una colonna"                                       |
    | Pulsante freccia destra | ' Sposta la posizione orizzontale a destra di una colonna "                                      |
    | Cursore di scorrimento       | "Indica la posizione orizzontale corrente e può essere trascinata per modificarla direttamente". |
    | Area a sinistra della pagina   | "Sposta la posizione orizzontale a sinistra di un paio di colonne"                              |
    | Area a destra della pagina  | "Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente".   |

    

     

-   [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la proprietà **Name** dipende dalla parte della barra di scorrimento su cui viene eseguita una query.

    I nomi delle parti di una barra di scorrimento verticale sono i seguenti.

    | Parte                | Nome        |
    |---------------------|-------------|
    | Finestra della barra di scorrimento   | Verticale  |
    | Pulsante freccia in alto    | "Riga su"   |
    | Pulsante freccia in basso | "Linea in basso" |
    | Cursore di scorrimento        | Posizione  |
    | Area di paging      | "PGSU"   |
    | Area in basso    | "PGGIÙ" |

    

     

    I nomi delle parti di una barra di scorrimento orizzontale sono i seguenti.

    

    | Parte               | Nome           |
    |--------------------|----------------|
    | Finestra della barra di scorrimento  | Orizzontale   |
    | Pulsante freccia sinistra  | "Colonna a sinistra"  |
    | Pulsante freccia destra | "Colonna a destra" |
    | Cursore di scorrimento       | Posizione     |
    | Area a destra della pagina  | "Pagina a destra"   |
    | Area a sinistra della pagina   | "Pagina a sinistra"    |

    

     

-   [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la proprietà **Parent** dei pulsanti di direzione, il cursore di scorrimento e l'area ombreggiata su entrambi i lati del cursore sono la finestra della barra di scorrimento. La proprietà **Parent** della finestra della barra di scorrimento è una finestra ( \_ finestra del sistema \_ di ruoli) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe Window.
-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la proprietà **Role** dipende dalla parte della barra di scorrimento su cui viene eseguita una query. Le parti di una barra di scorrimento hanno i ruoli seguenti. 

    | Parte                                                  | Ruolo                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Barra di scorrimento stessa                                     | [**\_barra di \_ scorrimento sistema ruolo**](object-roles.md)   |
    | Pulsanti freccia in alto, in basso, a sinistra e a destra              | [**\_pulsante sistema \_ ruolo**](object-roles.md) |
    | Cursore di scorrimento                                          | [**\_indicatore del sistema di ruolo \_**](object-roles.md)   |
    | PGSU, PGGIÙ, pagina a sinistra e pagina a destra | [**\_pulsante sistema \_ ruolo**](object-roles.md) |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la proprietà **state** di ogni componente della barra di scorrimento include una combinazione dei [valori](object-state-constants.md)seguenti.

    | State                                                                                 | Valore                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**sistema di stato \_ \_ invisibile**](object-state-constants.md)     | Per la barra di scorrimento, indica che la barra di scorrimento verticale o orizzontale specificata non esiste. Per le aree PGSU o PGGIÙ, questo indica che il cursore è posizionato in modo tale che l'area non esiste. |
    | [**\_Offscreen sistema di stato \_**](object-state-constants.md)     | Per la barra di scorrimento, indica che la finestra è dimensionata in modo tale che la barra di scorrimento verticale o orizzontale specificata non sia attualmente visualizzata.                                                                         |
    | [**sistema di stato \_ \_ premuto**](object-state-constants.md)         | Viene premuto il pulsante freccia o l'area della pagina.                                                                                                                                                                                 |
    | [**sistema di stato non \_ \_ disponibile**](object-state-constants.md) | Il componente è disabilitato.                                                                                                                                                                                                  |

    

     

-   [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la proprietà **value** per la finestra della barra di scorrimento indica la posizione della barra di scorrimento e è una stringa che contiene un numero intero compreso tra "0" e "100".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 