---
title: Errori comuni (AD DS)
description: La tabella seguente contiene un elenco di errori comuni che possono verificarsi in base all'ambito del gruppo nidificato.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Errori comuni AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "104472179"
---
# <a name="common-errors-ad-ds"></a><span data-ttu-id="99620-104">Errori comuni (AD DS)</span><span class="sxs-lookup"><span data-stu-id="99620-104">Common Errors (AD DS)</span></span>

<span data-ttu-id="99620-105">La tabella seguente contiene un elenco di errori comuni che possono verificarsi in base all'ambito del gruppo nidificato.</span><span class="sxs-lookup"><span data-stu-id="99620-105">The following table contains a list of common errors that can occur based on the scope of the group being nested.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99620-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="99620-106">HRESULT</span></span></th>
<th><span data-ttu-id="99620-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99620-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99620-108">0x8007001F</span><span class="sxs-lookup"><span data-stu-id="99620-108">0x8007001F</span></span></td>
<td><span data-ttu-id="99620-109">Errore generale.</span><span class="sxs-lookup"><span data-stu-id="99620-109">General failure.</span></span> <span data-ttu-id="99620-110">Questo errore si verifica se si tenta di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="99620-110">This error occurs if you attempt to:</span></span>
<ul>
<li><span data-ttu-id="99620-111">Aggiungere un gruppo locale di dominio a un gruppo globale o universale o a un gruppo locale di dominio in un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="99620-111">Add a domain local group to a global or universal group or a domain local group in another domain.</span></span> <span data-ttu-id="99620-112">I gruppi locali di dominio possono essere aggiunti solo come membri ad altri gruppi locali di dominio nello stesso dominio.</span><span class="sxs-lookup"><span data-stu-id="99620-112">Domain local groups can only be added as members to other domain local groups in the same domain.</span></span></li>
<li><span data-ttu-id="99620-113">Aggiungere un gruppo universale a un gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="99620-113">Add a universal group to a global group.</span></span> <span data-ttu-id="99620-114">I gruppi universali possono essere aggiunti a gruppi locali universali e di dominio, ma non a gruppi globali.</span><span class="sxs-lookup"><span data-stu-id="99620-114">Universal groups can be added to universal and domain local groups, but not global groups.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99620-115">0x8007202F</span><span class="sxs-lookup"><span data-stu-id="99620-115">0x8007202F</span></span></td>
<td><span data-ttu-id="99620-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span><span class="sxs-lookup"><span data-stu-id="99620-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span></span> <span data-ttu-id="99620-117">Questo errore si verifica se si tenta di aggiungere un gruppo di sicurezza a un altro gruppo in un dominio in esecuzione in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="99620-117">This error occurs if you attempt to add a security group to another group in a domain running in mixed mode.</span></span> <span data-ttu-id="99620-118">Non è possibile nidificare i gruppi di sicurezza in modalità mista. i gruppi di sicurezza possono essere annidati solo in modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="99620-118">Security groups cannot be nested in mixed mode; security groups can only be nested in native mode.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




