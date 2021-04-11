---
description: L'interfaccia IUpdateInstallationResult definisce le proprietà seguenti.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Proprietà di IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226224"
---
# <a name="iupdateinstallationresult-properties"></a>Proprietà di IUpdateInstallationResult

L'interfaccia [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) definisce le proprietà seguenti.



| Proprietà                                                           | Descrizione                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Ottiene il valore dell'eccezione **HRESULT** generato durante l'operazione su un aggiornamento.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Ottiene un valore booleano che indica se è necessario riavviare il sistema in un computer per completare l'installazione di un aggiornamento. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Ottiene un valore [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) che specifica il risultato di un'operazione su un aggiornamento.          |



 

 

 



