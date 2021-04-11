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
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117061"
---
# <a name="popup-resource"></a>Risorsa POPUP

Definisce una voce di menu che può contenere voci di menu e sottomenu.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Stringa che contiene il nome del menu. Questa stringa deve essere racchiusa tra virgolette doppie (**"**).

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*opzione*
</dt> <dd>

Questo parametro specifica le opzioni di menu ridefinite che specificano l'aspetto della voce di menu. Questo parametro facoltativo può essere uno o più degli elementi seguenti.



| Opzione           | Descrizione                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SELEZIONATA**      | Accanto alla voce di menu è presente un segno di spunta. Questa opzione non è valida per un menu di primo livello.                                                                                 |
| **IN grigio**       | La voce di menu inizialmente è inattiva e viene visualizzata nel menu in grigio o in una sfumatura schiarita del colore del testo del menu. Questa opzione non può essere usata con l'opzione **inactive** . |
| **Guida**         | Identifica un elemento della guida. La voce di menu è posizionata in corrispondenza della posizione più a destra nella barra dei menu.                                                                            |
| **INATTIVO**     | La voce di menu viene visualizzata, ma non è possibile selezionarla. Questa opzione non può essere usata con l'opzione **grigio** .                                                              |
| **MENUBARBREAK** | Analogamente a **MENUBREAK** , ad eccezione del fatto che per i menu popup, separa la nuova colonna dalla colonna precedente con una linea verticale.                                             |
| **MENUBREAK**    | Inserisce la voce di menu in una nuova riga per gli elementi statici della barra dei menu. Per i menu, inserisce la voce di menu in una nuova colonna senza linea di separazione tra le colonne.           |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **popup** :

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

[**MENU**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> </dl>

 

 




