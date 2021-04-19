---
description: L'interfaccia IAMTimelineTransable aggiunge transizioni a un oggetto in DirectShow editing Services (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interfaccia IAMTimelineTransable (qedit. h)
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
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332960"
---
# <a name="iamtimelinetransable-interface"></a>Interfaccia IAMTimelineTransable

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineTransable` interfaccia aggiunge transizioni a un oggetto in [DirectShow editing Services](directshow-editing-services.md) (des). Questa interfaccia è esposta da qualsiasi oggetto a cui possono essere applicate transizioni, tra cui tracce, composizioni e gruppi. Un oggetto che implementa questa interfaccia può avere un numero qualsiasi di transizioni, ma le transizioni non devono sovrapporsi nel tempo.

> [!Note]  
> L'audio non supporta le transizioni. Gli oggetti all'interno di gruppi audio possono esporre l' `IAMTimelineTransable` interfaccia, ma l'applicazione non deve aggiungere transizioni.

 

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineTransable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTransable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineTransable** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Recupera la prima transizione visualizzata all'ora specificata o successiva.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Recupera la prima transizione visualizzata all'ora specificata o in una versione successiva, con l'ora specificata come valore **REFTIME** .<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Recupera la transizione più vicina all'ora specificata.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Recupera la transizione più vicina all'ora specificata, specificata come valore **REFTIME** .<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Aggiunge una transizione all'oggetto.<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Recupera il numero di transizioni in questo oggetto.<br/>                                                                     |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
