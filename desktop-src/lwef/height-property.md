---
title: Proprietà Height (oggetto Characters)
description: Informazioni sulla proprietà Height dell'oggetto Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068512"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="5a844-104">Proprietà Height (oggetto Characters)</span><span class="sxs-lookup"><span data-stu-id="5a844-104">Height Property (Characters Object)</span></span>

<span data-ttu-id="5a844-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a844-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5a844-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5a844-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5a844-107">Restituisce o imposta l'altezza del frame del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="5a844-107">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="5a844-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="5a844-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5a844-109">*agent\***. Caratteri ("**_CharacterID_*_"). Valore_ \*  \[ =  *altezza*\]</span><span class="sxs-lookup"><span data-stu-id="5a844-109">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="5a844-110">Parte</span><span class="sxs-lookup"><span data-stu-id="5a844-110">Part</span></span>    | <span data-ttu-id="5a844-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a844-111">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="5a844-112">*value*</span><span class="sxs-lookup"><span data-stu-id="5a844-112">*value*</span></span> | <span data-ttu-id="5a844-113">Valore Long Integer che specifica l'altezza del frame del carattere.</span><span class="sxs-lookup"><span data-stu-id="5a844-113">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a844-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a844-114">Remarks</span></span>

<span data-ttu-id="5a844-115">La **proprietà Height** è sempre espressa in pixel, rispetto alle coordinate dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="5a844-115">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="5a844-116">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="5a844-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="5a844-117">Anche se il carattere viene visualizzato in una finestra di area di forma irregolare, l'altezza del carattere si basa sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5a844-117">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




