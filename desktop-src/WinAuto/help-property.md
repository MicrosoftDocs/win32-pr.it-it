---
title: Proprietà della Guida
description: La proprietà Help fornisce informazioni che indicano all'utente la funzione di un oggetto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329724"
---
# <a name="help-property"></a><span data-ttu-id="ec7e0-103">Proprietà della Guida</span><span class="sxs-lookup"><span data-stu-id="ec7e0-103">Help Property</span></span>

<span data-ttu-id="ec7e0-104">La proprietà **Help** fornisce informazioni che indicano all'utente la funzione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-104">The **Help** property provides information that tells the user about the function of an object.</span></span>

<span data-ttu-id="ec7e0-105">La proprietà della **Guida** viene recuperata chiamando [**IAccessible:: Get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span><span class="sxs-lookup"><span data-stu-id="ec7e0-105">The **Help** property is retrieved by calling [**IAccessible::get\_accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span></span>

<span data-ttu-id="ec7e0-106">Questa proprietà contiene informazioni di tipo Balloon (disponibili nelle descrizioni comandi) utilizzate per descrivere le operazioni svolte dall'oggetto o come utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-106">This property contains balloon-style information (as found in ToolTips) that is used either to describe what the object does or how to use it.</span></span> <span data-ttu-id="ec7e0-107">Ad esempio, la proprietà **Help** per un pulsante della barra degli strumenti che mostra una stampante potrebbe fornire il testo seguente: "Prints the current document".</span><span class="sxs-lookup"><span data-stu-id="ec7e0-107">For example, the **Help** property for a toolbar button that shows a printer might provide the following text: "Prints the current document."</span></span>

<span data-ttu-id="ec7e0-108">Non è necessario che il testo della proprietà della **Guida** sia univoco all'interno dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-108">The text for the **Help** property does not have to be unique within the user interface.</span></span>

## <a name="when-to-support-the-help-property"></a><span data-ttu-id="ec7e0-109">Quando supportare la proprietà della Guida</span><span class="sxs-lookup"><span data-stu-id="ec7e0-109">When to Support the Help Property</span></span>

<span data-ttu-id="ec7e0-110">I server non supportano la proprietà della **Guida** se altre proprietà forniscono informazioni sufficienti sullo scopo dell'oggetto e sulle azioni eseguite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-110">Servers do not support the **Help** property if other properties provide sufficient information about the object's purpose and the actions the object performs.</span></span> <span data-ttu-id="ec7e0-111">Gli oggetti accessibili che espongono i controlli forniti dal sistema non supportano la proprietà della **Guida** .</span><span class="sxs-lookup"><span data-stu-id="ec7e0-111">Accessible objects that expose system-provided controls do not support the **Help** property.</span></span>

 

 




