---
title: Proprietà Top (oggetto characters)
description: Top (proprietà)
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300804"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="db897-103">Proprietà Top (oggetto characters)</span><span class="sxs-lookup"><span data-stu-id="db897-103">Top Property (Characters Object)</span></span>

<span data-ttu-id="db897-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db897-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="db897-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="db897-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="db897-106">Restituisce o imposta il bordo superiore del frame del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="db897-106">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="db897-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="db897-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="db897-108">\*agente \***. Caratteri ("**_CharacterID_\*_")._ \*  \[  =  *Valore* superiore\]</span><span class="sxs-lookup"><span data-stu-id="db897-108">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="db897-109">Parte</span><span class="sxs-lookup"><span data-stu-id="db897-109">Part</span></span>    | <span data-ttu-id="db897-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db897-110">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="db897-111">*value*</span><span class="sxs-lookup"><span data-stu-id="db897-111">*value*</span></span> | <span data-ttu-id="db897-112">Valore long integer che specifica il bordo superiore del carattere.</span><span class="sxs-lookup"><span data-stu-id="db897-112">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db897-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="db897-113">Remarks</span></span>

<span data-ttu-id="db897-114">La proprietà **Top** è sempre espressa in pixel, in relazione all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="db897-114">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="db897-115">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="db897-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="db897-116">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="db897-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="db897-117">Usare il metodo [**MoveTo**](moveto-method.md) per modificare la posizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="db897-117">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="db897-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="db897-118">See Also</span></span>

<span data-ttu-id="db897-119">[**Proprietà Left**](left-property.md), [ **metodo MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="db897-119">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




