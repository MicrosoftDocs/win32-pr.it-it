---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- Identificatore UIA_NamePropertyId AutomationElement. proprietà NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396670"
---
# <a name="uianamelengthtoolong"></a><span data-ttu-id="ba2bb-104">UiaNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="ba2bb-104">UiaNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="ba2bb-105">Testo</span><span class="sxs-lookup"><span data-stu-id="ba2bb-105">Text</span></span>

<span data-ttu-id="ba2bb-106">Il nome dell'elemento non deve restituire una stringa più lunga di un {0} carattere</span><span class="sxs-lookup"><span data-stu-id="ba2bb-106">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="ba2bb-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba2bb-107">Type</span></span>

<span data-ttu-id="ba2bb-108">Errore</span><span class="sxs-lookup"><span data-stu-id="ba2bb-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="ba2bb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba2bb-109">Description</span></span>

<span data-ttu-id="ba2bb-110">Il nome di un elemento contiene troppi caratteri.</span><span class="sxs-lookup"><span data-stu-id="ba2bb-110">The name of an element contains too many characters.</span></span> <span data-ttu-id="ba2bb-111">Ad esempio, il metodo [**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) usato per recuperare il nome dell'elemento UIA di un elemento restituisce una stringa superiore al limite.</span><span class="sxs-lookup"><span data-stu-id="ba2bb-111">For example, the [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) method used to retrieve the UIA name of an element returns a string greater than the limit.</span></span>

<span data-ttu-id="ba2bb-112">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe avere un nome non pronunciabile e non intuitivo.</span><span class="sxs-lookup"><span data-stu-id="ba2bb-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ba2bb-113">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="ba2bb-113">Possible causes</span></span>

<span data-ttu-id="ba2bb-114">All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.</span><span class="sxs-lookup"><span data-stu-id="ba2bb-114">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba2bb-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba2bb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba2bb-116">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="ba2bb-116">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="ba2bb-117">**IUIAutomationElement:: currentname**</span><span class="sxs-lookup"><span data-stu-id="ba2bb-117">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




