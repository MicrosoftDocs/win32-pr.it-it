---
title: Istruzione MENUITEM
description: Definisce una voce di menu.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menu e altre risorse dell'istruzione MENUITEM
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bca50025e1c9136c22166d6d3f758c5c9b5819a9328d33d375195285f1d4f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092191"
---
# <a name="menuitem-statement"></a>Istruzione MENUITEM

Definisce una voce di menu.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Nome della voce di menu.

La stringa può contenere i caratteri di escape **\\ t** e **\\ .** Il **\\ carattere t** inserisce una tabulazione nella stringa e viene usato per allineare il testo nelle colonne. I caratteri di tabulazione devono essere usati solo nei menu, non nelle barre dei menu. Per informazioni sui menu, vedere [**Risorsa POPUP.**](popup-resource.md) Il **\\ carattere a** allinea tutto il testo che lo segue viene allineato direttamente alla barra dei menu o al menu a comparsa.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*Risultato*
</dt> <dd>

Numero che specifica il risultato generato quando l'utente seleziona la voce di menu. Questo parametro accetta un valore intero. I risultati delle voci di menu sono sempre numeri interi. Quando l'utente fa clic sul nome della voce di menu, il risultato viene inviato alla finestra proprietaria del menu.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*elenco di opzioni*
</dt> <dd>

Aspetto della voce di menu. Questo parametro facoltativo accetta una o più delle opzioni di menu ridefinite seguenti, separate da virgole o spazi.



| Opzione           | Descrizione                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Controllato**      | Accanto alla voce di menu è visualizzato un segno di spunta.                                                                                                                                |
| **Grigio**       | La voce di menu è inizialmente inattiva e viene visualizzata nel menu in grigio o in una sfumatura chiara del colore del testo del menu. Questa opzione non può essere usata con **l'opzione INACTIVE.** |
| **Guida**         | Identifica un elemento della Guida. Questa opzione non ha alcun effetto sull'aspetto della voce di menu.                                                                                 |
| **Inattivo**     | La voce di menu viene visualizzata ma non può essere selezionata. Questa opzione non può essere usata con **l'opzione GRAYED.**                                                              |
| **MENUBARBREAK** | Come **MENUBREAK,** ad eccezione del fatto che per i menu popup, separa la nuova colonna dalla colonna precedente con una linea verticale.                                             |
| **MENUBREAK**    | Inserisce la voce di menu in una nuova riga per le voci della barra dei menu statiche. Per i menu, inserisce la voce di menu in una nuova colonna senza alcuna linea di divisione tra le colonne.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**SEPARATORE MENUITEM**
</dt> <dd>

Il **formato MENUITEM SEPARATOR** dell'istruzione **MENUITEM** crea una voce di menu inattiva che funge da barra di divisione tra due voci di menu attive in un menu.

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso delle **istruzioni MENUITEM** e **MENUITEM SEPARATOR:**

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Popup**](popup-resource.md)
</dt> </dl>

 

 




