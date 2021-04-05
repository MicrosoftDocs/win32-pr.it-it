---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855838"
---
# <a name="uianameshouldnotcontaincontroltype"></a><span data-ttu-id="fc18e-103">UiaNameShouldNotContainControlType</span><span class="sxs-lookup"><span data-stu-id="fc18e-103">UiaNameShouldNotContainControlType</span></span>

## <a name="text"></a><span data-ttu-id="fc18e-104">Testo</span><span class="sxs-lookup"><span data-stu-id="fc18e-104">Text</span></span>

<span data-ttu-id="fc18e-105">Il nome dell'elemento ( {0} ) non deve contenere il testo di ControlType ( {1} )</span><span class="sxs-lookup"><span data-stu-id="fc18e-105">Element's Name ({0}) should not contain the text of the ControlType ({1})</span></span>

## <a name="type"></a><span data-ttu-id="fc18e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc18e-106">Type</span></span>

<span data-ttu-id="fc18e-107">Avviso</span><span class="sxs-lookup"><span data-stu-id="fc18e-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="fc18e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc18e-108">Description</span></span>

<span data-ttu-id="fc18e-109">Il nome di un elemento incorpora il tipo di controllo UIA.</span><span class="sxs-lookup"><span data-stu-id="fc18e-109">The name of an element incorporates its UIA control type.</span></span> <span data-ttu-id="fc18e-110">Questo avviso può verificarsi, ad esempio, se la proprietà nome dell'interfaccia utente per un elemento con il tipo di controllo Button è impostata su "My Button".</span><span class="sxs-lookup"><span data-stu-id="fc18e-110">For example, this warning can occur if the UIA Name property for an element with the Button control type is set to "My Button".</span></span>

<span data-ttu-id="fc18e-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché il tipo di controllo verrà letto due volte o potrebbe non essere pronunciabile o non intuitivo per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="fc18e-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the control type will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="fc18e-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="fc18e-112">Possible causes</span></span>

-   <span data-ttu-id="fc18e-113">All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.</span><span class="sxs-lookup"><span data-stu-id="fc18e-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="fc18e-114">L'elemento o il relativo padre ha un nome predefinito che non è stato modificato in un nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="fc18e-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="fc18e-115">Ad esempio, button1.</span><span class="sxs-lookup"><span data-stu-id="fc18e-115">For example, button1.</span></span>
-   <span data-ttu-id="fc18e-116">Uno sviluppatore non è A conoscenza dello schermo che legge i nomi e i tipi di controllo.</span><span class="sxs-lookup"><span data-stu-id="fc18e-116">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc18e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc18e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc18e-118">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="fc18e-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="fc18e-119">**IUIAutomationElement:: currentname**</span><span class="sxs-lookup"><span data-stu-id="fc18e-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




