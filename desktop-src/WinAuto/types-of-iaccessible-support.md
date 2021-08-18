---
title: Tipi di supporto IAccessible
description: Tipi di supporto IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb38ed0b5f7a306f2551085c77f77a3793efec3bc9281cd44d1d7277abe81fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993981"
---
# <a name="types-of-iaccessible-support"></a>Tipi di supporto IAccessible

Microsoft Active Accessibility server hanno due tipi di supporto [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo e proxy. Gli elementi dell'interfaccia utente usati in un'applicazione determinano il tipo di supporto appropriato. Molti server scritti oggi sfruttano appieno i proxy **IAccessible** e implementano **IAccessible** solo per i controlli che non sono proxy da Oleacc.dll, ad esempio controlli senza finestra o controlli con un nome di classe di finestra personalizzato.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Implementazione Active Accessibility nativa](native-active-accessibility-implementation.md)
-   [Proxy IAccessible](iaccessible-proxies.md)

 

 




