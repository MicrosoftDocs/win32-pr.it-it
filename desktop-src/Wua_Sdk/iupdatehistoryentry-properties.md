---
description: L'interfaccia IUpdateHistoryEntry definisce le proprietà seguenti.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Proprietà IUpdateHistoryEntry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5c6951857f72f4a9ee4f86cd29d42e024e05b87d58d589043f5a40e951d4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738270"
---
# <a name="iupdatehistoryentry-properties"></a>Proprietà IUpdateHistoryEntry

[**L'interfaccia IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) definisce le proprietà seguenti.



| Proprietà                                                               | Descrizione                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Ottiene l'identificatore dell'applicazione client che ha elaborato un aggiornamento.                                                  |
| [**Data**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Ottiene la data e l'ora in cui è stato applicato un aggiornamento.                                                                        |
| [**Descrizione**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Ottiene la descrizione di un aggiornamento.                                                                                       |
| [**Hresult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Ottiene il **valore HRESULT** restituito dall'operazione su un aggiornamento.                                             |
| [**Operazione**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Ottiene un [**valore UpdateOperation**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) che specifica l'operazione su un aggiornamento.                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Ottiene un [**valore OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) che specifica il risultato di un'operazione su un aggiornamento. |
| [**Selezione server**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Ottiene il [**valore ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) che indica quale server ha fornito un aggiornamento.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Ottiene l'identificatore del servizio di un servizio di aggiornamento che non è un Windows aggiornamento.                                           |
| [**Supporturl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Ottiene un collegamento ipertestuale alle informazioni di supporto specifiche della lingua per un aggiornamento.                                             |
| [**Titolo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Ottiene il titolo di un aggiornamento.                                                                                             |
| [**Note sulla disinstallazione**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Ottiene le note di disinstallazione di un aggiornamento.                                                                              |
| [**Passaggi di disinstallazione**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Ottiene [**l'interfaccia IStringCollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) che contiene i passaggi di disinstallazione per un aggiornamento.  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Ottiene il codice del risultato non mappato restituito da un'operazione su un aggiornamento.                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Ottiene una stringa. La stringa contiene l'identificatore univoco di un aggiornamento.                                                   |



 

 

 
