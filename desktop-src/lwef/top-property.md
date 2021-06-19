---
title: Proprietà Top (oggetto Characters)
description: Informazioni sulla proprietà Top (oggetto Characters). Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396346"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="18be9-104">Proprietà Top (oggetto Characters)</span><span class="sxs-lookup"><span data-stu-id="18be9-104">Top Property (Characters Object)</span></span>

<span data-ttu-id="18be9-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18be9-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="18be9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="18be9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="18be9-107">Restituisce o imposta il bordo superiore del frame del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="18be9-107">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="18be9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="18be9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="18be9-109">*agent\***. Caratteri ("**_CharacterID_*_"). Primo_ \*  \[  =  *valore*\]</span><span class="sxs-lookup"><span data-stu-id="18be9-109">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="18be9-110">Parte</span><span class="sxs-lookup"><span data-stu-id="18be9-110">Part</span></span>    | <span data-ttu-id="18be9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18be9-111">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="18be9-112">*value*</span><span class="sxs-lookup"><span data-stu-id="18be9-112">*value*</span></span> | <span data-ttu-id="18be9-113">Valore Long Integer che specifica il bordo superiore del carattere.</span><span class="sxs-lookup"><span data-stu-id="18be9-113">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18be9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="18be9-114">Remarks</span></span>

<span data-ttu-id="18be9-115">La **proprietà Top** è sempre espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="18be9-115">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="18be9-116">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="18be9-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="18be9-117">Anche se il carattere viene visualizzato in una finestra di area irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="18be9-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="18be9-118">Usare il [**metodo MoveTo**](moveto-method.md) per modificare la posizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="18be9-118">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="18be9-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="18be9-119">See Also</span></span>

<span data-ttu-id="18be9-120">[**Proprietà Left**](left-property.md), [ **metodo MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="18be9-120">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




