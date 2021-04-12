---
title: Oggetto Balloon
description: Oggetto Balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223560"
---
# <a name="the-balloon-object"></a><span data-ttu-id="f5971-103">Oggetto Balloon</span><span class="sxs-lookup"><span data-stu-id="f5971-103">The Balloon Object</span></span>

<span data-ttu-id="f5971-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5971-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f5971-105">Microsoft Agent supporta la didascalia testuale del metodo [**Speak**](speak-method.md) usando un fumetto di parole.</span><span class="sxs-lookup"><span data-stu-id="f5971-105">Microsoft Agent supports textual captioning of [**Speak**](speak-method.md) method using a cartoon word balloon.</span></span> <span data-ttu-id="f5971-106">Il metodo [**think**](think-method.md) consente di visualizzare testo senza output audio in un fumetto di parola "pensiero".</span><span class="sxs-lookup"><span data-stu-id="f5971-106">The [**Think**](think-method.md) method enables you to display text without audio output in a "thought" word balloon.</span></span>

<span data-ttu-id="f5971-107">Le impostazioni predefinite della finestra fumetto di Word iniziale di un carattere sono definite e compilate nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f5971-107">A character's initial word balloon window defaults are defined and compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f5971-108">Al termine dell'esecuzione, l'utente può eseguire l'override delle proprietà del [**tipo di carattere**](https://www.bing.com/search?q=**Font**) e [**abilitate**](enabled-property.md) per il fumetto.</span><span class="sxs-lookup"><span data-stu-id="f5971-108">Once running, the balloon's [**Enabled**](enabled-property.md) and [**Font**](https://www.bing.com/search?q=**Font**) properties may be overridden by the user.</span></span> <span data-ttu-id="f5971-109">Se un utente modifica le proprietà di Word Balloon, avrà effetto su tutti i caratteri.</span><span class="sxs-lookup"><span data-stu-id="f5971-109">If a user changes the word balloon's properties, they affect all characters.</span></span> <span data-ttu-id="f5971-110">Sia i [**fumetti di parole che quelli**](speak-method.md) [**di Word usano**](think-method.md) le stesse impostazioni delle proprietà per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f5971-110">Both the [**Speak**](speak-method.md) and [**Think**](think-method.md) word balloons use the same property settings for size.</span></span> <span data-ttu-id="f5971-111">È possibile accedere alle proprietà per la parola Balloon di un carattere tramite l'oggetto [**Balloon**](/windows/desktop/lwef/the-balloon-object) , che è un elemento figlio dell'oggetto [**character**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="f5971-111">You can access the properties for a character's word balloon through the [**Balloon**](/windows/desktop/lwef/the-balloon-object) object, which is a child of the [**Character**](/windows/desktop/lwef/the-characters-object) object.</span></span>

<span data-ttu-id="f5971-112">L'oggetto [**Balloon**](/windows/desktop/lwef/the-balloon-object) supporta le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5971-112">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object supports the following properties:</span></span>

-   [<span data-ttu-id="f5971-113">**BackColor**</span><span class="sxs-lookup"><span data-stu-id="f5971-113">**BackColor**</span></span>](backcolor-property.md)
-   [<span data-ttu-id="f5971-114">**ColoreBordo**</span><span class="sxs-lookup"><span data-stu-id="f5971-114">**BorderColor**</span></span>](bordercolor-property.md)
-   [<span data-ttu-id="f5971-115">**CharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="f5971-115">**CharsPerLine**</span></span>](charsperline-property.md)
-   [<span data-ttu-id="f5971-116">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="f5971-116">**Enabled**</span></span>](enabled-property.md)
-   [<span data-ttu-id="f5971-117">**FontCharSet**</span><span class="sxs-lookup"><span data-stu-id="f5971-117">**FontCharSet**</span></span>](fontcharset-property.md)
-   [<span data-ttu-id="f5971-118">**FontName**</span><span class="sxs-lookup"><span data-stu-id="f5971-118">**FontName**</span></span>](fontname-property-bal.md)
-   [<span data-ttu-id="f5971-119">**FontBold**</span><span class="sxs-lookup"><span data-stu-id="f5971-119">**FontBold**</span></span>](fontbold-property.md)
-   [<span data-ttu-id="f5971-120">**CarattereCorsivo**</span><span class="sxs-lookup"><span data-stu-id="f5971-120">**FontItalic**</span></span>](fontitalic-property.md)
-   [<span data-ttu-id="f5971-121">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="f5971-121">**FontSize**</span></span>](fontsize-property-bal.md)
-   [<span data-ttu-id="f5971-122">**FontStrikeThru**</span><span class="sxs-lookup"><span data-stu-id="f5971-122">**FontStrikeThru**</span></span>](fontstrikethru-property.md)
-   [<span data-ttu-id="f5971-123">**CarattereSottolineato**</span><span class="sxs-lookup"><span data-stu-id="f5971-123">**FontUnderline**</span></span>](fontunderline-property.md)
-   [<span data-ttu-id="f5971-124">**ColorePrimoPiano**</span><span class="sxs-lookup"><span data-stu-id="f5971-124">**ForeColor**</span></span>](forecolor-property.md)
-   [<span data-ttu-id="f5971-125">**NumberOfLines**</span><span class="sxs-lookup"><span data-stu-id="f5971-125">**NumberOfLines**</span></span>](numberoflines-property.md)
-   [<span data-ttu-id="f5971-126">**Stile**</span><span class="sxs-lookup"><span data-stu-id="f5971-126">**Style**</span></span>](style-property.md)
-   [<span data-ttu-id="f5971-127">**Visible**</span><span class="sxs-lookup"><span data-stu-id="f5971-127">**Visible**</span></span>](visible-property-bal.md)

 

 