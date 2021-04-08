---
description: Il provider di base originale ha erroneamente segnalato che l'algoritmo hash SHA enumerava gli algoritmi mediante chiamate a CryptGetProvParam con il parametro PP \_ ENUMALGS specificato.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Funzionalità SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749559"
---
# <a name="sha-functionality"></a><span data-ttu-id="8cb1c-103">Funzionalità SHA</span><span class="sxs-lookup"><span data-stu-id="8cb1c-103">SHA Functionality</span></span>

<span data-ttu-id="8cb1c-104">Il provider di base originale ha erroneamente segnalato che l'algoritmo hash [*Sha*](../secgloss/s-gly.md) enumerava gli algoritmi mediante chiamate a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con il parametro PP \_ ENUMALGS specificato.</span><span class="sxs-lookup"><span data-stu-id="8cb1c-104">The original Base Provider incorrectly reported that the [*SHA*](../secgloss/s-gly.md) hash algorithm enumerating algorithms by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with parameter PP\_ENUMALGS specified.</span></span> <span data-ttu-id="8cb1c-105">Questo problema è stato risolto nel provider di base.</span><span class="sxs-lookup"><span data-stu-id="8cb1c-105">This has been fixed in the Base Provider.</span></span> <span data-ttu-id="8cb1c-106">Sia il provider di base modificato che il provider esteso e ora segnalano correttamente SHA-1.</span><span class="sxs-lookup"><span data-stu-id="8cb1c-106">Both the revised Base Provider and the Extended Provider and now correctly report SHA-1.</span></span>

<span data-ttu-id="8cb1c-107">Una costante CALG \_ SHA1 definita è stata aggiunta a Wincrypt. h con lo stesso valore di CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="8cb1c-107">A defined CALG\_SHA1 constant has been added to Wincrypt.h with the same value as CALG\_SHA.</span></span>

 

 
