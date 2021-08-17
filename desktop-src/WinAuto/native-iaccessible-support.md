---
title: Supporto IAccessible nativo
description: Oleacc.dll implementa IAccIdentity per conto di OBJID CLIENT \ 160;Puntatori di interfaccia IAccessible e relativi elementi figlio di \_ elementi semplici immediati.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad499b96c668349cc481efd388a780ba094eff2ef6eb4ae52ab041aabea70fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565052"
---
# <a name="native-iaccessible-support"></a>Supporto IAccessible nativo

Oleacc.dll implementa [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) per conto dei puntatori di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) DEL [**\_ CLIENT OBJID**](object-identifiers.md) e dei relativi elementi figlio semplici immediati. Un puntatore a interfaccia **OBJID \_ CLIENT** **IAccessible** viene restituito quando [**WM \_ GETOBJECT**](wm-getobject.md) con *lParam*  =  **OBJID \_ CLIENT** viene inviato a **un HWND**, che rappresenta l'area client della finestra o del controllo nel suo complesso. L'elemento padre di tale puntatore a interfaccia **IAccessible** avrà in genere un ruolo [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ed è l'oggetto **IAccessible** restituito quando **WM \_ GETOBJECT** con *lParam*  =  [**OBJID \_ WINDOW**](object-identifiers.md) viene inviato a un hwnd.

Questi puntatori a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) si verificano in genere quando un proxy Oleacc.dll è sottoclassato o in cui un semplice controllo personalizzato ,ad esempio un contenitore **IAccessible** più un livello di elementi figlio semplici, fornisce un'implementazione **nativa di IAccessible.**

Le implementazioni [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) native più complesse, ad esempio la posizione in cui esiste una gerarchia **di IAccessible** s o in cui vengono usati ID oggetto personalizzati, devono implementare [**iAccIdentity.**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity)

 

 




