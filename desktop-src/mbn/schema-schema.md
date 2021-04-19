---
description: Definisce un profilo a banda larga mobile.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Riferimento allo schema del profilo broadband mobile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307529"
---
# <a name="mobile-broadband-profile-schema-reference"></a><span data-ttu-id="57e5e-103">Riferimento allo schema del profilo broadband mobile</span><span class="sxs-lookup"><span data-stu-id="57e5e-103">Mobile Broadband Profile Schema Reference</span></span>

<span data-ttu-id="57e5e-104">Lo schema del profilo Mobile Broadband definisce un profilo a banda larga mobile.</span><span class="sxs-lookup"><span data-stu-id="57e5e-104">The Mobile Broadband Profile Schema defines a Mobile Broadband Profile.</span></span>

<span data-ttu-id="57e5e-105">I profili archiviano i parametri di configurazione di rete e utente correlati a banda larga mobile.</span><span class="sxs-lookup"><span data-stu-id="57e5e-105">Profiles store Mobile Broadband connection related user and network configuration parameters.</span></span> <span data-ttu-id="57e5e-106">Vengono inoltre archiviate le preferenze dell'utente per una connessione.</span><span class="sxs-lookup"><span data-stu-id="57e5e-106">They also store the user preferences for a connection.</span></span>

<span data-ttu-id="57e5e-107">L'elemento radice di un profilo Mobile Broadband è l'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="57e5e-107">The root element of a Mobile Broadband profile is the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span> <span data-ttu-id="57e5e-108">Ogni profilo include esattamente un elemento radice.</span><span class="sxs-lookup"><span data-stu-id="57e5e-108">Each profile has exactly one root element.</span></span> <span data-ttu-id="57e5e-109">Tutti gli elementi dello schema del profilo broadband mobile utilizzati da Windows 7 si trovano nello spazio dei nomi `https://www.microsoft.com/networking/WWAN/profile/v1` e gli elementi utilizzati da Windows 8 si trovano nello spazio dei nomi `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="57e5e-109">All Mobile Broadband Profile Schema elements used by Windows 7 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1` and the elements used by Windows 8 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

<span data-ttu-id="57e5e-110">Lo schema del profilo Mobile Broadband impone rigorosamente l'ordine dei nodi.</span><span class="sxs-lookup"><span data-stu-id="57e5e-110">The Mobile Broadband Profile Schema strictly enforces the order of the nodes.</span></span> <span data-ttu-id="57e5e-111">I nodi specificati in un profilo devono essere conformi allo **schema del profilo broadband mobile** e vengono visualizzati nell'ordine previsto nella definizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="57e5e-111">Nodes specified in a profile must adhere to the **Mobile Broadband Profile Schema** and appear in the order prescribed in the schema definition.</span></span> <span data-ttu-id="57e5e-112">Ad esempio, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) deve essere specificato immediatamente dopo [**AccessString**](schema-accessstring-contexttype-element.md).</span><span class="sxs-lookup"><span data-stu-id="57e5e-112">For example, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) must be specified immediately after [**AccessString**](schema-accessstring-contexttype-element.md).</span></span>

-   [<span data-ttu-id="57e5e-113">Schema profilo broadband mobile V1</span><span class="sxs-lookup"><span data-stu-id="57e5e-113">Mobile Broadband Profile Schema v1</span></span>](mobile-broadband-profile-schema.md)
-   [<span data-ttu-id="57e5e-114">Schema del profilo broadband mobile V2</span><span class="sxs-lookup"><span data-stu-id="57e5e-114">Mobile Broadband Profile Schema v2</span></span>](mobile-broadband-profile-schema-v2.md)
-   [<span data-ttu-id="57e5e-115">Schema profilo a banda larga mobile V3</span><span class="sxs-lookup"><span data-stu-id="57e5e-115">Mobile Broadband Profile Schema v3</span></span>](mobile-broadband-profile-schema-v3.md)
-   <span data-ttu-id="57e5e-116">[Schema del profilo broadband mobile V4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="57e5e-116">[Mobile Broadband Profile Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span></span>

 

 
