---
title: Tipi di supporto di IAccessible
description: Tipi di supporto di IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710687"
---
# <a name="types-of-iaccessible-support"></a>Tipi di supporto di IAccessible

I server Microsoft Active Accessibility hanno due tipi di supporto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : nativo e con proxy. Gli elementi dell'interfaccia utente utilizzati in un'applicazione determinano il tipo di supporto appropriato. Molti server attualmente scritti sfruttano tutti i vantaggi dei proxy **IAccessible** e implementano solo **IAccessible** per i controlli che non sono inviati tramite proxy da Oleacc.dll, ad esempio controlli o controlli senza finestra con un nome di classe della finestra personalizzata.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Implementazione di Active Accessibility nativa](native-active-accessibility-implementation.md)
-   [Proxy IAccessible](iaccessible-proxies.md)

 

 




