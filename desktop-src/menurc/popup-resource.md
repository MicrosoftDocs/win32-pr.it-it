---
title: Risorsa POPUP
description: Definisce una voce di menu che può contenere voci di menu e sottomenu.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menu delle risorse POPUP e altre risorse
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f134b2d5801bc5003be6f45b42d13f1668c2e684b5f63fe0aed1f2c9c0400860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952341"
---
# <a name="popup-resource"></a>Risorsa POPUP

Definisce una voce di menu che può contenere voci di menu e sottomenu.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Stringa contenente il nome del menu. Questa stringa deve essere racchiusa tra virgolette doppie (**"**).

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*elenco di opzioni*
</dt> <dd>

Questo parametro specifica opzioni di menu ridefinite che specificano l'aspetto della voce di menu. Questo parametro facoltativo può essere uno o più degli elementi seguenti.



| Opzione           | Descrizione                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Controllato**      | Accanto alla voce di menu è visualizzato un segno di spunta. Questa opzione non è valida per un menu di primo livello.                                                                                 |
| **Grigio**       | La voce di menu è inizialmente inattiva e viene visualizzata nel menu in grigio o in una sfumatura chiara del colore del testo del menu. Questa opzione non può essere usata con **l'opzione INACTIVE.** |
| **Guida**         | Identifica un elemento della Guida. La voce di menu si trova nella posizione più a destra della barra dei menu.                                                                            |
| **Inattivo**     | La voce di menu viene visualizzata ma non può essere selezionata. Questa opzione non può essere usata con **l'opzione GRAYED.**                                                              |
| **MENUBARBREAK** | Come **MENUBREAK,** ad eccezione del fatto che per i menu popup, separa la nuova colonna dalla colonna precedente con una linea verticale.                                             |
| **MENUBREAK**    | Inserisce la voce di menu in una nuova riga per le voci della barra dei menu statiche. Per i menu, inserisce la voce di menu in una nuova colonna senza alcuna linea di divisione tra le colonne.           |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse](common-resource-attributes.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso **dell'istruzione POPUP:**

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Menuitem**](menuitem-statement.md)
</dt> </dl>

 

 




