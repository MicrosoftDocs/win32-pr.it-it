---
title: Annotazione mappa valori
description: Annotazione mappa valori
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d21b04374344475689989c2570af6975dc97c13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104565580"
---
# <a name="value-map-annotation"></a>Annotazione mappa valori

Con l'annotazione della mappa dei valori è possibile usare una stringa di mapping per indicare in che modo l'indice di immagine di un elemento in una visualizzazione elenco o in una visualizzazione albero corrisponde al relativo ruolo o stato. Una stringa di mapping, ad esempio, può indicare che l'indice immagine 0 di una visualizzazione elenco è mappato a un ruolo di casella di controllo, mentre l'indice di immagine 1 viene mappato a un ruolo di pulsante di opzione.

È anche possibile usare l'annotazione della mappa dei valori per specificare le stringhe mappate ai valori numerici su un dispositivo di scorrimento.

## <a name="when-to-use-this-technique"></a>Quando usare questa tecnica

Si consiglia di utilizzare l'annotazione della mappa di valori nelle situazioni seguenti.

-   Quando una visualizzazione elenco disegnata dal proprietario o una visualizzazione albero incorpora l'utilizzo di immagini e si desidera fornire una descrizione accessibile personalizzata (proprietà [**Description**](description-property.md) ) basata sull'immagine. La figura seguente mostra un esempio.

    ![illustrazione del menu Start, in cui le icone forniscono gli indizi visivi al contenuto](images/iconlist.gif)

-   Quando una visualizzazione elenco disegnata dal proprietario o un controllo di visualizzazione ad albero incorpora l'utilizzo di immagini per fare in modo che la struttura ad albero o gli elementi di elenco fungano da controlli semplici, in genere caselle di controllo o pulsanti di opzione e si desidera eseguire il mapping dell'immagine a un ruolo. Lo screenshot seguente mostra un esempio.

    ![screenshot delle opzioni di Internet Explorer per l'impostazione del valore di caselle di controllo e pulsanti di opzione](images/customlist.gif)

-   Quando si usa un dispositivo di scorrimento per selezionare un valore che può essere descritto come un valore diverso da un numero intero semplice, come illustrato nella schermata seguente, in cui l'impostazione di risoluzione dello schermo è descritta da una stringa.

    ![Screenshot di un dispositivo di scorrimento usato per impostare la risoluzione dello schermo](images/slider.gif)

Con l'annotazione della mappa di valori, una stringa di mapping indica il modo in cui l'indice dell'immagine o dell'albero dell'elenco corrisponde al relativo ruolo o stato. Oppure può indicare il modo in cui il valore numerico di un dispositivo di scorrimento corrisponde a una stringa. Una stringa di mapping, ad esempio, può indicare che l'indice immagine 0 di una visualizzazione elenco è mappato a un ruolo di casella di controllo e l'indice di immagine 1 viene mappato a un ruolo di pulsante di opzione. Usare [**IAccPropServices:: SetHwndPropStr ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) per alleghi la stringa di mapping al controllo.

Poiché è necessaria una conoscenza specifica del controllo per supportare il mapping dei valori, è disponibile un numero limitato di controlli e proprietà che supportano l'annotazione della mappa di valori, incluse le mappe dei valori di scorrimento, le visualizzazioni elenco e le visualizzazioni ad albero.

## <a name="slider-value-map"></a>Mappa del valore del dispositivo di scorrimento

**Propid \_ ACC \_ VALUEMAP** contiene un mapping dalle posizioni interne del dispositivo di scorrimento alle stringhe leggibili. Questa proprietà è supportata dal proxy del dispositivo di scorrimento Oleacc.dll. Se il valore del dispositivo di scorrimento corrente viene trovato nella mappa del valore, la stringa corrispondente verrà esposta come valore anziché come stringa di percentuale predefinita, ad esempio "50".

## <a name="list-view-and-tree-view"></a>Visualizzazione elenco e visualizzazione albero

**Propid \_ ACC \_ ROLEMAP**, **propid \_ ACC \_ STATEMAP** e **propid \_ ACC \_ DESCRIPTONMAP** forniscono i mapping tra gli indici di immagini di stato e i valori di ruolo e stato. Queste mappe consentono di eseguire il mapping degli indici di immagini ai ruoli appropriati (in genere il [**ruolo di sistema del ruolo \_ \_**](object-roles.md) o [**\_ \_ CHECKBUTTON**](object-roles.md)) e i bit di stato aggiuntivi, in genere [**controllati dal \_ sistema \_ di stato**](object-state-constants.md).

Per ulteriori informazioni sull'annotazione della mappa dei valori, vedere gli argomenti seguenti:

-   [Uso dell'annotazione della mappa di valori](using-value-map-annotation.md)
-   [Esempio di annotazione mappa di valori](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a>Formato mappa annotazioni

Nella tabella seguente vengono descritti i campi inclusi in una mappa delle annotazioni.



| Campo               | Descrizione                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Un                 | Indica che viene utilizzato uno schema di codifica specifico. I prefissi aggiuntivi possono essere supportati per gli schemi di codifica futuri.                                                                                                                                                          |
| Carattere delimitatore | In genere i due punti (:) viene usato, ma può essere un altro carattere eccetto **null** o uno spazio vuoto. Poiché questo carattere verrà utilizzato come delimitatore per i campi rimanenti, non può essere utilizzato come parte di un valore nella mappa.                                               |
| 0, 1 o 2          | Valore che indica quale chiave viene utilizzata. Per la visualizzazione albero e il ruolo Visualizzazione elenco e le mappe di stato, questa chiave può essere 0 (indice immagine), 1 (indice immagine stato) o 2 (indice immagine sovrapposta). Per i dispositivi di scorrimento e gli altri controlli che non offrono una scelta di chiavi, questo valore deve essere 0. |
| Carattere delimitatore | :                                                                                                                                                                                                                                                                             |
| Coppie chiave-valore     | Ogni coppia è costituita da una stringa chiave e da un carattere delimitatore. La stringa chiave è un numero e può essere in formato decimale o esadecimale (con prefisso "0x" iniziale).                                                                                                            |
| Stringa valore        | Per le mappe di valori, si tratta di una stringa. Per il ruolo e le mappe di stato, si tratta di un numero (decimale o esadecimale).                                                                                                                                                                         |
| Carattere delimitatore | :                                                                                                                                                                                                                                                                             |



 

Ad esempio, una mappa potrebbe essere simile alla seguente:


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



Quando questa mappa di valori viene applicata a un controllo dispositivo di scorrimento, il valore "warm" viene esposto quando il dispositivo di scorrimento si trova nella posizione 1. Poiché il valore 2 non è incluso in questo esempio, verrà esposto il valore predefinito per tale posizione. Per un dispositivo di scorrimento, il valore predefinito è un valore percentuale, ad esempio 33.

 

 




