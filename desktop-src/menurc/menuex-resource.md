---
title: Risorsa MENUEX
description: Definisce il contenuto di una risorsa di menu. | Risorsa MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menu delle risorse MENUEX e altre risorse
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec78bd0d33b48b11de77fe7742affb4265160752ffad30d72ecf3e9c173bb77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825941"
---
# <a name="menuex-resource"></a>Risorsa MENUEX

Definisce il contenuto di una risorsa di menu. Una risorsa di menu è una raccolta di informazioni che definisce l'aspetto e la funzione di un menu dell'applicazione. Un menu è uno strumento di input speciale che consente a un utente di selezionare comandi e aprire sottomenu da un elenco di voci di menu. Definisce anche quanto segue:

-   Identificatori della Guida nei menu.
-   Identificatori nei menu.
-   Uso dei flag **MFT \_ \** _ type e dei flag _*di stato MFS. \_ \**_ Per altre informazioni su questi flag, vedere la [struttura _ *MENUITEMINFO.* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**Menuitem**](menuitem-statement.md)
</dt> <dd>

Definisce una voce di menu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Stringa contenente il testo per la voce di menu. Per altre informazioni, vedere [**MENUITEM**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Espressione numerica che indica l'identificatore della voce di menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*digitare*
</dt> <dd>

Espressione numerica che indica il tipo della voce di menu Per usare i valori di tipo MFT predefiniti, includere l'istruzione seguente \_ \* nel file RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Stato*
</dt> <dd>

Espressione numerica che indica lo stato della voce di menu Per usare i valori di stato MFS predefiniti, includere \_ \* l'istruzione seguente in . File RC:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**Popup**](popup-resource.md)
</dt> <dd>

Definisce una voce di menu a cui è associato un sottomenu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Stringa contenente il testo per la voce di menu.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Espressione numerica che indica l'identificatore della voce di menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*digitare*
</dt> <dd>

Espressione numerica che indica il tipo della voce di menu Per usare i valori di tipo MFT predefiniti, includere \_ \* l'istruzione seguente in . File RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Stato*
</dt> <dd>

Espressione numerica che indica lo stato della voce di menu Per usare i valori di stato MFS predefiniti, includere l'istruzione seguente \_ \* nel file RC:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Espressione numerica che indica l'identificatore utilizzato per identificare il menu durante [**l'elaborazione di WM \_ HELP.**](../shell/wm-help.md)

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Contiene qualsiasi combinazione di [**istruzioni MENUITEM**](menuitem-statement.md) [**e POPUP.**](popup-resource.md)

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

Le operazioni aritmetiche e booleane valide che possono essere contenute in qualsiasi espressione numerica nelle istruzioni **menuEX** sono le seguenti:

-   Aggiungi ('+')
-   Sottrazione ('-')
-   Unry minus ('-')
-   NOT uniri ('~')
-   AND ('&')
-   OR (' \| ')

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di menu](./using-menus.md)
</dt> <dt>

[**Acceleratori**](accelerators-resource.md)
</dt> <dt>

[**Caratteristiche**](characteristics-statement.md)
</dt> <dt>

[**Dialogo**](dialog-resource.md)
</dt> <dt>

[**Lingua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Menuitem**](menuitem-statement.md)
</dt> <dt>

[**Popup**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 
