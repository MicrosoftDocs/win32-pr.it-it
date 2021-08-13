---
title: Controllo Slider (riferimenti a elementi dell'interfaccia utente MSAA)
description: Un controllo dispositivo di scorrimento, detto anche controllo trackbar, consente a un utente di selezionare da un intervallo di valori spostando un dispositivo di scorrimento. I controlli del volume disponibili nel sistema operativo Windows sono dispositivi di scorrimento.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d92799a8a644d5e5e00c695d628cb827ba60f73cc3a0d7b7f5dc505a6c2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564429"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Controllo Slider (riferimenti a elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Controllo Slider** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Controllo Slider** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

Un controllo dispositivo di scorrimento, detto anche controllo trackbar, consente a un utente di selezionare da un intervallo di valori spostando un dispositivo di scorrimento. I controlli del volume disponibili nel sistema operativo Windows sono dispositivi di scorrimento.

Il nome della classe della finestra per un controllo dispositivo di scorrimento è TRACKBAR CLASS, definito \_ come "msctls \_ trackbar" in Commctrl.h.

Il contenuto delle [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dipende dal fatto che il dispositivo di scorrimento sia verticale o orizzontale e su quale delle parti seguenti del controllo dispositivo di scorrimento viene eseguita una query dal client:

-   Finestra Dispositivo di scorrimento
-   Cursore del dispositivo di scorrimento
-   Area ombreggiata sopra (o a
-   Area ombreggiata sotto (o a destra) del cursore del dispositivo di scorrimento

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo dispositivo di scorrimento supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo dispositivo di scorrimento supporta le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)la proprietà **KeyboardShortcut** è il tasto di scelta della finestra del dispositivo di scorrimento, ovvero un carattere sottolineato nel testo dell'etichetta per il dispositivo di scorrimento. La stringa restituita contiene il carattere del tasto di scelta aggiunto alla stringa "Alt+".
-   [**get \_ accName:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)la **proprietà Name** dipende dalla parte del dispositivo di scorrimento su cui viene eseguita la query.

    Le parti di un dispositivo di scorrimento verticale hanno i nomi seguenti:

    

    | Parte del dispositivo di scorrimento                    | Nome                                |
    |--------------------------------|-------------------------------------|
    | Finestra Dispositivo di scorrimento                  | Controllo testo statico usato come etichetta |
    | Cursore del dispositivo di scorrimento                   | "Position"                          |
    | Area ombreggiata sopra il cursore del dispositivo di scorrimento | "Pagina precedente"                           |
    | Area ombreggiata sotto il cursore del dispositivo di scorrimento | "Pagina successiva"                         |

    

     

    Le parti di un dispositivo di scorrimento orizzontale hanno i nomi seguenti:

    

    | Parte del dispositivo di scorrimento                              | Nome                                |
    |------------------------------------------|-------------------------------------|
    | Finestra Dispositivo di scorrimento                            | Controllo testo statico usato come etichetta |
    | Cursore del dispositivo di scorrimento                             | "Position"                          |
    | Area ombreggiata a sinistra del cursore del dispositivo di scorrimento  | "Pagina a sinistra"                         |
    | Area ombreggiata a destra del cursore del dispositivo di scorrimento | "Pagina a destra"                        |

    

     

-   [**get \_ accParent:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)la **proprietà Parent** dei pulsanti freccia, del cursore di scorrimento e dell'area ombreggiata su entrambi i lati del cursore è la finestra del dispositivo di scorrimento. La **proprietà Parent** della finestra del dispositivo di scorrimento è una finestra ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra.
-   [**get \_ accRole:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)la **proprietà Role** dipende dalla parte del dispositivo di scorrimento su cui viene eseguita la query. 

    | Parte del dispositivo di scorrimento                                     | [Ruolo](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Finestra Dispositivo di scorrimento                                   | [**DISPOSITIVO DI \_ SCORRIMENTO SISTEMA \_ RUOLO**](object-roles.md)         |
    | Cursore del dispositivo di scorrimento                                    | [**INDICATORE \_ DEL SISTEMA DI \_ RUOLI**](object-roles.md)   |
    | Aree ombreggiate su entrambi i lati del cursore del dispositivo di scorrimento | [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md) |

    

     

-   [**get \_ accState:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)[i valori](object-state-constants.md) per la proprietà **State** dipendono dalla parte del dispositivo di scorrimento su cui viene eseguita la query. 

    | Parte del dispositivo di scorrimento                                     | Valori di stato possibili                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestra Dispositivo di scorrimento                                   | [**STATE \_ SYSTEM \_ INVISIBLE STATE**](object-state-constants.md) SYSTEM UNAVAILABLE STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md) |
    | Cursore del dispositivo di scorrimento                                    | Zero (0), che indica che l'oggetto è visibile o [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)                                                                                                                       |
    | Aree ombreggiate su entrambi i lati del cursore del dispositivo di scorrimento | Zero (0), che indica che l'oggetto è visibile o [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)                                                                                                                       |

    

     

-   [**get \_ accValue:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)la proprietà **Value** per la finestra del dispositivo di scorrimento indica la posizione del cursore ed è una stringa che contiene un numero intero compreso tra "0" e "100".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra di scorrimento**](scroll-bar.md)
</dt> </dl>

 

 




