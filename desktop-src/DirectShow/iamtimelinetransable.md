---
description: L'interfaccia IAMTimelineTransable aggiunge transizioni a un oggetto in DirectShow Editing Services (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interfaccia IAMTimelineTransable (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6228b836f85251dda7f43d6c3b421d486b727c6bdc6c319b9cf7ca1e37d34a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052031"
---
# <a name="iamtimelinetransable-interface"></a>Interfaccia IAMTimelineTransable

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`IAMTimelineTransable`L'interfaccia aggiunge transizioni a un oggetto in [DirectShow Editing Services](directshow-editing-services.md) (DES). Questa interfaccia viene esposta da qualsiasi oggetto a cui possono essere applicate transizioni, tra cui tracce, composizione e gruppi. Un oggetto che implementa questa interfaccia può avere un numero qualsiasi di transizioni, ma le transizioni non devono sovrapporsi nel tempo.

> [!Note]  
> L'audio non supporta le transizioni. Gli oggetti all'interno di gruppi audio possono esporre l'interfaccia , ma l'applicazione non deve `IAMTimelineTransable` aggiungervi transizioni.

 

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineTransable** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTransable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IAMTimelineTransable** include questi metodi.



| Metodo                                                          | Descrizione                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Recupera la prima transizione visualizzata all'ora specificata o in un secondo momento.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Recupera la prima transizione visualizzata all'ora specificata o successiva, con l'ora specificata come **valore REFTIME.**<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Recupera la transizione più vicina all'ora specificata.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Recupera la transizione più vicina all'ora specificata, specificata come **valore REFTIME.**<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Aggiunge una transizione all'oggetto .<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Recupera il numero di transizioni su questo oggetto .<br/>                                                                     |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
