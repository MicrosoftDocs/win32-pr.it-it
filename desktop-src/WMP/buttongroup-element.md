---
title: Elemento BUTTONGROUP
description: Elemento BUTTONGROUP
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Windows Media Player Skin, elemento BUTTONGROUP
- interfacce, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- riferimento per le interfacce, elemento BUTTONGROUP
- elementi, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116905"
---
# <a name="buttongroup-element"></a>Elemento BUTTONGROUP

L'elemento **ButtonGroup** fornisce un modo per raggruppare diversi pulsanti all'interno di un'interfaccia. È possibile specificare questi pulsanti usando gli elementi **ButtonElement** come elementi figlio dell'elemento **ButtonGroup** .

L'elemento **ButtonGroup** supporta i seguenti attributi.



| Attributo                                              | Descrizione                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [buttonCount](buttongroup-buttoncount.md)             | Recupera il numero di pulsanti presenti in **ButtonGroup**.                                                                                                                                                                         |
| [cursor](buttongroup-cursor.md)                       | Specifica o Recupera il tipo di cursore visualizzato quando il mouse è posizionato su un pulsante in **ButtonGroup**.                                                                                                                  |
| [disabledImage](buttongroup-disabledimage.md)         | Specifica o Recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in **ButtonGroup**.                                                                                                             |
| [downImage](buttongroup-downimage.md)                 | Specifica o Recupera il nome dell'immagine che rappresenta lo stato di inattività di **ButtonGroup**.                                                                                                                                |
| [hoverDownImage](buttongroup-hoverdownimage.md)       | Specifica o Recupera il nome dell'immagine che rappresenta lo stato di spostamento verso il basso di un pulsante in **ButtonGroup**. Lo stato di spostamento verso il basso si verifica quando il pulsante è nello stato di inattività e l'utente passa il mouse su di esso con il mouse. |
| [hoverImage](buttongroup-hoverimage.md)               | Specifica o Recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse su un pulsante in **ButtonGroup**. Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato attivo e l'utente passa su di esso con il mouse.             |
| [hueShift](buttongroup-hueshift.md)                   | Specifica o recupera la quantità in base alla quale viene spostata la tonalità delle immagini **ButtonGroup** .                                                                                                                                    |
| [image](buttongroup-image.md)                         | Specifica o Recupera il nome dell'immagine che rappresenta i pulsanti di un **ButtonGroup**.                                                                                                                                     |
| [mappingImage](buttongroup-mappingimage.md)           | Specifica o Recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di **ButtonGroup**.                                                                                                                                |
| [radio](buttongroup-radio.md)                         | Specifica o recupera un valore che indica se **ButtonGroup** è costituito da pulsanti di opzione.                                                                                                                             |
| [saturazione](buttongroup-saturation.md)               | Specifica o Recupera il valore di saturazione delle immagini **ButtonGroup** .                                                                                                                                                      |
| [showBackground](buttongroup-showbackground.md)       | Specifica o recupera un valore che indica se **ButtonGroup** Visualizza solo i pulsanti oppure Visualizza la bitmap completa specificata nell'attributo **Image** .                                                              |
| [transparencyColor](buttongroup-transparencycolor.md) | Specifica o Recupera il colore trasparente delle immagini **ButtonGroup** .                                                                                                                                                     |



 

L'elemento **ButtonGroup** supporta i metodi seguenti.



| Metodo                                 | Descrizione                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [Clicca](buttongroup-click.md)         | Chiama il gestore dell'evento **OnClick** definito per l'oggetto **ButtonElement** con l'indice specificato. |
| [GetButton](buttongroup-getbutton.md) | Recupera l'oggetto **ButtonElement** con l'indice specificato.                                       |



 

L'elemento **ButtonGroup** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




