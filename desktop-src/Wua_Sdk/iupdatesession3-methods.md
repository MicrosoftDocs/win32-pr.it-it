---
description: L'interfaccia IUpdateSession3 definisce i metodi seguenti.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Metodi IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845af7bc4858aa713a3c044562c91325d337e49da0f413a3b2536c0129a85bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896741"
---
# <a name="iupdatesession3-methods"></a>Metodi IUpdateSession3

[**L'interfaccia IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) definisce i metodi seguenti.



| Metodo                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Restituisce un puntatore a [**un'interfaccia IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) per la sessione.                                                                                                                                                                                                                |
| [**Queryhistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Restituisce un puntatore a [**un'interfaccia IUpdateHistoryEntryCollection.**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) L'interfaccia contiene record di eventi corrispondenti nel computer. In questo modo [**il metodo QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) esegue in modo sincrono una query sul computer per la cronologia degli eventi di aggiornamento. |



 

Per informazioni sui membri ereditati da questa interfaccia, vedere le interfacce seguenti:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



