---
description: Rappresenta il metodo chiamato al completamento di un'azione asincrona.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interfaccia AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 5d7e091ab250dc8b7475dbf17a1d1502cd1c4aa110106584c8c8b190c927f4aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561176"
---
# <a name="asyncactioncompletedhandler-interface"></a>Interfaccia AsyncActionCompletedHandler

Rappresenta il metodo chiamato al completamento di un'azione asincrona.

## <a name="members"></a>Membri

**L'interfaccia AsyncActionCompletedHandler** eredita da [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo). **AsyncActionCompletedHandler** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia AsyncActionCompletedHandler** include questi metodi.



| Metodo                                               | Descrizione                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**evocare**](asyncactioncompletedhandler-invoke.md) | Richiama il metodo chiamato al completamento dell'azione asincrona specificata.<br/> |



 

## <a name="remarks"></a>Commenti

Assegnare **AsyncActionCompletedHandler** a [**un oggetto IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) per ricevere una notifica al completamento dell'azione asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Iasyncinfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

