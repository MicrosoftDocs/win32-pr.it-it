---
description: L'interfaccia IAutomaticUpdatesSettings definisce i metodi seguenti.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Metodi IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880390"
---
# <a name="iautomaticupdatessettings-methods"></a>Metodi IAutomaticUpdatesSettings

L'interfaccia [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definisce i metodi seguenti.



| Metodo                                               | Descrizione                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Aggiorna**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Recupera le impostazioni di Aggiornamenti automatici più recenti. |
| [**Salva**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Applica le impostazioni di Aggiornamenti automatici correnti.  |



 

> [!Note]  
> In Windows RT non è più possibile usare il metodo [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) per configurare le impostazioni Windows Update a livello di codice. L'operazione di configurazione non riesce se si usa **Save** per impostare un valore diverso da 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



