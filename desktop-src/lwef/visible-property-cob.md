---
title: Proprietà Visible (oggetto Characters)
description: Informazioni sulla proprietà Visible dell'oggetto Characters, che restituisce un valore booleano che indica se il carattere è visibile.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396306"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="3008e-103">Proprietà Visible (oggetto Characters)</span><span class="sxs-lookup"><span data-stu-id="3008e-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="3008e-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3008e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3008e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3008e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3008e-106">Restituisce un valore booleano che indica se il carattere è visibile.</span><span class="sxs-lookup"><span data-stu-id="3008e-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="3008e-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="3008e-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="3008e-108">*agent\***. Characters(**"* CharacterID *"\*\*). Visibile*\*</span><span class="sxs-lookup"><span data-stu-id="3008e-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="3008e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3008e-109">Value</span></span> | <span data-ttu-id="3008e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3008e-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="3008e-111">True</span><span class="sxs-lookup"><span data-stu-id="3008e-111">True</span></span>  | <span data-ttu-id="3008e-112">Viene visualizzato il carattere .</span><span class="sxs-lookup"><span data-stu-id="3008e-112">The character is displayed.</span></span>            |
| <span data-ttu-id="3008e-113">Falso</span><span class="sxs-lookup"><span data-stu-id="3008e-113">False</span></span> | <span data-ttu-id="3008e-114">Il carattere è nascosto (non visibile).</span><span class="sxs-lookup"><span data-stu-id="3008e-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3008e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3008e-115">Remarks</span></span>

<span data-ttu-id="3008e-116">Questa proprietà indica se il frame del carattere viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3008e-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="3008e-117">Non significa necessariamente che sia presente un'immagine sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="3008e-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="3008e-118">Ad esempio, questa proprietà restituisce **True** anche quando il carattere è posizionato fuori dall'area di visualizzazione visibile o quando la cornice del carattere corrente non contiene immagini.</span><span class="sxs-lookup"><span data-stu-id="3008e-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="3008e-119">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="3008e-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="3008e-120">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3008e-120">This property is read-only.</span></span> <span data-ttu-id="3008e-121">Per rendere visibile o nascosto un carattere, usare i [**metodi Mostra**](show-method.md) [**o Nascondi.**](https://www.bing.com/search?q=**Hide**)</span><span class="sxs-lookup"><span data-stu-id="3008e-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




