---
title: Uso di sottoclassi di tema
description: Le classi di tema che rappresentano controlli quali ComboBox, Edit, ExplorerBar, Rebar, TAB e Toolbar possono essere sottoclassi per fornire variazioni del tema per quel particolare controllo.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710048"
---
# <a name="using-theme-subclasses"></a>Uso di sottoclassi di tema

Le classi di tema che rappresentano controlli quali ComboBox, Edit, ExplorerBar, Rebar, TAB e Toolbar possono essere sottoclassi per fornire variazioni del tema per quel particolare controllo. La classe **Button** , ad esempio, è sottoclassata come per `Start::Button` fornire il controllo sul tema applicato al pulsante **Avvia** .

> [!Note]  
> Prestare attenzione quando si creano sottoclassi come quelle descritte in questo argomento. Poiché le sottoclassi potrebbero essere modificate o non disponibili nelle versioni successive di Windows, non è consigliabile utilizzarle.

 

## <a name="two-ways-to-use-a-theme-subclass"></a>Due modi per usare una sottoclasse di tema

Un'applicazione può usare un tema sottoclassato in uno dei due modi seguenti:

-   Può usare la funzione [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) con una stringa del form `subclass::class` nel parametro *pszClassList* .
-   Può chiamare [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) con il nome della sottoclasse del tema nel parametro *pszSubAppName* .

## <a name="using-theme-messages-that-set-visual-style"></a>Uso di messaggi di tema che impostano lo stile di visualizzazione

Alcuni controlli, ad esempio Rebar e Toolbar, forniscono messaggi specifici che è possibile inviare per indicare al controllo di usare una sottoclasse di tema. Per questi controlli, fornire un puntatore a un buffer contenente il nome della sottoclasse del tema nel parametro *lParam* del messaggio. Usare il messaggio [**\_ SETWINDOWTHEME CCM**](ccm-setwindowtheme.md) generico oppure usare una variante specifica come quelle mostrate nella tabella seguente.



| Control    | Message                                             |
|------------|-----------------------------------------------------|
| Descrizione comando    | [**\_SETWINDOWTHEME TTM**](ttm-setwindowtheme.md)   |
| Barra degli strumenti    | [**TB \_ SETWINDOWTHEME**](tb-setwindowtheme.md)     |
| Rebar      | [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**\_SETWINDOWTHEME CBEM**](cbem-setwindowtheme.md) |



 

Nella tabella seguente sono elencate alcune delle sottoclassi definite da Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Classe</th>
<th>Sottoclassi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ComboBox</td>
<td><ul>
<li>Indirizzo</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>Modifica</td>
<td><ul>
<li>Indirizzo</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>InactiveSearchBoxEdit</li>
<li>InactiveSearchBoxEditComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
<li>MaxInactiveSearchBoxEdit</li>
<li>MaxInactiveSearchBoxEditComposited</li>
<li>MaxSearchBoxEdit</li>
<li>MaxSearchBoxEditComposited</li>
<li>SearchBoxEdit</li>
<li>SearchBoxEditComposited</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rebar</td>
<td><ul>
<li>BrowserTabBar</li>
<li>InactiveNavbar</li>
<li>InactiveNavbarComposited</li>
<li>MaxInactiveNavbar</li>
<li>MaxInactiveNavbarComposited</li>
<li>MaxNavbar</li>
<li>MaxNavbarComposited</li>
<li>Barra di navigazione</li>
<li>NavbarComposited</li>
<li>NavbarNonTopmost</li>
</ul></td>
</tr>
<tr class="even">
<td>Scheda</td>
<td><ul>
<li>BrowserTab</li>
</ul></td>
</tr>
<tr class="odd">
<td>Barra degli strumenti</td>
<td><ul>
<li>Go</li>
<li>GoComposited</li>
<li>InactiveGo</li>
<li>InactiveGoComposited</li>
<li>MaxGo</li>
<li>MaxGoComposited</li>
<li>MaxInactiveGo</li>
<li>MaxInactiveGoComposited</li>
<li>SearchButton</li>
<li>SearchButtonComposited</li>
<li>Viaggi</li>
<li>TravelComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a>Sottoclassi di Internet Explorer

In Windows Vista, le sottoclassi di determinate classi interne a Windows Internet Explorer ed Esplora risorse sono disponibili anche se le classi stesse non lo sono. Nella tabella seguente sono elencate le sottoclassi disponibili.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AddressBand</td>
<td><ul>
<li>AB</li>
<li>ABGreen</li>
<li>ABGreenComposited</li>
<li>ABRed</li>
<li>ABRedComposited</li>
<li>ABYellow</li>
<li>ABYellowComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>SearchBox</td>
<td><ul>
<li>InactiveSearchBox</li>
<li>InactiveSearchBoxComposited</li>
<li>MaxInactiveSearchBox</li>
<li>MaxInactiveSearchBoxComposited</li>
<li>MaxSearchBox</li>
<li>MaxSearchBoxComposited</li>
<li>SearchBoxComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente vengono illustrate le specifiche di queste classi.



| Control     | Parte         | Stati                                                 |
|-------------|--------------|--------------------------------------------------------|
| ADDRESSBAND | ABBACKGROUND | NORMAL (0x1), HOT (0x2), DISABLEd (0x3), FOCUSED (0x4) |
| SEARCHBOX   | SBBACKGROUND | NORMAL (0x1), HOT (0x2), DISABLEd (0x3), FOCUSED (0x4) |



 

 

 




