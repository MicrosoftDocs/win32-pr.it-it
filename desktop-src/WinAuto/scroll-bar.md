---
title: Barra di scorrimento (riferimenti a elementi dell'interfaccia utente MSAA)
description: Le barre di scorrimento consentono all'utente di scegliere la direzione e la distanza per scorrere le informazioni in una finestra o in una casella di riepilogo correlata. Il nome della classe della finestra per una barra di scorrimento è \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6acb609ee56d6e766a2f94cf75406211741ba0a711699f4e8c912790dc71cffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734331"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Barra di scorrimento (riferimenti a elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **barra di scorrimento** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti barra di** scorrimento in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

Le barre di scorrimento consentono all'utente di scegliere la direzione e la distanza per scorrere le informazioni in una finestra o in una casella di riepilogo correlata. Il nome della classe della finestra per una barra di scorrimento è "SCROLLBAR".

Il contenuto delle [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dipende dal fatto che la barra di scorrimento sia verticale o orizzontale e da quale delle parti seguenti della barra di scorrimento viene eseguita una query dal client:

-   Barra di scorrimento
-   Pulsante freccia superiore o destra
-   Pulsante freccia in basso o a sinistra
-   Casella di scorrimento (casella di scorrimento)
-   La pagina verso l'alto o l'area destra della pagina
-   La pagina verso il basso o l'area sinistra della pagina

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una barra di scorrimento supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accDoDefaultAction:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)l'oggetto barra di scorrimento stesso e il cursore di scorrimento non supportano il **metodo accDoDefaultAction.**

    Per le altre parti della barra di scorrimento su una barra di scorrimento verticale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chiama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con il messaggio [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) con *wParam* impostato sui valori seguenti.

    

    | Pulsante/Area       | Vacola        |
    |---------------------|--------------|
    | Pulsante freccia in alto    | SB \_ LINEUP   |
    | Pulsante freccia inferiore | SB \_ LINEDOWN |
    | Pagina precedente area      | SB \_ PAGEUP   |
    | Pagina successiva area    | SB \_ PAGEDOWN |

    

     

    Per le altre parti della barra di scorrimento su una barra di scorrimento orizzontale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chiama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con il messaggio [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) con *wParam* impostato sui valori seguenti.

    

    | Pulsante/Area      | Valore         |
    |--------------------|---------------|
    | Pulsante freccia sinistra  | SB \_ LINELEFT  |
    | Pulsante freccia destra | SB \_ LINERIGHT |
    | Area a sinistra della pagina   | SB \_ PAGELEFT  |
    | Area a destra della pagina  | SB \_ PAGERIGHT |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una barra di scorrimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**get \_ accChildCount:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)la **proprietà ChildCount** per l'oggetto barra di scorrimento è cinque. Per le altre parti della barra di scorrimento, **la proprietà ChildCount** è zero.
-   [**get \_ accDefaultAction:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)l'oggetto barra di scorrimento stesso e il cursore di scorrimento non supportano la **proprietà DefaultAction.** La **proprietà DefaultAction** per i pulsanti freccia e le aree ombreggiate su entrambi i lati del cursore di scorrimento è "Press".
-   [**get \_ accDescription:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)la **proprietà Description** dipende dalla parte della barra di scorrimento su cui viene eseguita la query.

    Le parti di una barra di scorrimento verticale hanno le descrizioni seguenti.

    

    | Parte                | Descrizione                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Barra di scorrimento   | "Usato per modificare l'area di visualizzazione verticale"                                          |
    | Pulsante freccia in alto    | "Sposta la posizione verticale verso l'alto di una riga"                                           |
    | Pulsante freccia inferiore | "Sposta la posizione verticale verso il basso di una riga"                                         |
    | Scorrimento del cursore        | "Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente" |
    | Pagina precedente area      | "Sposta la posizione verticale verso l'alto di un paio di righe"                                  |
    | Pagina successiva area    | "Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente" |

    

     

    Le parti di una barra di scorrimento orizzontale hanno le descrizioni seguenti.

    

    | Parte               | Descrizione                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Barra di scorrimento  | "Usato per modificare l'area di visualizzazione orizzontale"                                          |
    | Pulsante freccia sinistra  | "Sposta la posizione orizzontale a sinistra di una colonna"                                       |
    | Pulsante freccia destra | "Sposta la posizione orizzontale a destra di una colonna"                                      |
    | Scorrimento del cursore       | "Indica la posizione orizzontale corrente e può essere trascinata per modificarla direttamente" |
    | Area a sinistra della pagina   | "Sposta la posizione orizzontale a sinistra di un paio di colonne"                              |
    | Area a destra della pagina  | "Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente"   |

    

     

-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accName:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)la **proprietà Name** dipende dalla parte della barra di scorrimento su cui viene eseguita la query.

    Le parti di una barra di scorrimento verticale hanno i nomi seguenti.

    | Parte                | Nome        |
    |---------------------|-------------|
    | Finestra della barra di scorrimento   | "Vertical"  |
    | Pulsante freccia in alto    | "Line up"   |
    | Pulsante freccia inferiore | "Riga in giù" |
    | Scorrimento del cursore        | "Position"  |
    | Pagina precedente area      | "Pagina precedente"   |
    | Pagina successiva area    | "Pagina successiva" |

    

     

    Le parti di una barra di scorrimento orizzontale hanno i nomi seguenti.

    

    | Parte               | Nome           |
    |--------------------|----------------|
    | Finestra della barra di scorrimento  | "Orizzontale"   |
    | Pulsante freccia SINISTRA  | "Colonna a sinistra"  |
    | Pulsante freccia destra | "Colonna a destra" |
    | Scorrimento della casella di scorrimento       | "Position"     |
    | Area a destra della pagina  | "Pagina a destra"   |
    | Area di sinistra della pagina   | "Pagina a sinistra"    |

    

     

-   [**get \_ accParent:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)la **proprietà Parent** dei pulsanti freccia, la casella di scorrimento e l'area ombreggiata su entrambi i lati del cursore è la finestra della barra di scorrimento. La **proprietà Parent** della finestra della barra di scorrimento è una finestra (ROLE SYSTEM WINDOW) che racchiude il controllo e ha lo stesso nome della proprietà Name e della classe della \_ \_ finestra. 
-   [**get \_ accRole:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)la **proprietà Role** dipende dalla parte della barra di scorrimento su cui viene eseguita la query. Le parti di una barra di scorrimento hanno i ruoli seguenti. 

    | Parte                                                  | Ruolo                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Barra di scorrimento                                     | [**BARRA \_ DI SCORRIMENTO \_ DEL SISTEMA RUOLO**](object-roles.md)   |
    | Pulsanti freccia in alto, in basso, a sinistra e a destra              | [**PULSANTE \_ PUSH DEL SISTEMA DI \_ RUOLI**](object-roles.md) |
    | Scorrimento della casella di scorrimento                                          | [**INDICATORE \_ DI SISTEMA DEL \_ RUOLO**](object-roles.md)   |
    | Pagina precedente, pagina giù, pagina a sinistra e a destra della pagina | [**PULSANTE \_ PUSH DEL SISTEMA DI \_ RUOLI**](object-roles.md) |

    

     

-   [**get \_ accState:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)la **proprietà State** di ogni componente della barra di scorrimento include una combinazione dei valori [seguenti.](object-state-constants.md)

    | State                                                                                 | Valore                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**SISTEMA \_ DI STATO \_ INVISIBILE**](object-state-constants.md)     | Per la barra di scorrimento, indica che la barra di scorrimento verticale o orizzontale specificata non esiste. Per le aree pagina su o pagina giù, indica che la casella di scorrimento è posizionata in modo che l'area non esista. |
    | [**STATE \_ SYSTEM \_ OFFSCREEN**](object-state-constants.md)     | Per la barra di scorrimento, indica che la finestra è ridimensionata in modo che la barra di scorrimento verticale o orizzontale specificata non sia attualmente visualizzata.                                                                         |
    | [**STATO \_ PREMUTO DAL \_ SISTEMA**](object-state-constants.md)         | Viene premuto il pulsante freccia o l'area della pagina.                                                                                                                                                                                 |
    | [**SISTEMA \_ DI STATO NON \_ DISPONIBILE**](object-state-constants.md) | Il componente è disabilitato.                                                                                                                                                                                                  |

    

     

-   [**get \_ accValue:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)la proprietà **Value** per la finestra della barra di scorrimento indica la posizione della barra di scorrimento ed è una stringa contenente un numero intero compreso tra "0" e "100".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 