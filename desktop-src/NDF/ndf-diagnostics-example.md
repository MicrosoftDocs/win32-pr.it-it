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
# <a name="ndf-diagnostics-example"></a>Esempio di diagnostica NDF

Nell'esempio seguente viene illustrato come avviare l'interfaccia utente di NDF e diagnosticare la connettività al sito Web https://www.microsoft.com .


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



L'interfaccia utente di NDF può essere avviata come finestra modale. A tale scopo, modificare il secondo parametro di [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) da **null** all'handle (HWND) della finestra padre.

Questo esempio può essere modificato per diagnosticare altre aree di rete. A tale scopo, sostituire la chiamata [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) con una delle altre funzioni di creazione degli eventi imprevisti, ad esempio [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) o [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




