---
title: Controllo Slider (riferimento all'elemento MSAA UI)
description: Un controllo dispositivo di scorrimento, detto anche controllo TrackBar, consente a un utente di selezionare da un intervallo di valori spostando un dispositivo di scorrimento. I controlli del volume disponibili nel sistema operativo Windows sono dispositivi di scorrimento.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045286"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Controllo Slider (riferimento all'elemento MSAA UI)

> [!Note]  
> In questo argomento vengono descritti gli oggetti **controllo dispositivo di scorrimento** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti **controllo dispositivo di scorrimento** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Un controllo dispositivo di scorrimento, detto anche controllo TrackBar, consente a un utente di selezionare da un intervallo di valori spostando un dispositivo di scorrimento. I controlli del volume disponibili nel sistema operativo Windows sono dispositivi di scorrimento.

Il nome della classe della finestra per un controllo dispositivo di scorrimento è la \_ classe TrackBar, definita come "msctls \_ TrackBar" in commctrl. h.

Il contenuto delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varia a seconda che il dispositivo di scorrimento sia verticale o orizzontale e che il client esegue una query sulle parti seguenti del controllo dispositivo di scorrimento:

-   Finestra del dispositivo di scorrimento
-   Cursore del dispositivo di scorrimento
-   Area ombreggiata sopra (o
-   Area ombreggiata sotto (o a destra di) il cursore del dispositivo di scorrimento

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo dispositivo di scorrimento supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo dispositivo di scorrimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): la proprietà **KeyboardShortcut** è la chiave di accesso della finestra del dispositivo di scorrimento, che è un carattere sottolineato nel testo dell'etichetta per il dispositivo di scorrimento. La stringa restituita contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la proprietà **Name** dipende dalla parte del dispositivo di scorrimento su cui viene eseguita una query.

    Le parti di un dispositivo di scorrimento verticale hanno i nomi seguenti:

    

    | Parte dispositivo di scorrimento                    | Nome                                |
    |--------------------------------|-------------------------------------|
    | Finestra del dispositivo di scorrimento                  | Controllo testo statico utilizzato come etichetta |
    | Cursore del dispositivo di scorrimento                   | Posizione                          |
    | Area ombreggiata sopra il cursore del dispositivo di scorrimento | "PGSU"                           |
    | Area ombreggiata sotto il cursore del dispositivo di scorrimento | "PGGIÙ"                         |

    

     

    Le parti di un dispositivo di scorrimento orizzontale hanno i nomi seguenti:

    

    | Parte dispositivo di scorrimento                              | Nome                                |
    |------------------------------------------|-------------------------------------|
    | Finestra del dispositivo di scorrimento                            | Controllo testo statico utilizzato come etichetta |
    | Cursore del dispositivo di scorrimento                             | Posizione                          |
    | Area ombreggiata a sinistra del cursore del dispositivo di scorrimento  | "Pagina a sinistra"                         |
    | Area ombreggiata a destra del cursore del dispositivo di scorrimento | "Pagina a destra"                        |

    

     

-   [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la proprietà **Parent** dei pulsanti di direzione, il cursore di scorrimento e l'area ombreggiata su entrambi i lati del controllo Thumb è la finestra del dispositivo di scorrimento. La proprietà **Parent** della finestra del dispositivo di scorrimento è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe Window.
-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la proprietà **Role** dipende dalla parte del dispositivo di scorrimento su cui viene eseguita una query. 

    | Parte dispositivo di scorrimento                                     | [Ruolo](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Finestra del dispositivo di scorrimento                                   | [**\_dispositivo di \_ scorrimento sistema ruolo**](object-roles.md)         |
    | Cursore del dispositivo di scorrimento                                    | [**\_indicatore del sistema di ruolo \_**](object-roles.md)   |
    | Aree ombreggiate su entrambi i lati del cursore del dispositivo di scorrimento | [**\_pulsante sistema \_ ruolo**](object-roles.md) |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate):[i valori](object-state-constants.md) per la proprietà **state** dipendono dalla parte del dispositivo di scorrimento su cui viene eseguita una query. 

    | Parte dispositivo di scorrimento                                     | Possibili valori di stato                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestra del dispositivo di scorrimento                                   | [**Stato \_ di sistema stato \_ invisibile**](object-state-constants.md) al sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema |
    | Cursore del dispositivo di scorrimento                                    | Zero (0), che indica che l'oggetto è visibile oppure che lo stato del sistema di stato [**\_ \_ invisibile**](object-state-constants.md) al sistema dello stato non è \| [**\_ \_ disponibile**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)                                                                                                                       |
    | Aree ombreggiate su entrambi i lati del cursore del dispositivo di scorrimento | Zero (0), che indica che l'oggetto è visibile oppure che lo stato del sistema di stato [**\_ \_ invisibile**](object-state-constants.md) al sistema dello stato non è \| [**\_ \_ disponibile**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)                                                                                                                       |

    

     

-   [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la proprietà **value** per la finestra del dispositivo di scorrimento indica la posizione del cursore e è una stringa che contiene un numero intero compreso tra "0" e "100".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra di scorrimento**](scroll-bar.md)
</dt> </dl>

 

 




