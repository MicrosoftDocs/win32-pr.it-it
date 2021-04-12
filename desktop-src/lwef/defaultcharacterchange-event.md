---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396371"
---
# <a name="defaultcharacterchange-event"></a><span data-ttu-id="ce2c6-103">Evento DefaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="ce2c6-103">DefaultCharacterChange Event</span></span>

<span data-ttu-id="ce2c6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ce2c6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ce2c6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ce2c6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ce2c6-106">Si verifica quando l'utente modifica il carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="ce2c6-106">Occurs when the user changes the default character.</span></span>

</dd> <dt>

<span data-ttu-id="ce2c6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ce2c6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ce2c6-108">**Sub** *Agent. \* \* \* DefaultCharacterChange* \*  **(ByVal** *GUID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="ce2c6-108">**Sub** *agent.\*\*\*DefaultCharacterChange*\* **(ByVal** *GUID\*\*\*)*\*</span></span>



| <span data-ttu-id="ce2c6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ce2c6-109">Part</span></span>   | <span data-ttu-id="ce2c6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce2c6-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="ce2c6-111">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ce2c6-111">*GUID*</span></span> | <span data-ttu-id="ce2c6-112">Restituisce l'identificatore univoco per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ce2c6-112">Returns the unique identifier for the character.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="ce2c6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce2c6-113">Remarks</span></span>

<span data-ttu-id="ce2c6-114">Questo evento indica quando l'utente ha modificato il carattere assegnato come carattere predefinito dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ce2c6-114">This event indicates when the user has changed the character assigned as the user's default character.</span></span> <span data-ttu-id="ce2c6-115">Il server invia questo solo ai client che hanno caricato il carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="ce2c6-115">The server sends this only to clients that have loaded the default character.</span></span>

<span data-ttu-id="ce2c6-116">Quando viene visualizzato il nuovo carattere, assume le stesse dimensioni di qualsiasi istanza già caricata del carattere o del carattere predefinito precedente (in quell'ordine).</span><span class="sxs-lookup"><span data-stu-id="ce2c6-116">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

### <a name="see-also"></a><span data-ttu-id="ce2c6-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ce2c6-117">See Also</span></span>

<span data-ttu-id="ce2c6-118">[**Metodo ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **metodo Load**](load-method.md)</span><span class="sxs-lookup"><span data-stu-id="ce2c6-118">[**ShowDefaultCharacterProperties method**](showdefaultcharacterproperties-method.md), [**Load method**](load-method.md)</span></span>


 

 




