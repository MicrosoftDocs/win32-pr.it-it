---
title: Proprietà HasOtherClients
description: Proprietà HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044744"
---
# <a name="hasotherclients-property"></a><span data-ttu-id="9092c-103">Proprietà HasOtherClients</span><span class="sxs-lookup"><span data-stu-id="9092c-103">HasOtherClients Property</span></span>

<span data-ttu-id="9092c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9092c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9092c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9092c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9092c-106">Restituisce un valore che indica se il carattere specificato è utilizzato da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9092c-106">Returns whether the specified character is in use by other applications.</span></span>

</dd> <dt>

<span data-ttu-id="9092c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="9092c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9092c-108">*agente*. **Caratteri ("***CharacterID***"). HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="9092c-108">*agent*.**Characters("***CharacterID***").HasOtherClients**</span></span>



| <span data-ttu-id="9092c-109">Valore</span><span class="sxs-lookup"><span data-stu-id="9092c-109">Value</span></span>     | <span data-ttu-id="9092c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9092c-110">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="9092c-111">**True**</span><span class="sxs-lookup"><span data-stu-id="9092c-111">**True**</span></span>  | <span data-ttu-id="9092c-112">Il carattere dispone di altri client.</span><span class="sxs-lookup"><span data-stu-id="9092c-112">The character has other clients.</span></span>           |
| <span data-ttu-id="9092c-113">**False**</span><span class="sxs-lookup"><span data-stu-id="9092c-113">**False**</span></span> | <span data-ttu-id="9092c-114">Il carattere non dispone di altri client.</span><span class="sxs-lookup"><span data-stu-id="9092c-114">The character does not have other clients.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9092c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9092c-115">Remarks</span></span>

<span data-ttu-id="9092c-116">È possibile usare questa proprietà per determinare se l'applicazione è l'unico o l'ultimo client del carattere, quando più di un'applicazione condivide (ha caricato) lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="9092c-116">You can use this property to determine whether your application is the only or last client of the character, when more than one application is sharing (has loaded) the same character.</span></span>

 

 




