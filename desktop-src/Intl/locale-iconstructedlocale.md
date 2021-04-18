---
description: Descrizione della \_ costante ICONSTRUCTEDLOCALE delle impostazioni locali
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/30/2021
ms.locfileid: "106334293"
---
# <a name="locale_iconstructedlocale"></a><span data-ttu-id="1eadb-103">impostazioni locali \_ ICONSTRUCTEDLOCALE</span><span class="sxs-lookup"><span data-stu-id="1eadb-103">LOCALE\_ICONSTRUCTEDLOCALE</span></span>

<span data-ttu-id="1eadb-104">Identificatore da richiedere se le impostazioni locali sono "costruite".</span><span class="sxs-lookup"><span data-stu-id="1eadb-104">Identifier to request if the locale is a "constructed" locale.</span></span> <span data-ttu-id="1eadb-105">L'uso di questo LCTYPE è sconsigliato.</span><span class="sxs-lookup"><span data-stu-id="1eadb-105">Use of this LCTYPE is discouraged.</span></span>

<span data-ttu-id="1eadb-106">Identifica le impostazioni locali per le quali Windows non dispone di informazioni complete e deve "costruire" informazioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1eadb-106">This identifies a locale for which Windows many not have complete information and has to "construct" information at runtime.</span></span> <span data-ttu-id="1eadb-107">In genere le informazioni fornite da LOCALE_ICONSTRUCTEDLOCALE sono di uso limitato poiché Windows fornirà la quantità di dati disponibile per ogni impostazione locale.</span><span class="sxs-lookup"><span data-stu-id="1eadb-107">Typically the information provided by LOCALE_ICONSTRUCTEDLOCALE is of limited use as Windows will provide as much data as is available for every locale.</span></span> <span data-ttu-id="1eadb-108">Pertanto, l'utilizzo di questo LCTYPE è sconsigliato.</span><span class="sxs-lookup"><span data-stu-id="1eadb-108">Therefore, use of this LCTYPE is discouraged.</span></span>


| <span data-ttu-id="1eadb-109">Valore</span><span class="sxs-lookup"><span data-stu-id="1eadb-109">Value</span></span> | <span data-ttu-id="1eadb-110">Significato</span><span class="sxs-lookup"><span data-stu-id="1eadb-110">Meaning</span></span>                 |
|-------|-------------------------|
| <span data-ttu-id="1eadb-111">0</span><span class="sxs-lookup"><span data-stu-id="1eadb-111">0</span></span>     | <span data-ttu-id="1eadb-112">Non costruito</span><span class="sxs-lookup"><span data-stu-id="1eadb-112">Not constructed</span></span>         |
| <span data-ttu-id="1eadb-113">1</span><span class="sxs-lookup"><span data-stu-id="1eadb-113">1</span></span>     | <span data-ttu-id="1eadb-114">È un'impostazione locale costruita</span><span class="sxs-lookup"><span data-stu-id="1eadb-114">Is a constructed locale</span></span> |


<span data-ttu-id="1eadb-115">Un esempio potrebbe essere una richiesta di "de-US" o del tedesco nel Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="1eadb-115">An example would be a request for "de-US", or German in the United States.</span></span> <span data-ttu-id="1eadb-116">NLS utilizzerà i dati in lingua tedesca che è possibile trovare e i dati Stati Uniti area che è possibile trovare.</span><span class="sxs-lookup"><span data-stu-id="1eadb-116">NLS will use the German language data that it can find and the United States region data that it can find.</span></span> 

<span data-ttu-id="1eadb-117">Questo potrebbe non essere perfetto come, ad esempio, il sistema non avrà probabilmente informazioni sul nome di Stati Uniti in tedesco.</span><span class="sxs-lookup"><span data-stu-id="1eadb-117">This may not be perfect as, for example, the system will likely not have information about the name of United States in German.</span></span> <span data-ttu-id="1eadb-118">Tuttavia, se l'applicazione o l'utente desidera un contesto "de-US", i dati restituiti sono i migliori disponibili.</span><span class="sxs-lookup"><span data-stu-id="1eadb-118">However, if the application or user desires a "de-US" context, then the returned data is the best available.</span></span> 

<span data-ttu-id="1eadb-119">In questo esempio le app che usano LOCALE_ICONSTRUCTEDLOCALE per rifiutare le impostazioni locali e per eseguire il fallback a impostazioni locali diverse si concludono in modo peggiore, ad esempio per l'atterraggio in de-DE o en-US.</span><span class="sxs-lookup"><span data-stu-id="1eadb-119">Apps that use LOCALE_ICONSTRUCTEDLOCALE to reject locales and fall back to a different locale typically end up with a worse experience, such as landing on de-DE or en-US in this example.</span></span> <span data-ttu-id="1eadb-120">Nessuno di questi si avvicina alla richiesta originale per la lingua tedesca con un'area Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="1eadb-120">Neither of those are close to the original request for German language with a United States region.</span></span>

