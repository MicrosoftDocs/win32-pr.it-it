---
description: L'interfaccia IUpdateInstaller definisce le proprietà seguenti.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Proprietà di IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c6076e395e98ef21cd54fbf45ffdc5e57bc29fa8ceffc78c16d9a9a0d2bc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049149"
---
# <a name="iupdateinstaller-properties"></a>Proprietà di IUpdateInstaller

[**L'interfaccia IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) definisce le proprietà seguenti.



| Proprietà                                                                                      | Descrizione                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Ottiene e imposta un valore booleano che indica se visualizzare le richieste di origine all'utente durante l'installazione degli aggiornamenti.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Ottiene e imposta l'applicazione client corrente.                                                                                         |
| [**Isbusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Ottiene un valore booleano che indica se è in corso un'installazione o una disinstallazione in un computer in un momento specifico.        |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Ottiene o imposta un valore booleano che indica se installare o disinstallare forzatamente un aggiornamento.                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Ottiene e imposta un handle per la finestra padre che può contenere una finestra di dialogo.                                                            |
| [**Finestra padre**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Ottiene e imposta l'interfaccia che rappresenta la finestra padre che può contenere una finestra di dialogo.                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Ottiene un valore booleano che indica se è necessario un riavvio del sistema prima di installare o disinstallare gli aggiornamenti.                   |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Ottiene e imposta un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati per l'installazione o la disinstallazione. |



 

 

 



