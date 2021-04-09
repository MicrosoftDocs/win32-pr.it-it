---
title: Attributi di ambiente
description: Attributi di ambiente
ms.assetid: 9dc8c770-4de3-42d8-b388-4426a4b0e788
keywords:
- Interfacce di Media Player di Windows, attributi di ambiente
- interfacce, attributi di ambiente
- riferimento per le interfacce, gli attributi di ambiente
- attributi di ambiente
- attributi, ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5157dc3cbb528cf546ff91d879d00c9b3ec2de8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855726"
---
# <a name="ambient-attributes"></a>Attributi di ambiente

Gli attributi e i metodi di ambiente sono supportati da tutti gli elementi dell'interfaccia appropriati, tranne nei casi indicati.

Gli attributi seguenti sono di ambiente.



| Attributo                                                        | Descrizione                                                                                                                               |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [accName](ambientattributes-accname.md)                         | Specifica o recupera un nome per qualsiasi elemento.                                                                                            |
| [accDescription](ambientattributes-accdescription.md)           | Specifica o Recupera una descrizione per qualsiasi elemento.                                                                                     |
| [accKeyboardShortcut](ambientattributes-acckeyboardshortcut.md) | Specifica o Recupera una descrizione del tasto di scelta rapida per qualsiasi elemento.                                                                   |
| [alphaBlend](ambientattributes-alphablend.md)                   | Specifica o recupera un valore per la fusione alfa di qualsiasi **visualizzazione**, **vista** o widget dell'interfaccia utente.                                                |
| [parte inferiore](ambientattributes-bottom.md)                           | Specifica o recupera la coordinata inferiore del controllo.                                                                              |
| [clippingColor](ambientattributes-clippingcolor.md)             | Specifica o Recupera il colore da ritagliare dalla bitmap **clippingImage** .                                                           |
| [clippingImage](ambientattributes-clippingimage.md)             | Specifica o recupera l'area in cui ritagliare il controllo.                                                                                 |
| [elementType](ambientattributes-elementtype.md)                 | Recupera il tipo dell'elemento (ad esempio, **Button**).                                                                             |
| [abilitato](ambientattributes-enabled.md)                         | Specifica o recupera un valore che indica se il controllo è abilitato o disabilitato.                                                     |
| [height](ambientattributes-height.md)                           | Specifica o recupera l'altezza del controllo.                                                                                         |
| [horizontalAlignment](ambientattributes-horizontalalignment.md) | Specifica o recupera un valore che indica la posizione orizzontale del controllo quando la **visualizzazione** o la **Sottovisualizzazione** padre viene ridimensionata. |
| [id](ambientattributes-id.md)                                   | Specifica o recupera l'identificatore di un controllo. Può essere impostato solo in fase di progettazione.                                                       |
| [sinistra](ambientattributes-left.md)                               | Specifica o recupera la coordinata sinistra del controllo.                                                                                |
| [nineGridMargins](ambientattributes-ninegridmargins.md)         | Specifica le larghezze dei margini per il ridimensionamento non uniforme dell'elemento Skin.                                                                      |
| [Pass-through](ambientattributes-passthrough.md)                 | Specifica o recupera un valore che indica se il controllo passerà tutti gli eventi del mouse al controllo sottostante.                 |
| [resizeImages](ambientattributes-resizeimages.md)               | Specifica o recupera un valore che indica se le immagini contenute nel controllo vengono ridimensionate automaticamente quando si modifica la dimensione del controllo.     |
| [Ok](ambientattributes-right.md)                             | Specifica o recupera la coordinata destra del controllo.                                                                               |
| [tabStop](ambientattributes-tabstop.md)                         | Specifica o recupera un valore che indica se il controllo sarà nell'ordine di tabulazione.                                               |
| [top](ambientattributes-top.md)                                 | Specifica o recupera la coordinata superiore del controllo.                                                                                 |
| [verticalAlignment](ambientattributes-verticalalignment.md)     | Specifica o recupera un valore che indica la posizione verticale del controllo quando la **visualizzazione** o la **Sottovisualizzazione** padre viene ridimensionata.   |
| [visibile](ambientattributes-visible.md)                         | Specifica o recupera la visibilità del controllo.                                                                                     |
| [width](ambientattributes-width.md)                             | Specifica o recupera la larghezza del controllo.                                                                                          |
| [zIndex](ambientattributes-zindex.md)                           | Specifica o recupera l'ordine in cui viene eseguito il rendering del controllo.                                                                        |



 

I metodi seguenti sono di ambiente.



| Metodo                                             | Descrizione                                                                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [alphaBlendTo](ambientattributes-alphablendto.md) | Regola la proprietà **alphaBlend** per un periodo di tempo.                                                                                                           |
| [moveSizeTo](ambientattributes-movesizeto.md)     | Sposta il controllo e specifica una nuova dimensione per il controllo nella nuova posizione. Il controllo viene spostato e ridimensionato in modo animato nel periodo di tempo specificato. |
| [moveTo](ambientattributes-moveto.md)             | Sposta il controllo in una nuova posizione a una velocità lineare.                                                                                                               |
| [slideTo](ambientattributes-slideto.md)           | Sposta il controllo in una nuova posizione. Il controllo viene spostato in modo non lineare nel periodo di tempo specificato.                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




