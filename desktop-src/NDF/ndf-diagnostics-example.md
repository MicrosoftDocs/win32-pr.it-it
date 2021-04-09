---
title: Esempio di diagnostica NDF
description: Nell'esempio seguente viene illustrato come avviare l'interfaccia utente di NDF e diagnosticare la connettività al sito Web http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044574"
---
# <a name="ndf-diagnostics-example"></a><span data-ttu-id="77ede-103">Esempio di diagnostica NDF</span><span class="sxs-lookup"><span data-stu-id="77ede-103">NDF Diagnostics Example</span></span>

<span data-ttu-id="77ede-104">Nell'esempio seguente viene illustrato come avviare l'interfaccia utente di NDF e diagnosticare la connettività al sito Web https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="77ede-104">The following example shows how to launch the NDF user interface and diagnose connectivity to the website https://www.microsoft.com.</span></span>


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



<span data-ttu-id="77ede-105">L'interfaccia utente di NDF può essere avviata come finestra modale.</span><span class="sxs-lookup"><span data-stu-id="77ede-105">The NDF UI can be launched as a modal window.</span></span> <span data-ttu-id="77ede-106">A tale scopo, modificare il secondo parametro di [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) da **null** all'handle (HWND) della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="77ede-106">To do so, change the second parameter of [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) from **NULL** to the handle (HWND) of the parent window.</span></span>

<span data-ttu-id="77ede-107">Questo esempio può essere modificato per diagnosticare altre aree di rete.</span><span class="sxs-lookup"><span data-stu-id="77ede-107">This example can be modified to diagnose other areas of networking.</span></span> <span data-ttu-id="77ede-108">A tale scopo, sostituire la chiamata [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) con una delle altre funzioni di creazione degli eventi imprevisti, ad esempio [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) o [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span><span class="sxs-lookup"><span data-stu-id="77ede-108">To do so, replace the [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) call with one of the other incident creation functions, such as [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) or [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77ede-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77ede-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ede-110">**NdfCloseIncident**</span><span class="sxs-lookup"><span data-stu-id="77ede-110">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[<span data-ttu-id="77ede-111">**NdfCreateWebIncident**</span><span class="sxs-lookup"><span data-stu-id="77ede-111">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[<span data-ttu-id="77ede-112">**NdfExecuteDiagnosis**</span><span class="sxs-lookup"><span data-stu-id="77ede-112">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




