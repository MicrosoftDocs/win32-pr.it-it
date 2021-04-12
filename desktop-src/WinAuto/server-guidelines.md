---
title: Linee guida sul server
description: Affinché Microsoft Active Accessibility funzioni come previsto, i server devono fornire informazioni sull'accessibilità ai client.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395510"
---
# <a name="server-guidelines"></a>Linee guida sul server

Affinché Microsoft Active Accessibility funzioni come previsto, i server devono fornire informazioni sull'accessibilità ai client.

Per implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), è necessario che gli sviluppatori di server seguano questo processo di base.

1.  Creare oggetti accessibili implementando le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per gli elementi dell'interfaccia utente personalizzati e per il client dell'applicazione. Assicurarsi di fornire un'interfaccia duale che supporti sia **IAccessible** che [**IDispatch**](idispatch-interface.md) in modo che i client scritti in Microsoft Visual Basic e vari linguaggi di scripting possano ottenere informazioni sugli oggetti.
2.  Chiamare [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per notificare ai client le modifiche apportate agli elementi dell'interfaccia utente personalizzata.
3.  Gestire [**WM \_ GetObject**](wm-getobject.md) per fornire l'accesso agli oggetti accessibili.

Per suggerimenti e linee guida per la progettazione di oggetti accessibili, vedere [la guida per gli sviluppatori per i server Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>Contenuto della sezione

-   [Modalità di implementazione degli ID figlio da server](how-servers-implement-child-ids.md)

 

 




