---
title: Esempio di diagnostica NDF
description: L'esempio seguente illustra come avviare l'interfaccia utente NDF e diagnosticare la connettività al sito Web http //www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa1971da12b7d707dc74b34497dff630ee8fdd8f93d5737ae3757bdde129fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802371"
---
# <a name="ndf-diagnostics-example"></a>Esempio di diagnostica NDF

L'esempio seguente illustra come avviare l'interfaccia utente NDF e diagnosticare la connettività al sito Web https://www.microsoft.com .


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



L'interfaccia utente NDF può essere avviata come finestra modale. A tale scopo, modificare il secondo parametro di [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) da **NULL** all'handle (HWND) della finestra padre.

Questo esempio può essere modificato per diagnosticare altre aree di rete. A tale scopo, sostituire la chiamata [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) con una delle altre funzioni di creazione degli eventi imprevisti, ad esempio [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) o [**NdfCreateWinSockIncident.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




