---
description: L'azione RegisterUser registra le informazioni utente con il programma di installazione per identificare l'utente di un prodotto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Azione RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756464"
---
# <a name="registeruser-action"></a><span data-ttu-id="518dd-103">Azione RegisterUser</span><span class="sxs-lookup"><span data-stu-id="518dd-103">RegisterUser Action</span></span>

<span data-ttu-id="518dd-104">L'azione RegisterUser registra le informazioni utente con il programma di installazione per identificare l'utente di un prodotto.</span><span class="sxs-lookup"><span data-stu-id="518dd-104">The RegisterUser action registers the user information with the installer to identify the user of a product.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="518dd-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="518dd-105">Sequence Restrictions</span></span>

<span data-ttu-id="518dd-106">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="518dd-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="518dd-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="518dd-107">ActionData Messages</span></span>



| <span data-ttu-id="518dd-108">Campo</span><span class="sxs-lookup"><span data-stu-id="518dd-108">Field</span></span> | <span data-ttu-id="518dd-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="518dd-109">Description of action data</span></span>   |
|-------|------------------------------|
| <span data-ttu-id="518dd-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="518dd-110">\[1\]</span></span> | <span data-ttu-id="518dd-111">Informazioni utente registrate.</span><span class="sxs-lookup"><span data-stu-id="518dd-111">Registered user information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="518dd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="518dd-112">Remarks</span></span>

<span data-ttu-id="518dd-113">L'azione RegisterUser non viene eseguita durante un'installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="518dd-113">The RegisterUser action is not performed during an administrative installation.</span></span> <span data-ttu-id="518dd-114">Se l'identificatore del prodotto immesso dall'utente non è stato convalidato dall' [azione ValidateProductID](validateproductid-action.md), la proprietà [**ProductID**](productid.md) non è impostata e questa azione non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="518dd-114">If the product identifier entered by the user has not been validated by the [ValidateProductID action](validateproductid-action.md), the [**ProductID**](productid.md) property is not set and this action does nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="518dd-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="518dd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="518dd-116">**NOME utente**</span><span class="sxs-lookup"><span data-stu-id="518dd-116">**USERNAME**</span></span>](username.md)
</dt> <dt>

[<span data-ttu-id="518dd-117">**COMPANYNAME**</span><span class="sxs-lookup"><span data-stu-id="518dd-117">**COMPANYNAME**</span></span>](companyname.md)
</dt> <dt>

[<span data-ttu-id="518dd-118">**ProductID**</span><span class="sxs-lookup"><span data-stu-id="518dd-118">**ProductID**</span></span>](productid.md)
</dt> </dl>

 

 



