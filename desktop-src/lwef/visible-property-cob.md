---
title: Proprietà Visible (oggetto characters)
description: Visible (proprietà)
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300727"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="2bd4f-103">Proprietà Visible (oggetto characters)</span><span class="sxs-lookup"><span data-stu-id="2bd4f-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="2bd4f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2bd4f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2bd4f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2bd4f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2bd4f-106">Restituisce un valore booleano che indica se il carattere è visibile.</span><span class="sxs-lookup"><span data-stu-id="2bd4f-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="2bd4f-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="2bd4f-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="2bd4f-108">\*agente \***. Caratteri (**"\* CharacterID *" \* *). Visibile**</span><span class="sxs-lookup"><span data-stu-id="2bd4f-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="2bd4f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd4f-109">Value</span></span> | <span data-ttu-id="2bd4f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bd4f-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="2bd4f-111">True</span><span class="sxs-lookup"><span data-stu-id="2bd4f-111">True</span></span>  | <span data-ttu-id="2bd4f-112">Viene visualizzato il carattere.</span><span class="sxs-lookup"><span data-stu-id="2bd4f-112">The character is displayed.</span></span>            |
| <span data-ttu-id="2bd4f-113">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd4f-113">False</span></span> | <span data-ttu-id="2bd4f-114">Il carattere è nascosto (non visibile).</span><span class="sxs-lookup"><span data-stu-id="2bd4f-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bd4f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bd4f-115">Remarks</span></span>

<span data-ttu-id="2bd4f-116">Questa proprietà indica se viene visualizzato il frame del carattere.</span><span class="sxs-lookup"><span data-stu-id="2bd4f-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="2bd4f-117">Non significa necessariamente che sia presente un'immagine sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2bd4f-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="2bd4f-118">Questa proprietà, ad esempio, restituisce **true** anche quando il carattere è posizionato all'esterno dell'area di visualizzazione visibile o quando il frame di caratteri corrente non contiene immagini.</span><span class="sxs-lookup"><span data-stu-id="2bd4f-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="2bd4f-119">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="2bd4f-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="2bd4f-120">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2bd4f-120">This property is read-only.</span></span> <span data-ttu-id="2bd4f-121">Per rendere un carattere visibile o nascosto, utilizzare i metodi [**Mostra**](show-method.md) o [**Nascondi**](https://www.bing.com/search?q=**Hide**) .</span><span class="sxs-lookup"><span data-stu-id="2bd4f-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




