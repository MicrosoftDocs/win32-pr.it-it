---
title: Linee guida per i server
description: Per Microsoft Active Accessibility funzionino come previsto, i server devono fornire informazioni sull'accessibilità ai client.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b92d70a33dc8d397ff84fc3b9901dba044741d3044f6a7b7f6d1226aa5b683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614551"
---
# <a name="server-guidelines"></a>Linee guida per i server

Per Microsoft Active Accessibility funzionino come previsto, i server devono fornire informazioni sull'accessibilità ai client.

Per implementare [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)gli sviluppatori di server devono seguire questo processo di base.

1.  Creare oggetti accessibili implementando le proprietà e i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per gli elementi dell'interfaccia utente personalizzata e per il client dell'applicazione. Assicurarsi di fornire un'interfaccia duale che supporta **sia IAccessible** che [**IDispatch**](idispatch-interface.md) in modo che i client scritti in Microsoft Visual Basic e in vari linguaggi di scripting possano ottenere informazioni sugli oggetti.
2.  Chiamare [**NotifyWinEvent per**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) notificare ai client le modifiche apportate agli elementi dell'interfaccia utente personalizzata.
3.  Gestire [**WM \_ GETOBJECT per**](wm-getobject.md) fornire l'accesso agli oggetti accessibili.

Per suggerimenti e linee guida per la progettazione di oggetti accessibili, vedere [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>Contenuto della sezione

-   [Implementazione degli ID figlio da parte dei server](how-servers-implement-child-ids.md)

 

 




