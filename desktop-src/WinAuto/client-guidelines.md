---
title: Linee guida per i client
description: Gli sviluppatori client devono usare le funzionalità seguenti per ottenere informazioni sugli elementi dell'interfaccia utente
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3cfa9a269d796d7071b2107bba2fde6717f42928b9c9dc8074f94afbdbe15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133944"
---
# <a name="client-guidelines"></a>Linee guida per i client

Gli sviluppatori client devono usare le funzionalità seguenti per ottenere informazioni sugli elementi dell'interfaccia utente:

-   Per ottenere [**un'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per gli oggetti, chiamare [**AccessibleObjectFromWindow,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromEvent.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   Per esaminare e modificare gli oggetti accessibili, usare le proprietà e i [**metodi IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
-   Per ricevere [WinEvents,](winevents-overview.md)chiamare [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) per registrare una funzione di callback WinEvent per gli eventi rilevanti per l'applicazione client.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Come i client ottengono gli ID figlio](how-clients-obtain-child-ids.md)

 

 




