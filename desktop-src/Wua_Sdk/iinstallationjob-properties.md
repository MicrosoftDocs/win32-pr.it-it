---
description: L'interfaccia IInstallationJob definisce le proprietà seguenti.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Proprietà IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb1604e69efc1d716b77be7303fc2148e93c0fe6d4fe2bc1ccd299f18ed9d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896981"
---
# <a name="iinstallationjob-properties"></a>Proprietà IInstallationJob

[**L'interfaccia IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) definisce le proprietà seguenti.



| Proprietà                                            | Descrizione                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asyncstate**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Ottiene l'oggetto stato specifico del chiamante passato al metodo [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) [**o IUpdateInstaller.BeginUninstall.**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Ottiene un valore che indica se una chiamata al metodo [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) viene elaborata completamente. |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Ottiene un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati nell'installazione o nella disinstallazione.                                                                                                        |



 

 

 



