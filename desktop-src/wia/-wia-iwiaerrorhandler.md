---
description: L'interfaccia IWiaErrorHandler fornisce i metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede i dati dell'immagine, sia per l'anteprima che per i bit finali.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interfaccia IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130011"
---
# <a name="iwiaerrorhandler-interface"></a>Interfaccia IWiaErrorHandler

L'interfaccia **IWiaErrorHandler** fornisce i metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede i dati dell'immagine, sia per l'anteprima che per i bit finali.

## <a name="members"></a>Membri

L'interfaccia **IWiaErrorHandler** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaErrorHandler** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWiaErrorHandler** dispone di questi metodi.



| Metodo                                                                     | Descrizione                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Restituisce una stringa che descrive il codice di stato.<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Gestisce i messaggi di stato e di errore durante il trasferimento dei dati dell'immagine e li visualizza all'utente.<br/> |



 

## <a name="remarks"></a>Commenti

L'oggetto callback dell'applicazione può implementare **IWiaErrorHandler**.

Questa interfaccia non è progettata per gestire gli errori riscontrati al di fuori dei trasferimenti di dati di immagini, ad esempio errori durante il recupero o l'impostazione delle proprietà del dispositivo o callback non restituiti in un driver.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
