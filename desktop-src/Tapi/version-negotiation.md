---
description: Nel tempo è possibile che esistano versioni diverse per le applicazioni TAPI, TAPI e i provider di servizi.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Negoziazione della versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968286"
---
# <a name="version-negotiation"></a><span data-ttu-id="26314-103">Negoziazione della versione</span><span class="sxs-lookup"><span data-stu-id="26314-103">Version Negotiation</span></span>

<span data-ttu-id="26314-104">Nel tempo è possibile che esistano versioni diverse per le applicazioni TAPI, TAPI e i provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="26314-104">Over time, different versions may exist for TAPI applications, TAPI, and the service providers.</span></span> <span data-ttu-id="26314-105">L'interoperabilità ottimale di un'applicazione TAPI richiede una conoscenza non solo della versione TAPI dell'applicazione, ma anche delle versioni del provider di servizi, TAPISVR e DLL di TAPI.</span><span class="sxs-lookup"><span data-stu-id="26314-105">Optimal interoperability of a TAPI application requires knowledge of not just the application's TAPI version, but also of the TAPI DLL, TAPISVR, and service provider versions.</span></span>

<span data-ttu-id="26314-106">La mancata corretta negoziazione della versione può causare gravi problemi.</span><span class="sxs-lookup"><span data-stu-id="26314-106">Failure to do proper version negotiation can result in serious problems.</span></span> <span data-ttu-id="26314-107">Alcune strutture utilizzate, ad esempio, hanno membri dati aggiunti da una versione a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="26314-107">For example, some heavily used structures have data members added from one version to the next.</span></span> <span data-ttu-id="26314-108">Se la dimensione della struttura non corrisponde a quella prevista dall'applicazione o da TAPI, le conseguenze variano a causa di perdite di memoria in AVs intermittenti.</span><span class="sxs-lookup"><span data-stu-id="26314-108">If the structure size does not match what the application or TAPI expects, the consequences range from memory leaks to intermittent AVs.</span></span>

<span data-ttu-id="26314-109">Per ulteriori informazioni, vedere [controllo delle versioni di TAPI](./tapi-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="26314-109">For additional information, see [TAPI Versioning](./tapi-versioning.md).</span></span>

<span data-ttu-id="26314-110">**TAPI 2. x:** Le applicazioni negoziano con TAPI e TAPISVR durante [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="26314-110">**TAPI 2.x:** Applications negotiate with TAPI and TAPISVR during [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span> <span data-ttu-id="26314-111">Le applicazioni eseguono la negoziazione del dispositivo con i provider di servizi chiamando [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) per ogni riga che l'applicazione potrebbe usare.</span><span class="sxs-lookup"><span data-stu-id="26314-111">Applications perform device negotiation with service providers by calling [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) for each line that the application might use.</span></span>

<span data-ttu-id="26314-112">**TAPI 3. x:** Non è necessario eseguire la negoziazione della versione. Tuttavia, è possibile utilizzare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per determinare se un'interfaccia è disponibile nella propria versione.</span><span class="sxs-lookup"><span data-stu-id="26314-112">**TAPI 3.x:** There is no need to perform version negotiation; however, you can use [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to determine if an interface is available on their version.</span></span>

 

 
