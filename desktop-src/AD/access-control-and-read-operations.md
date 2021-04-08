---
title: Controllo di accesso e operazioni di lettura
description: La sicurezza è un filtro implicito per la ricerca, l'enumerazione di contenitori o la lettura di proprietà.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Controllo di accesso e operazioni di lettura AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044017"
---
# <a name="access-control-and-read-operations"></a><span data-ttu-id="3b64b-104">Controllo di accesso e operazioni di lettura</span><span class="sxs-lookup"><span data-stu-id="3b64b-104">Access Control and Read Operations</span></span>

<span data-ttu-id="3b64b-105">La sicurezza è un filtro implicito per la ricerca, l'enumerazione di contenitori o la lettura di proprietà.</span><span class="sxs-lookup"><span data-stu-id="3b64b-105">Security is an implicit filter for searching, enumerating containers, or reading properties.</span></span> <span data-ttu-id="3b64b-106">Se non si dispone dei diritti di accesso necessari, i tentativi di elencare gli oggetti o le proprietà di lettura possono avere esito negativo con i codici di errore seguenti, anche se l'oggetto o la proprietà esiste:</span><span class="sxs-lookup"><span data-stu-id="3b64b-106">If you do not have the necessary access rights, attempts to list objects or read properties can fail with the following error codes even thought the object or property exists:</span></span>

-   <span data-ttu-id="3b64b-107">**E \_ Ads \_ dominio non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3b64b-107">**E\_ADS\_INVALID\_DOMAIN\_OBJECT**</span></span>
-   <span data-ttu-id="3b64b-108">**\_Proprietà Ads \_ E \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="3b64b-108">**E\_ADS\_PROPERTY\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="3b64b-109">**\_Proprietà Ads \_ E \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="3b64b-109">**E\_ADS\_PROPERTY\_NOT\_FOUND**</span></span>

<span data-ttu-id="3b64b-110">Tenere presente che un chiamante con **Ads \_ Rights \_ ACTRL \_ DS \_ List** Access to a container può enumerare gli oggetti figlio nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="3b64b-110">Be aware that a caller with **ADS\_RIGHT\_ACTRL\_DS\_LIST** access to a container can enumerate the child objects in the container.</span></span> <span data-ttu-id="3b64b-111">Tuttavia, un tentativo di accedere a un oggetto figlio può comunque avere esito negativo con un errore, ad esempio **E \_ Ads \_ Unknown \_ Object** se il chiamante non dispone di **Ads \_ right \_ ACTRL \_ \_ elenco DS \_** accesso all'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="3b64b-111">But an attempt to access a child object can still fail with an error such as **E\_ADS\_UNKNOWN\_OBJECT** if the caller does not have **ADS\_RIGHT\_ACTRL\_DS\_LIST\_OBJECT** access to the child object.</span></span>

<span data-ttu-id="3b64b-112">L'effetto della sicurezza sulle operazioni di lettura non è necessariamente manifesto come un errore.</span><span class="sxs-lookup"><span data-stu-id="3b64b-112">The impact of security on read operations is not necessarily manifested as an error.</span></span> <span data-ttu-id="3b64b-113">Ad esempio, un'operazione di ricerca può avere esito positivo, ma i risultati della ricerca non includono oggetti o proprietà a cui il chiamante non ha accesso.</span><span class="sxs-lookup"><span data-stu-id="3b64b-113">For example, a search operation can succeed, but the search results do not include objects or properties to which the caller does not have access.</span></span>

 

 




