---
description: L'interfaccia IUpdateHistoryEntry definisce le proprietà seguenti.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Proprietà di IUpdateHistoryEntry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3acdc9ed32c35028a253944d434c23231c5b6d
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/11/2021
ms.locfileid: "106322045"
---
# <a name="iupdatehistoryentry-properties"></a>Proprietà di IUpdateHistoryEntry

L'interfaccia [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) definisce le proprietà seguenti.



| Proprietà                                                               | Descrizione                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Ottiene l'identificatore dell'applicazione client che ha elaborato un aggiornamento.                                                  |
| [**Data**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Ottiene la data e l'ora in cui è stato applicato un aggiornamento.                                                                        |
| [**Descrizione**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Ottiene la descrizione di un aggiornamento.                                                                                       |
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Ottiene il valore **HRESULT** restituito dall'operazione su un aggiornamento.                                             |
| [**Operazione**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Ottiene un valore [**Insert**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) che specifica l'operazione su un aggiornamento.                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Ottiene un valore [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) che specifica il risultato di un'operazione su un aggiornamento. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Ottiene il valore [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) che indica quale server ha fornito un aggiornamento.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Ottiene l'identificatore di servizio di un servizio di aggiornamento che non è un aggiornamento di Windows.                                           |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Ottiene un collegamento ipertestuale alle informazioni di supporto specifiche della lingua per un aggiornamento.                                             |
| [**Titolo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Ottiene il titolo di un aggiornamento.                                                                                             |
| [**UninstallationNotes**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Ottiene le note di disinstallazione di un aggiornamento.                                                                              |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Ottiene l' [**interfaccia dell'oggetto che**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) contiene i passaggi di disinstallazione di un aggiornamento.  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Ottiene il codice di risultato senza mapping restituito da un'operazione su un aggiornamento.                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Ottiene una stringa. La stringa contiene l'identificatore univoco di un aggiornamento.                                                   |



 

 

 
