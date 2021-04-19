---
description: Le funzioni seguenti vengono utilizzate con la rete DDE.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funzioni DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319618"
---
# <a name="network-dde-functions"></a><span data-ttu-id="9dd7d-103">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="9dd7d-103">Network DDE Functions</span></span>

<span data-ttu-id="9dd7d-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="9dd7d-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="9dd7d-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="9dd7d-106">Le funzioni seguenti vengono utilizzate con la rete DDE.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-106">The following functions are used with network DDE.</span></span>



| <span data-ttu-id="9dd7d-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="9dd7d-107">Function</span></span>                                                   | <span data-ttu-id="9dd7d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dd7d-108">Description</span></span>                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dd7d-109">**NDdeGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-109">**NDdeGetErrorString**</span></span>](nddegeterrorstring.md)           | <span data-ttu-id="9dd7d-110">Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che descrive il codice di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-110">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span> |
| [<span data-ttu-id="9dd7d-111">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-111">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)       | <span data-ttu-id="9dd7d-112">Recupera il descrittore di sicurezza associato alla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-112">Retrieves the security descriptor associated with the DDE share.</span></span>                                                      |
| [<span data-ttu-id="9dd7d-113">**NDdeGetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-113">**NDdeGetTrustedShare**</span></span>](nddegettrustedshare.md)         | <span data-ttu-id="9dd7d-114">Recupera le opzioni associate a una condivisione DDE presente nell'elenco di condivisioni attendibili dell'utente del server.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-114">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>                |
| [<span data-ttu-id="9dd7d-115">**NDdeIsValidAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-115">**NDdeIsValidAppTopicList**</span></span>](nddeisvalidapptopiclist.md) | <span data-ttu-id="9dd7d-116">Determina se un'applicazione e una stringa di argomento ("*appname* \| *topicName*") utilizzano la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-116">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>                 |
| [<span data-ttu-id="9dd7d-117">**NDdeIsValidShareName**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-117">**NDdeIsValidShareName**</span></span>](nddeisvalidsharename.md)       | <span data-ttu-id="9dd7d-118">Determina se un nome di condivisione utilizza la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-118">Determines whether a share name uses the proper syntax.</span></span>                                                               |
| [<span data-ttu-id="9dd7d-119">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-119">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)       | <span data-ttu-id="9dd7d-120">Imposta il descrittore di sicurezza associato alla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-120">Sets the security descriptor associated with the DDE share.</span></span>                                                           |
| [<span data-ttu-id="9dd7d-121">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-121">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)         | <span data-ttu-id="9dd7d-122">Concede lo stato attendibile della condivisione DDE specificato all'interno del contesto dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-122">Grants the specified DDE share trusted status within the current user's context.</span></span>                                      |
| [<span data-ttu-id="9dd7d-123">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-123">**NDdeShareAdd**</span></span>](nddeshareadd.md)                       | <span data-ttu-id="9dd7d-124">Crea e aggiunge una nuova condivisione DDE alla gestione del database di condivisione DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="9dd7d-124">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>                                            |
| [<span data-ttu-id="9dd7d-125">**NDdeShareDel**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-125">**NDdeShareDel**</span></span>](nddesharedel.md)                       | <span data-ttu-id="9dd7d-126">Elimina una condivisione DDE dal DSDM.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-126">Deletes a DDE share from the DSDM.</span></span>                                                                                    |
| [<span data-ttu-id="9dd7d-127">**NDdeShareEnum**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-127">**NDdeShareEnum**</span></span>](nddeshareenum.md)                     | <span data-ttu-id="9dd7d-128">Recupera l'elenco delle condivisioni DDE disponibili.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-128">Retrieves the list of available DDE shares.</span></span>                                                                           |
| [<span data-ttu-id="9dd7d-129">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-129">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)               | <span data-ttu-id="9dd7d-130">Recupera le informazioni sulla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-130">Retrieves DDE share information.</span></span>                                                                                      |
| [<span data-ttu-id="9dd7d-131">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-131">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)               | <span data-ttu-id="9dd7d-132">Imposta le informazioni sulla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-132">Sets DDE share information.</span></span>                                                                                           |
| [<span data-ttu-id="9dd7d-133">**NDdeTrustedShareEnum**</span><span class="sxs-lookup"><span data-stu-id="9dd7d-133">**NDdeTrustedShareEnum**</span></span>](nddetrustedshareenum.md)       | <span data-ttu-id="9dd7d-134">Recupera i nomi di tutte le condivisioni DDE di rete considerate attendibili nel contesto del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="9dd7d-134">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>                 |



 

 

 



