---
description: Le funzioni seguenti vengono usate per gestire i ticket di stampa.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Funzioni dell'API Print Ticket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a908da3aee9e9fa1c3b7181261164860be95193cb4dc0d34a7fe17e6f2a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033919"
---
# <a name="print-ticket-api-functions"></a>Funzioni dell'API Print Ticket

Le funzioni seguenti vengono usate per gestire i ticket di stampa.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                                  | Descrizione                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Converte una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un ticket di stampa.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Converte un print ticket in una [**struttura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Unisce due print ticket e restituisce un ticket di stampa valido e valido.<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Chiude un handle del provider di ticket di stampa.<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Converte una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un ticket di stampa all'interno di [**un oggetto IStream.**](/windows/desktop/Stg/istream-compound-file-implementation)<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Converte un print ticket in una [**struttura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Recupera le funzionalità della stampante formattate in conformità con XML [Print Schema.](./printschema.md)<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Recupera le funzionalità della stampante del dispositivo formattate in conformità con XML [Print Schema.](./printschema.md)<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Recupera le risorse dei dispositivi di stampa per una stampante formattata in conformità con XML [Print Schema.](./printschema.md)<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Unisce due print ticket e restituisce un ticket di stampa valido e valido.<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Apre un'istanza di un provider di ticket di stampa.<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Apre un'istanza di un provider di ticket di stampa.<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Recupera la versione più recente (più recente) dello [schema di](./printschema.md) stampa supportata dalla stampante specificata.<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Rilascia i buffer associati ai ticket di stampa e alle funzionalità di stampa.<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | Chiude un handle per un provider di ticket di stampa.<br/>                                                                                                 |



 

 

