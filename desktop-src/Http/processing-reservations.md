---
title: Elaborazione delle prenotazioni
description: Le prenotazioni per parti dello spazio dei nomi URL vengono effettuate dall'amministratore di sistema e inserite nell'archivio prenotazioni permanente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399898"
---
# <a name="processing-reservations"></a><span data-ttu-id="57e3b-103">Elaborazione delle prenotazioni</span><span class="sxs-lookup"><span data-stu-id="57e3b-103">Processing Reservations</span></span>

<span data-ttu-id="57e3b-104">Le prenotazioni per parti dello spazio dei nomi URL vengono effettuate dall'amministratore di sistema e inserite nell'archivio prenotazioni permanente.</span><span class="sxs-lookup"><span data-stu-id="57e3b-104">Reservations for portions of the URL namespace are made by the system administrator and placed in the persistent reservation store.</span></span> <span data-ttu-id="57e3b-105">La radice dello spazio dei nomi URL per HTTP è di proprietà dell'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="57e3b-105">The root of the URL namespace for HTTP is owned by the system administrator.</span></span> <span data-ttu-id="57e3b-106">Per tutti i valori host e porta, le due prenotazioni seguenti vengono sempre presupposte nella radice dello spazio dei nomi **relativeUri** .</span><span class="sxs-lookup"><span data-stu-id="57e3b-106">For all host and port values, the following two reservations are always assumed at the root of the **relativeUri** namespace.</span></span>



| <span data-ttu-id="57e3b-107">Spazio dei nomi riservato</span><span class="sxs-lookup"><span data-stu-id="57e3b-107">Namespace reserved</span></span>                 | <span data-ttu-id="57e3b-108">Riservato per</span><span class="sxs-lookup"><span data-stu-id="57e3b-108">Reserved for</span></span>              |
|------------------------------------|---------------------------|
| <span data-ttu-id="57e3b-109"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="57e3b-109">https://<host>:<port>/</span></span>  | <span data-ttu-id="57e3b-110">Amministratore LocalSystem</span><span class="sxs-lookup"><span data-stu-id="57e3b-110">LocalSystem Administrator</span></span> |
| <span data-ttu-id="57e3b-111"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="57e3b-111">https://<host>:<port>/</span></span> | <span data-ttu-id="57e3b-112">Amministratore LocalSystem</span><span class="sxs-lookup"><span data-stu-id="57e3b-112">LocalSystem Administrator</span></span> |



 

<span data-ttu-id="57e3b-113">Non è possibile rimuovere queste prenotazioni implicite.</span><span class="sxs-lookup"><span data-stu-id="57e3b-113">These implicit reservations cannot be removed.</span></span> <span data-ttu-id="57e3b-114">Tuttavia, è possibile delegare le prenotazioni radice esplicite ad altri utenti.</span><span class="sxs-lookup"><span data-stu-id="57e3b-114">However, it is possible to delegate explicit root reservations to other users.</span></span> <span data-ttu-id="57e3b-115">Le prenotazioni come quelle riportate di seguito creeranno tali deleghe:</span><span class="sxs-lookup"><span data-stu-id="57e3b-115">Reservations such as the following would create such delegations:</span></span>



| <span data-ttu-id="57e3b-116">Spazio dei nomi riservato</span><span class="sxs-lookup"><span data-stu-id="57e3b-116">Namespace reserved</span></span>        | <span data-ttu-id="57e3b-117">Riservato per</span><span class="sxs-lookup"><span data-stu-id="57e3b-117">Reserved for</span></span> |
|---------------------------|--------------|
| `https://+:80/`           | <span data-ttu-id="57e3b-118">UtenteA, l'utente c</span><span class="sxs-lookup"><span data-stu-id="57e3b-118">UserA, UserC</span></span> |
| `https://adatum.com:443/` | <span data-ttu-id="57e3b-119">UtenteB</span><span class="sxs-lookup"><span data-stu-id="57e3b-119">UserB</span></span>        |



 

<span data-ttu-id="57e3b-120">Se queste prenotazioni delegate vengono rimosse dall'amministratore di sistema, la proprietà dello spazio dei nomi ripristina la prenotazione implicita per i valori host e porta corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="57e3b-120">If these delegated reservations are removed by the system administrator, ownership of the namespace reverts to the implicit reservation for the corresponding host and port values.</span></span>

 

 




