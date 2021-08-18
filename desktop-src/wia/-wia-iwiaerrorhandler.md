---
description: L'interfaccia IWiaErrorHandler fornisce metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede dati di immagine, sia per i bit di anteprima che per i bit finali.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interfaccia IWiaErrorHandler (Wia.h)
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
ms.openlocfilehash: 6e97c5a146c23ce1ecdb2ba77cde5d37cd9091fc9d77e288042f02fc118816e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965590"
---
# <a name="iwiaerrorhandler-interface"></a>Interfaccia IWiaErrorHandler

**L'interfaccia IWiaErrorHandler** fornisce metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede dati di immagine, sia per i bit di anteprima che per i bit finali.

## <a name="members"></a>Membri

**L'interfaccia IWiaErrorHandler** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaErrorHandler** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWiaErrorHandler** include questi metodi.



| Metodo                                                                     | Descrizione                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Restituisce una stringa che descrive il codice di stato.<br/>                                             |
| [**Stato report**](-wia-iwiaerrorhandler-reportstatus.md)                 | Gestisce i messaggi di stato e di errore durante i trasferimenti di dati di immagine e li visualizza all'utente.<br/> |



 

## <a name="remarks"></a>Commenti

L'oggetto callback dell'applicazione **può implementare IWiaErrorHandler.**

Questa interfaccia non è progettata per gestire gli errori che si verificano all'esterno dei trasferimenti di dati di immagine, ad esempio errori di recupero o impostazione delle proprietà del dispositivo o callback non trasformati in un driver.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
