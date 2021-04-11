---
description: L'interfaccia IUpdateSession3 definisce i metodi seguenti.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Metodi IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128275"
---
# <a name="iupdatesession3-methods"></a>Metodi IUpdateSession3

L'interfaccia [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) definisce i metodi seguenti.



| Metodo                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Restituisce un puntatore a un'interfaccia [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) per la sessione.                                                                                                                                                                                                                |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Restituisce un puntatore a un'interfaccia [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) . L'interfaccia contiene i record degli eventi corrispondenti nel computer. In questo modo, il metodo [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) esegue una query in modo sincrono sul computer per la cronologia degli eventi di aggiornamento. |



 

Per informazioni sui membri ereditati da questa interfaccia, vedere le interfacce seguenti:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



