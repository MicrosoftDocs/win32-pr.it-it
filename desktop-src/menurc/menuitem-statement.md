---
title: MENUITEM (istruzione)
description: Definisce una voce di menu.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menu di istruzioni MENUITEM e altre risorse
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299263"
---
# <a name="menuitem-statement"></a>MENUITEM (istruzione)

Definisce una voce di menu.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Nome della voce di menu.

La stringa può contenere i caratteri di escape **\\ t** e **\\ un oggetto**. Il carattere **\\ t** inserisce una scheda nella stringa e viene utilizzata per allineare il testo nelle colonne. I caratteri di tabulazione devono essere utilizzati solo nei menu, non nelle barre dei menu. Per informazioni sui menu, vedere [**risorsa popup**](popup-resource.md). Il carattere **\\ a** è allineato a tutto il testo che lo segue scaricando direttamente dalla barra dei menu o dal menu a comparsa.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*risultato*
</dt> <dd>

Numero che specifica il risultato generato quando l'utente seleziona la voce di menu. Questo parametro accetta un valore integer. I risultati dei menu-item sono sempre numeri interi. Quando l'utente fa clic sul nome del menu-elemento, il risultato viene inviato alla finestra che possiede il menu.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*opzione*
</dt> <dd>

Aspetto della voce di menu. Questo parametro facoltativo accetta una o più delle seguenti opzioni di menu ridefinite, separate da virgole o spazi.



| Opzione           | Descrizione                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SELEZIONATA**      | Accanto alla voce di menu è presente un segno di spunta.                                                                                                                                |
| **IN grigio**       | La voce di menu inizialmente è inattiva e viene visualizzata nel menu in grigio o in una sfumatura schiarita del colore del testo del menu. Questa opzione non può essere usata con l'opzione **inactive** . |
| **Guida**         | Identifica un elemento della guida. Questa opzione non ha alcun effetto sull'aspetto della voce di menu.                                                                                 |
| **INATTIVO**     | La voce di menu viene visualizzata, ma non è possibile selezionarla. Questa opzione non può essere usata con l'opzione **grigio** .                                                              |
| **MENUBARBREAK** | Analogamente a **MENUBREAK** , ad eccezione del fatto che per i menu popup, separa la nuova colonna dalla colonna precedente con una linea verticale.                                             |
| **MENUBREAK**    | Inserisce la voce di menu in una nuova riga per gli elementi statici della barra dei menu. Per i menu, inserisce la voce di menu in una nuova colonna senza linea di separazione tra le colonne.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**SEPARATORE MENUITEM**
</dt> <dd>

Il formato **separatore MenuItem** dell'istruzione **MenuItem** crea una voce di menu inattiva che funge da barra di divisione tra due voci di menu attive in un menu.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo delle istruzioni del **separatore** **MenuItem** e MenuItem:

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**POPUP**](popup-resource.md)
</dt> </dl>

 

 




