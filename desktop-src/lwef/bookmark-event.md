---
title: Evento segnalibro
description: Evento segnalibro
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221268"
---
# <a name="bookmark-event"></a><span data-ttu-id="60994-103">Evento segnalibro</span><span class="sxs-lookup"><span data-stu-id="60994-103">Bookmark Event</span></span>

<span data-ttu-id="60994-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60994-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="60994-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="60994-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="60994-106">Si verifica quando viene attivato un segnalibro in una stringa di testo vocale definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60994-106">Occurs when a bookmark in a speech text string that your application defined is activated.</span></span>

</dd> <dt>

<span data-ttu-id="60994-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="60994-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="60994-108">  \_ **Segnalibro** Sub Agent **(ByVal** *BookmarkI\D \* * *)**</span><span class="sxs-lookup"><span data-stu-id="60994-108">**Sub** *agent*\_**Bookmark** **(ByVal** *BookmarkID\*\*\*)*\*</span></span>



| <span data-ttu-id="60994-109">Parte</span><span class="sxs-lookup"><span data-stu-id="60994-109">Part</span></span>         | <span data-ttu-id="60994-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60994-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="60994-111">*BookmarkID*</span><span class="sxs-lookup"><span data-stu-id="60994-111">*BookmarkID*</span></span> | <span data-ttu-id="60994-112">Valore long integer che identifica il numero di segnalibri.</span><span class="sxs-lookup"><span data-stu-id="60994-112">A Long integer identifying the bookmark number.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="60994-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="60994-113">Remarks</span></span>

<span data-ttu-id="60994-114">Per specificare un evento di segnalibro, usare il metodo [**Speak**](speak-method.md) con un tag **MRK** nel testo fornito.</span><span class="sxs-lookup"><span data-stu-id="60994-114">To specify a bookmark event, use the [**Speak**](speak-method.md) method with a **Mrk** tag in your supplied text.</span></span> <span data-ttu-id="60994-115">Per altre informazioni sui tag, vedere Tag di output vocale.</span><span class="sxs-lookup"><span data-stu-id="60994-115">For more information about tags, see Speech Output Tags.</span></span>

 

 




