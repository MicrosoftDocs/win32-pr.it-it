---
description: L'interfaccia IUpdateInstallationResult definisce le proprietà seguenti.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Proprietà IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7574d6fd84afc737d67147c8b40e1e501857f6c19d69bcce4b4b7216bb9c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994411"
---
# <a name="iupdateinstallationresult-properties"></a>Proprietà IUpdateInstallationResult

[**L'interfaccia IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) definisce le proprietà seguenti.



| Proprietà                                                           | Descrizione                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Hresult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Ottiene il **valore dell'eccezione HRESULT** generato durante l'operazione su un aggiornamento.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Ottiene un valore booleano che indica se è necessario un riavvio del sistema in un computer per completare l'installazione di un aggiornamento. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Ottiene un [**valore OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) che specifica il risultato di un'operazione su un aggiornamento.          |



 

 

 



