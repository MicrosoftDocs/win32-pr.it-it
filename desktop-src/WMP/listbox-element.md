---
title: LISTBOX (elemento)
description: LISTBOX (elemento)
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Windows Media Player Skin, elemento LISTBOX
- interfacce, elemento LISTBOX
- LISTBOX (elemento)
- riferimento per le interfacce, elemento LISTBOX
- elementi, LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044501"
---
# <a name="listbox-element"></a>LISTBOX (elemento)

L'elemento **ListBox** consente agli utenti di selezionare gli elementi da un elenco. Questi elementi possono essere specificati usando gli elementi **elemento** come elementi figlio dell'elemento **ListBox** . Se è necessario un controllo casella di riepilogo visualizzato solo quando necessario, utilizzare l'elemento **popup** , che è identico all'elemento **ListBox** , ad eccezione del valore predefinito dell'attributo **popup** , che determina il comportamento di visualizzazione.

L'elemento **ListBox** supporta gli attributi seguenti.



| Attributo                                        | Descrizione                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](listbox-backgroundcolor.md)   | Specifica o Recupera il colore di sfondo nel controllo casella di riepilogo.                                                  |
| [bordo](listbox-border.md)                     | Specifica o recupera un valore che indica se il controllo casella di riepilogo presenta un bordo. Può essere impostato solo in fase di progettazione.  |
| [firstVisibleItem](listbox-firstvisibleitem.md) | Specifica o recupera l'indice della prima riga visibile nel controllo casella di riepilogo.                                   |
| [focusItem](listbox-focusitem.md)               | Specifica o recupera la riga che contiene lo stato attivo.                                                                  |
| [fontFace](listbox-fontface.md)                 | Specifica o Recupera il tipo di carattere per il controllo casella di riepilogo.                                                             |
| [fontSize](listbox-fontsize.md)                 | Specifica o recupera le dimensioni del carattere per il controllo casella di riepilogo.                                                        |
| [fontStyle](listbox-fontstyle.md)               | Specifica o recupera lo stile del carattere per il controllo casella di riepilogo.                                                       |
| [foregroundColor](listbox-foregroundcolor.md)   | Specifica o Recupera il colore del testo nel controllo casella di riepilogo.                                                        |
| [itemCount](listbox-itemcount.md)               | Recupera il numero di elementi nel controllo casella di riepilogo.                                                                |
| [multiSelect](listbox-multiselect.md)           | Specifica o recupera un valore che indica se l'utente può selezionare più righe. Può essere impostato solo in fase di progettazione. |
| [popUp](listbox-popup.md)                       | Specifica un valore che indica se l'elemento rappresenta un controllo popup o una casella di riepilogo.                              |
| [readOnly](listbox-readonly.md)                 | Specifica o recupera un valore che indica se il testo è di sola lettura o se il testo può essere selezionato dall'utente.              |
| [selectedItem](listbox-selecteditem.md)         | Specifica o recupera l'indice dell'elemento selezionato nel controllo casella di riepilogo.                                        |
| [ordinati](listbox-sorted.md)                     | Specifica o recupera un valore che indica se il controllo casella di riepilogo è ordinato in ordine alfabetico.                      |



 

L'elemento **ListBox** supporta i metodi seguenti.



| Metodo                                                 | Descrizione                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [appendItem](listbox-appenditem.md)                   | Inserisce nuovo testo alla fine del controllo casella di riepilogo.                                                                  |
| [deleteAll](listbox-deleteall.md)                     | Elimina tutti gli elementi dal controllo casella di riepilogo.                                                                          |
| [deleteItem](listbox-deleteitem.md)                   | Elimina l'elemento di controllo della casella di riepilogo in corrispondenza dell'indice specificato.                                                             |
| [respingere](listbox-dismiss.md)                         | Nasconde il controllo.                                                                                                    |
| [findItem](listbox-finditem.md)                       | Cerca una determinata stringa a partire dall'elemento che segue l'indice dell'elemento specificato.                                |
| [getItem](listbox-getitem.md)                         | Recupera il testo per l'elemento con l'indice specificato.                                                             |
| [getNextSelectedItem](listbox-getnextselecteditem.md) | Recupera il successivo elemento selezionato nel controllo casella di riepilogo a partire dall'elemento dopo quello con l'indice specificato. |
| [insertItem](listbox-insertitem.md)                   | Inserisce il testo specificato in corrispondenza dell'indice specificato nel controllo casella di riepilogo.                                            |
| [replaceItem](listbox-replaceitem.md)                 | Sostituisce il testo in corrispondenza dell'indice specificato con il testo specificato.                                                     |
| [setSelectedState](listbox-setselectedstate.md)       | Seleziona o deseleziona l'elemento con l'indice specificato.                                                               |
| [show](listbox-show.md)                               | Visualizza il controllo.                                                                                                 |



 

> [!Note]  
> Questo elemento richiede Windows Media Player per Windows XP o versione successiva.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elemento POPUP**](popup-element.md)
</dt> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




