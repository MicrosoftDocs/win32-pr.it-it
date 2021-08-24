---
description: L'interfaccia IAutomaticUpdatesSettings definisce i metodi seguenti.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Metodi IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ae30a987dcf9d6573c179e7ef453c10c35a84b915b76a16439ba83a7174fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049469"
---
# <a name="iautomaticupdatessettings-methods"></a>Metodi IAutomaticUpdatesSettings

[**L'interfaccia IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definisce i metodi seguenti.



| Metodo                                               | Descrizione                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Aggiorna**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Recupera le impostazioni di Aggiornamenti automatici più recenti. |
| [**Salva**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Applica le impostazioni Aggiornamenti automatici corrente.  |



 

> [!Note]  
> In Windows RT non è più possibile usare il metodo [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) per configurare le impostazioni di Windows a livello di codice. L'operazione di configurazione non riesce se si usa **Salva** per impostare un valore diverso da 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



