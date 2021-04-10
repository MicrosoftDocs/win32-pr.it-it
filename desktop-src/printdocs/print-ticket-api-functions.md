---
description: Le funzioni seguenti vengono utilizzate per gestire i ticket di stampa.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Funzioni API del ticket di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5dfda941d0b0f7d99b0ffbef703a98e357ccc6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882821"
---
# <a name="print-ticket-api-functions"></a>Funzioni API del ticket di stampa

Le funzioni seguenti vengono utilizzate per gestire i ticket di stampa.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                                  | Descrizione                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Converte una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un Print Ticket.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Converte un ticket di stampa in una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Unisce due ticket di stampa e restituisce un ticket di stampa valido ed valido.<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Chiude un handle del provider di ticket di stampa.<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Converte una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un ticket di stampa all'interno di un [**IStream**](/windows/desktop/Stg/istream-compound-file-implementation).<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Converte un ticket di stampa in una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Recupera le funzionalità della stampante formattate in conformità con lo [schema di stampa](./printschema.md)XML.<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Recupera le funzionalità della stampante del dispositivo formattate in conformità con lo [schema di stampa](./printschema.md)XML.<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Consente di recuperare le risorse dei dispositivi di stampa per una stampante formattata in conformità con lo [schema di stampa](./printschema.md)XML.<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Unisce due ticket di stampa e restituisce un ticket di stampa valido ed valido.<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Apre un'istanza di un provider di ticket di stampa.<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Apre un'istanza di un provider di ticket di stampa.<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Recupera la versione più recente dello [schema di stampa](./printschema.md) supportata dalla stampante specificata.<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Rilascia i buffer associati ai ticket di stampa e alle funzionalità di stampa.<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | Chiude un handle a un provider di ticket di stampa.<br/>                                                                                                 |



 

 

