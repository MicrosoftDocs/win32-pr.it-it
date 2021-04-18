---
title: UI_PKEY_TooltipTitle
description: Identifica la proprietà TooltipTitle dell'interfaccia utente \_ pkey \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298605"
---
# <a name="ui_pkey_tooltiptitle"></a><span data-ttu-id="d9e29-103">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="d9e29-103">UI\_PKEY\_TooltipTitle</span></span>

<span data-ttu-id="d9e29-104">Identifica la proprietà TooltipTitle dell'interfaccia utente \_ pkey \_ .</span><span class="sxs-lookup"><span data-stu-id="d9e29-104">Identifies the UI\_PKEY\_TooltipTitle property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="d9e29-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9e29-105">Remarks</span></span>

<span data-ttu-id="d9e29-106">L'interfaccia utente \_ pkey \_ TooltipTitle viene utilizzata da un'applicazione per eseguire una query sulla descrizione comando di schede, gruppi, pulsanti, elementi della raccolta e altri controlli della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d9e29-106">UI\_PKEY\_TooltipTitle is used by an application to query the tooltip of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

<span data-ttu-id="d9e29-107">Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="d9e29-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="d9e29-108">Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="d9e29-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="d9e29-109">L'allineamento a destra non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d9e29-109">Right alignment is not supported.</span></span>

<span data-ttu-id="d9e29-110">La lunghezza massima dell'interfaccia utente \_ pkey \_ TooltipTitle è unbounded.</span><span class="sxs-lookup"><span data-stu-id="d9e29-110">The maximum length of UI\_PKEY\_TooltipTitle is unbounded.</span></span>

<span data-ttu-id="d9e29-111">Per visualizzare una e commerciale in una descrizione comando, eseguire l'escape della designazione del carattere speciale con una doppia e commerciale ( `&&` ), come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d9e29-111">To display an ampersand in a tooltip, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a><span data-ttu-id="d9e29-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9e29-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e29-113">Proprietà delle risorse</span><span class="sxs-lookup"><span data-stu-id="d9e29-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="d9e29-114">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="d9e29-114">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[<span data-ttu-id="d9e29-115">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="d9e29-115">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




