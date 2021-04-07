---
title: Esecuzione di query per gli utenti
description: Per eseguire una query per un utente, la query deve contenere l'espressione di ricerca \ 0034;( (utente objectClass) (objectCategory person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- utenti AD, esecuzione di query per gli utenti
- Active Directory, utilizzo di, utenti, esecuzione di query per gli utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724458"
---
# <a name="querying-for-users"></a><span data-ttu-id="75544-105">Esecuzione di query per gli utenti</span><span class="sxs-lookup"><span data-stu-id="75544-105">Querying for Users</span></span>

<span data-ttu-id="75544-106">Per eseguire una query per un utente, la query deve contenere l'espressione di ricerca "(& (objectClass = user) (objectCategory = person))".</span><span class="sxs-lookup"><span data-stu-id="75544-106">To query for a user, the query must contain the search expression "(&(objectClass=user)(objectCategory=person))".</span></span>

<span data-ttu-id="75544-107">Poiché la classe computer è una sottoclasse di User, una query contenente solo (objectClass = user) restituirà oggetti utente e computer.</span><span class="sxs-lookup"><span data-stu-id="75544-107">Because the computer class is a subclass of user, a query containing only (objectClass=user) would return user objects and computer objects.</span></span> <span data-ttu-id="75544-108">Inoltre, la categoria dell'oggetto utente è persona (non utente); Pertanto, l'espressione (objectCategory = user) non restituisce alcun utente.</span><span class="sxs-lookup"><span data-stu-id="75544-108">Also, the object category of the user object is person (not user); therefore, the expression (objectCategory=user) does not return any users.</span></span> <span data-ttu-id="75544-109">Se si utilizza l'espressione (objectCategory = person), la query restituisce oggetti utente e oggetti contatto.</span><span class="sxs-lookup"><span data-stu-id="75544-109">If you use the expression (objectCategory=person), the query returns user objects and contact objects.</span></span>

<span data-ttu-id="75544-110">Gli utenti possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio.</span><span class="sxs-lookup"><span data-stu-id="75544-110">Users can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="75544-111">Questo significa che gli utenti possono trovarsi in numerose posizioni nella gerarchia di directory.</span><span class="sxs-lookup"><span data-stu-id="75544-111">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="75544-112">È possibile eseguire una ricerca completa di "(objectCategory = user)" per trovare tutti gli utenti in un contenitore, in un'unità organizzativa, in un dominio, in un albero di dominio o in una foresta, a seconda dell'oggetto a cui è associato il puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) in uso.</span><span class="sxs-lookup"><span data-stu-id="75544-112">You can perform a deep search for "(objectCategory=user)" to find all users in a container, organizational unit, domain, domain tree, or forest—depending on the object that the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer you are using is bound to.</span></span>

 

 