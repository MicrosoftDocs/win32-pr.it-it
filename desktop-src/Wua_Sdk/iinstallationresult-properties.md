---
description: L'interfaccia IInstallationResult definisce le proprietà seguenti.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Proprietà di IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049546"
---
# <a name="iinstallationresult-properties"></a>Proprietà di IInstallationResult

L'interfaccia [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) definisce le proprietà seguenti.



| Proprietà                                                     | Descrizione                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | Ottiene il valore **HRESULT** dell'eccezione, se presente, generato durante l'installazione.                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | Ottiene un valore booleano che indica se è necessario riavviare il computer per completare l'installazione o la disinstallazione di un aggiornamento. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | Ottiene un valore [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) che specifica il risultato di un'operazione su un aggiornamento.               |



 

 

 



