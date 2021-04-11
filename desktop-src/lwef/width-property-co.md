---
title: Proprietà Width (oggetto characters)
description: Width (proprietà)
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047714"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="48efe-103">Proprietà Width (oggetto characters)</span><span class="sxs-lookup"><span data-stu-id="48efe-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="48efe-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="48efe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="48efe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="48efe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="48efe-106">Restituisce o imposta la larghezza del frame per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="48efe-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="48efe-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="48efe-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="48efe-108">\*agente \***. Caratteri ("**_CharacterID_\*_")._ \*  \[ =  *Valore* larghezza\]</span><span class="sxs-lookup"><span data-stu-id="48efe-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="48efe-109">Parte</span><span class="sxs-lookup"><span data-stu-id="48efe-109">Part</span></span>    | <span data-ttu-id="48efe-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48efe-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="48efe-111">*value*</span><span class="sxs-lookup"><span data-stu-id="48efe-111">*value*</span></span> | <span data-ttu-id="48efe-112">Valore long integer che specifica la larghezza del frame del carattere.</span><span class="sxs-lookup"><span data-stu-id="48efe-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48efe-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="48efe-113">Remarks</span></span>

<span data-ttu-id="48efe-114">La proprietà [**Width**](width-property.md) è sempre espressa in pixel.</span><span class="sxs-lookup"><span data-stu-id="48efe-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="48efe-115">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="48efe-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="48efe-116">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="48efe-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




