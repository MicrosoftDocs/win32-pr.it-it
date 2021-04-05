---
description: L'interfaccia IInstallationJob definisce le proprietà seguenti.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Proprietà di IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752095"
---
# <a name="iinstallationjob-properties"></a>Proprietà di IInstallationJob

L'interfaccia [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) definisce le proprietà seguenti.



| Proprietà                                            | Descrizione                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Ottiene l'oggetto di stato specifico del chiamante passato al metodo [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Ottiene un valore che indica se una chiamata al metodo [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) è stata elaborata completamente. |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Ottiene un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati durante l'installazione o la disinstallazione.                                                                                                        |



 

 

 



