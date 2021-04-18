---
description: L'interfaccia IWiaAppErrorHandler consente alle applicazioni di visualizzare le finestre di errore, durante i trasferimenti di dati, da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interfaccia IWiaAppErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312420"
---
# <a name="iwiaapperrorhandler-interface"></a>Interfaccia IWiaAppErrorHandler

L'interfaccia **IWiaAppErrorHandler** consente alle applicazioni di visualizzare le finestre di errore, durante i trasferimenti di dati, da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.

## <a name="members"></a>Membri

L'interfaccia **IWiaAppErrorHandler** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaAppErrorHandler** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWiaAppErrorHandler** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Ottiene un handle per la finestra di dialogo in cui vengono visualizzati i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | Gestisce i messaggi di errore e di stato del dispositivo durante i trasferimenti di dati di immagini e Visualizza i messaggi all'utente.<br/>                                  |



 

## <a name="remarks"></a>Commenti

L'oggetto di gestione degli errori, o callback, che implementa questa interfaccia viene passato in [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md) e [**IWiaTransfer:: upload**](-wia-iwiatransfer-upload.md).

Questa interfaccia non è progettata per gestire gli errori riscontrati al di fuori dei trasferimenti di dati di immagini, ad esempio errori durante il recupero o l'impostazione delle proprietà del dispositivo o callback non restituiti in un driver.

Un gestore degli errori del driver deve implementare [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), invece di **IWiaAppErrorHandler**.

L'oggetto che implementa questa interfaccia deve implementare anche [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).

Se si desidera che un gestore degli errori del driver e un gestore degli errori predefinito visualizzino le finestre dei messaggi di errore, ma non si desidera creare un gestore degli errori completo per l'applicazione, implementare questa interfaccia e implementare anche il metodo [**IWiaAppErrorHandler:: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) per restituire \_ lo stato WIA \_ non \_ gestito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
