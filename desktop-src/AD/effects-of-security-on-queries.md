---
title: Effetti della sicurezza sulla ricerca
description: La sicurezza è un filtro implicito durante l'esecuzione di ricerche, l'enumerazione di contenitori o la lettura di proprietà.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- effetti della sicurezza sulla ricerca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707699"
---
# <a name="effects-of-security-on-searching"></a><span data-ttu-id="4cb6f-104">Effetti della sicurezza sulla ricerca</span><span class="sxs-lookup"><span data-stu-id="4cb6f-104">Effects of Security on Searching</span></span>

<span data-ttu-id="4cb6f-105">La sicurezza è un filtro implicito durante l'esecuzione di ricerche, l'enumerazione di contenitori o la lettura di proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-105">Security is an implicit filter when performing searches, enumerating containers, or reading properties.</span></span>

<span data-ttu-id="4cb6f-106">ADSI non può restituire \_ tali \_ proprietà o \_ \_ errori di questo tipo anche quando l'oggetto esiste se non si dispone dell'accesso per leggere gli attributi sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-106">ADSI can return NO\_SUCH\_PROPERTY or NO\_SUCH\_OBJECT errors even when the object exists if you do not have access to read attributes on the object.</span></span>

<span data-ttu-id="4cb6f-107">Un chiamante, ad esempio, può essere in grado di enumerare gli oggetti figlio in un contenitore perché il chiamante dispone \_ dei diritti di contenuto dell'elenco nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-107">For example, a caller may be able to enumerate the child objects in a container because the caller has LIST\_CONTENTS rights on the container.</span></span> <span data-ttu-id="4cb6f-108">Tuttavia, lo stesso chiamante potrebbe non essere in grado di accedere agli oggetti enumerati se il chiamante non dispone dell'accesso in lettura agli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-108">But the same caller may not be able to access the enumerated objects if the caller does not have read access to the child objects.</span></span> <span data-ttu-id="4cb6f-109">In questo caso, una query per un oggetto figlio può restituire un oggetto di questo \_ tipo \_ anche se il chiamante ha enumerato correttamente l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-109">In this case, a query for a child object may return NO\_SUCH\_OBJECT even though the caller successfully enumerated the object.</span></span>

<span data-ttu-id="4cb6f-110">Se il chiamante non dispone di diritti sufficienti, è possibile che vengano restituiti i seguenti codici restituiti:</span><span class="sxs-lookup"><span data-stu-id="4cb6f-110">If the caller does not have sufficient rights, the following return codes may be returned:</span></span>

<span data-ttu-id="4cb6f-111">E \_ Ads \_ dominio non valido \_ \_</span><span class="sxs-lookup"><span data-stu-id="4cb6f-111">E\_ADS\_INVALID\_DOMAIN\_OBJECT</span></span>

<span data-ttu-id="4cb6f-112">\_Proprietà Ads \_ E \_ non \_ supportata</span><span class="sxs-lookup"><span data-stu-id="4cb6f-112">E\_ADS\_PROPERTY\_NOT\_SUPPORTED</span></span>

<span data-ttu-id="4cb6f-113">\_Proprietà Ads \_ E \_ non \_ trovata</span><span class="sxs-lookup"><span data-stu-id="4cb6f-113">E\_ADS\_PROPERTY\_NOT\_FOUND</span></span>

 

 




