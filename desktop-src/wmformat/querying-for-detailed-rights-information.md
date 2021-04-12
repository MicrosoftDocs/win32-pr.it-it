---
title: Esecuzione di query per informazioni dettagliate sui diritti
description: Esecuzione di query per informazioni dettagliate sui diritti
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows Media Format SDK, esecuzione di query per i diritti dettagliati
- Windows Media Format SDK, query sui diritti dettagliati
- Digital Rights Management (DRM), esecuzione di query per i diritti dettagliati
- DRM (Digital Rights Management), esecuzione di query per i diritti dettagliati
- Digital Rights Management (DRM), query sui diritti dettagliati
- DRM (Digital Rights Management), query sui diritti dettagliati
- API estese del client DRM, esecuzione di query per i diritti dettagliati
- API estese del client, esecuzione di query per i diritti dettagliati
- API estese del client DRM, query sui diritti dettagliati
- API estese client, query con diritti dettagliati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221530"
---
# <a name="querying-for-detailed-rights-information"></a><span data-ttu-id="b5842-113">Esecuzione di query per informazioni dettagliate sui diritti</span><span class="sxs-lookup"><span data-stu-id="b5842-113">Querying for Detailed Rights Information</span></span>

<span data-ttu-id="b5842-114">Usando il metodo [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) , è possibile ottenere informazioni dettagliate sui diritti concessi dalle licenze per un ID chiave.</span><span class="sxs-lookup"><span data-stu-id="b5842-114">By using the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method, you can obtain detailed information about the rights granted by licenses for a key ID.</span></span> <span data-ttu-id="b5842-115">Le informazioni che si ottengono da questo metodo vengono aggregate da tutte le licenze nell'archivio licenze locale che si applicano all'ID chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="b5842-115">The information that you get from this method is aggregated from all licenses in the local license store that apply to the specified key ID.</span></span>

<span data-ttu-id="b5842-116">**QueryLicenseState** usa la [**struttura \_ \_ \_ dei dati di stato delle licenze DRM**](drmdrm-license-state-data.md) per visualizzare informazioni aggregate su tutte le licenze per l'ID chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="b5842-116">**QueryLicenseState** uses the [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure to display aggregate information about all the licenses for the specified key ID.</span></span> <span data-ttu-id="b5842-117">Questo utilizzo è diverso rispetto ad altri oggetti in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="b5842-117">This usage is different than by other objects in the Windows Media Format SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5842-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5842-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5842-119">**Recupero di informazioni dalle licenze nell'archivio licenze locale**</span><span class="sxs-lookup"><span data-stu-id="b5842-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




