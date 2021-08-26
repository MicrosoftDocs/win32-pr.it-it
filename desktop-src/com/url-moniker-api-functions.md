---
title: Funzioni moniker URL
description: Funzioni moniker URL
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4dc19d47a933e9f93516630b25fdab2f64b21cb3755ac9fd5bbdfa7edaba51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992041"
---
# <a name="url-moniker-functions"></a>Funzioni moniker URL

Le funzioni del moniker URL isolano gli sviluppatori dalle complessità di creazione, gestione e uso dei moniker URL. Queste funzioni sono le seguenti:

-   [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))
-   [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))
-   [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))
-   [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))
-   [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))
-   [**Classe RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))
-   [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))
-   [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))
-   [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))

La familiarità con queste funzioni può essere la seguente:

-   Avere familiarità [**con CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) e [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) se si usano moniker URL nelle applicazioni autonome. Se si crea un controllo ActiveX, è necessario usare [**IBindHost::CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) anziché **CreateURLMoniker**.
-   Avere familiarità con [**RegisterMediaTypes,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) [**CreateFormatEnumerator,**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator) [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))e [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) se si eseguirà qualsiasi negoziazione MIME con moniker URL.
-   Acquisire familiarità con [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85)), [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85)), [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))e [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) solo se si ha un'esperienza significativa sia con i moniker URL che con COM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker URL](url-monikers.md)
</dt> </dl>

 

 