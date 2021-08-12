---
description: L'interfaccia IWiaAppErrorHandler consente alle applicazioni di visualizzare le finestre di errore (durante i trasferimenti di dati) da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interfaccia IWiaAppErrorHandler (Wia.h)
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
ms.openlocfilehash: 385a97a71d7017cba5bbfffd0833068a74acbe9d7281f8308b003a525b3f60f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441347"
---
# <a name="iwiaapperrorhandler-interface"></a>Interfaccia IWiaAppErrorHandler

**L'interfaccia IWiaAppErrorHandler** consente alle applicazioni di visualizzare le finestre di errore (durante i trasferimenti di dati) da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.

## <a name="members"></a>Membri

**L'interfaccia IWiaAppErrorHandler** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaAppErrorHandler** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWiaAppErrorHandler.**



| Metodo                                                        | Descrizione                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Ottiene un handle per la finestra di dialogo che visualizza i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | Gestisce lo stato del dispositivo e i messaggi di errore durante i trasferimenti di dati di immagine e visualizza i messaggi all'utente.<br/>                                  |



 

## <a name="remarks"></a>Commenti

L'oggetto di gestione degli errori, o callback, che implementa questa interfaccia viene passato in [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md) e [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).

Questa interfaccia non è progettata per gestire gli errori rilevati all'esterno dei trasferimenti di dati di immagine, ad esempio errori nel recupero o nell'impostazione delle proprietà del dispositivo o dei callback non annullati in un driver.

Un gestore degli errori del driver deve implementare [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)anziché **IWiaAppErrorHandler**.

L'oggetto che implementa questa interfaccia deve implementare [**anche IWiaTransferCallback.**](-wia-iwiatransfercallback.md)

Se si desidera che un gestore degli errori del driver e un gestore degli errori predefinito visualizzano le finestre dei messaggi di errore, ma non si vuole creare un gestore errori completo per l'applicazione, implementare questa interfaccia e implementare anche il metodo [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) per restituire WIA \_ STATUS NOT \_ \_ HANDLED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
