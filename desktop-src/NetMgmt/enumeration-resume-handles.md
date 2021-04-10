---
title: Handle di ripresa dell'enumerazione
description: Gli handle di ripresa dell'enumerazione sono identificatori per la chiave di ripresa effettiva contenuta nei dati dell'istanza per la funzione. Questa operazione è necessaria per la sicurezza, l'interoperabilità e per semplificare il codice chiamante per la funzione.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955499"
---
# <a name="enumeration-resume-handles"></a><span data-ttu-id="ec2c9-104">Handle di ripresa dell'enumerazione</span><span class="sxs-lookup"><span data-stu-id="ec2c9-104">Enumeration Resume Handles</span></span>

<span data-ttu-id="ec2c9-105">Gli handle di ripresa dell'enumerazione sono identificatori per la chiave di ripresa effettiva contenuta nei dati dell'istanza per la funzione.</span><span class="sxs-lookup"><span data-stu-id="ec2c9-105">Enumeration resume handles are identifiers for the actual resume key contained in the instance data for the function.</span></span> <span data-ttu-id="ec2c9-106">Questa operazione è necessaria per la sicurezza, l'interoperabilità e per semplificare il codice chiamante per la funzione.</span><span class="sxs-lookup"><span data-stu-id="ec2c9-106">This is required for security, interoperability, and to simplify the caller code for the function.</span></span>

<span data-ttu-id="ec2c9-107">Se viene passato un **valore null** per il puntatore al punto di ripristino, non viene archiviato alcun handle e non è possibile continuare la ricerca dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ec2c9-107">If a **NULL** is passed for the pointer to the resume handle, no handle is stored and the enumeration search cannot be continued.</span></span> <span data-ttu-id="ec2c9-108">Questa operazione è utile nei casi in cui l'applicazione non desidera enumerare tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="ec2c9-108">This is useful in cases where the application does not want to enumerate all the items.</span></span>

<span data-ttu-id="ec2c9-109">Se viene restituito un errore da una chiamata di enumerazione, l'handle di ripresa deve essere considerato non valido e non usato per le successive chiamate di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ec2c9-109">If an error is returned from an enumeration call, the resume handle must be treated as invalid and not used for any subsequent enumeration calls.</span></span> <span data-ttu-id="ec2c9-110">Quando si verifica questa situazione, è necessario riavviare l'enumerazione dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="ec2c9-110">When this occurs you must restart the enumeration from the beginning.</span></span>

 

 




