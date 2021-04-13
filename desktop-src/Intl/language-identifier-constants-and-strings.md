---
description: Ogni identificatore di lingua è costituito da un identificatore di lingua principale che indica la lingua e un identificatore di lingua secondaria che indica il paese/area geografica.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Costanti e stringhe degli identificatori di lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346041"
---
# <a name="language-identifier-constants-and-strings"></a><span data-ttu-id="bce3f-103">Costanti e stringhe degli identificatori di lingua</span><span class="sxs-lookup"><span data-stu-id="bce3f-103">Language Identifier Constants and Strings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bce3f-104">Le costanti identificatore della lingua sono deprecate e il loro utilizzo è sconsigliato.</span><span class="sxs-lookup"><span data-stu-id="bce3f-104">Language identifier constants are deprecated and their use is discouraged.</span></span> <span data-ttu-id="bce3f-105">L'uso di nomi delle impostazioni locali invece degli identificatori delle impostazioni locali è sempre preferibile.</span><span class="sxs-lookup"><span data-stu-id="bce3f-105">Use of locale names instead of locale identifiers is always preferable.</span></span>

<span data-ttu-id="bce3f-106">Per una descrizione degli identificatori di lingua, vedere [identificatore](language-identifiers.md) della lingua.</span><span class="sxs-lookup"><span data-stu-id="bce3f-106">See [language identifier](language-identifiers.md) for a description of language identifiers.</span></span>

<span data-ttu-id="bce3f-107">Un identificatore primario o sublingua può essere definito dall'utente o predefinito.</span><span class="sxs-lookup"><span data-stu-id="bce3f-107">A primary or sublanguage identifier can be user-defined or predefined.</span></span> <span data-ttu-id="bce3f-108">Per gli identificatori di lingua primaria predefiniti con i relativi identificatori di sottolingua validi, vedere [[MS-LCID]: informazioni di riferimento sull'identificatore del codice lingua (LCID) di Windows](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span><span class="sxs-lookup"><span data-stu-id="bce3f-108">For the predefined primary language identifiers with their valid sublanguage identifiers, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span></span>

> [!Note]  
> <span data-ttu-id="bce3f-109">Se non è disponibile alcun identificatore di lingua per l'uso con un identificatore di lingua principale, l'applicazione deve usare l' **\_ impostazione predefinita di SUBLANG**.</span><span class="sxs-lookup"><span data-stu-id="bce3f-109">If there is no sublanguage identifier to use with a primary language identifier, your application should use **SUBLANG\_DEFAULT**.</span></span> <span data-ttu-id="bce3f-110">Per le risorse identiche per tutte le sottolingue di una lingua primaria, è necessario usare la sottolingua **\_ neutra** .</span><span class="sxs-lookup"><span data-stu-id="bce3f-110">It should use **SUBLANG\_NEUTRAL** for resources that are the same for all sublanguages of a primary language.</span></span>

<span data-ttu-id="bce3f-111">Un identificatore della lingua primaria definito dall'utente ha un valore compreso nell'intervallo tra 0x0200 e 0x03ff.</span><span class="sxs-lookup"><span data-stu-id="bce3f-111">A user-defined primary language identifier has a value in the range 0x0200 to 0x03ff.</span></span> <span data-ttu-id="bce3f-112">Tutti gli altri valori sono riservati per l'utilizzo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bce3f-112">All other values are reserved for operating system use.</span></span>

<span data-ttu-id="bce3f-113">Un identificatore di lingua inglese definito dall'utente ha un valore compreso nell'intervallo tra 0x20 e 0x3F.</span><span class="sxs-lookup"><span data-stu-id="bce3f-113">A user-defined sublanguage identifier has a value in the range 0x20 to 0x3f.</span></span> <span data-ttu-id="bce3f-114">Tutti gli altri valori sono riservati per l'utilizzo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bce3f-114">All other values are reserved for operating system use.</span></span>
