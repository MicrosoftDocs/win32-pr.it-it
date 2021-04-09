---
description: L'interfaccia IUpdateInstaller definisce le proprietà seguenti.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Proprietà di IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879438"
---
# <a name="iupdateinstaller-properties"></a>Proprietà di IUpdateInstaller

L'interfaccia [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) definisce le proprietà seguenti.



| Proprietà                                                                                      | Descrizione                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Ottiene e imposta un valore booleano che indica se visualizzare le richieste di origine all'utente durante l'installazione degli aggiornamenti.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Ottiene e imposta l'applicazione client corrente.                                                                                         |
| [**Della proprietà IsBusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Ottiene un valore booleano che indica se è in corso un'installazione o una disinstallazione di un computer in un determinato momento.        |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Ottiene o imposta un valore booleano che indica se forzare l'installazione o la disinstallazione di un aggiornamento.                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Ottiene e imposta un handle per la finestra padre che può contenere una finestra di dialogo.                                                            |
| [**ParentWindow**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Ottiene e imposta l'interfaccia che rappresenta la finestra padre che può contenere una finestra di dialogo.                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Ottiene un valore booleano che indica se è necessario riavviare il sistema prima di installare o disinstallare gli aggiornamenti.                   |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Ottiene e imposta un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati per l'installazione o la disinstallazione. |



 

 

 



