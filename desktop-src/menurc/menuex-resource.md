---
title: Risorsa MENUEX
description: Definisce il contenuto di una risorsa di menu. | Risorsa MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menu risorse MENUEX e altre risorse
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321825"
---
# <a name="menuex-resource"></a>Risorsa MENUEX

Definisce il contenuto di una risorsa di menu. Una risorsa di menu è una raccolta di informazioni che definiscono l'aspetto e la funzione di un menu dell'applicazione. Un menu è uno strumento di input speciale che consente a un utente di selezionare i comandi e aprire sottomenu da un elenco di voci di menu. Definisce inoltre quanto segue:

-   Identificatori della guida nei menu.
-   Identificatori nei menu.
-   Usare i flag di tipo **MFT \_ \** _ e i flag di stato _*MFS \_ \**_ . Per ulteriori informazioni su questi flag, vedere la struttura [_ *MENUITEMINFO* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)
</dt> <dd>

Definisce una voce di menu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Stringa contenente il testo per la voce di menu. Per ulteriori informazioni, vedere [**MenuItem**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*ID*
</dt> <dd>

Espressione numerica che indica l'identificatore della voce di menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*tipo*
</dt> <dd>

Espressione numerica che indica il tipo di voce di menu per usare i valori di tipo MFT predefiniti \_ \* , includere l'istruzione seguente nel file RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*stato*
</dt> <dd>

Espressione numerica che indica lo stato della voce di menu per usare i valori di stato MFS predefiniti \_ \* , includere l'istruzione seguente in. File RC:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)
</dt> <dd>

Definisce una voce di menu a cui è associato un sottomenu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Stringa contenente il testo per la voce di menu.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*ID*
</dt> <dd>

Espressione numerica che indica l'identificatore della voce di menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*tipo*
</dt> <dd>

Espressione numerica che indica il tipo di voce di menu per usare i valori di tipo MFT predefiniti \_ \* , includere l'istruzione seguente in. File RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*stato*
</dt> <dd>

Espressione numerica che indica lo stato della voce di menu per usare i valori di stato MFS predefiniti \_ \* , includere l'istruzione seguente nel file RC:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Espressione numerica che indica l'identificatore usato per identificare il menu durante l'elaborazione della [**\_ Guida WM**](../shell/wm-help.md) .

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Contiene qualsiasi combinazione di istruzioni [**MenuItem**](menuitem-statement.md) e [**popup**](popup-resource.md) .

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

Le operazioni aritmetiche e booleane valide che possono essere contenute in qualsiasi espressione numerica nelle istruzioni di **menuex** sono le seguenti:

-   Aggiungi (' +')
-   Subtract ('-')
-   Meno unario ('-')
-   NOT unario (' ~')
-   E (' &')
-   O (' \| ')

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di menu](./using-menus.md)
</dt> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**DIALOGO**](dialog-resource.md)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**POPUP**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 
