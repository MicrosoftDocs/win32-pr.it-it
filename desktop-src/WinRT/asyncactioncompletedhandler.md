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
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307085"
---
# <a name="asyncactioncompletedhandler-interface"></a>Interfaccia AsyncActionCompletedHandler

Rappresenta il metodo chiamato al completamento di un'azione asincrona.

## <a name="members"></a>Membri

L'interfaccia **asyncActionCompletedHandler** eredita da [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo). **AsyncActionCompletedHandler** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **asyncActionCompletedHandler** dispone di questi metodi.



| Metodo                                               | Descrizione                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Richiamare**](asyncactioncompletedhandler-invoke.md) | Richiama il metodo che viene chiamato quando l'azione asincrona specificata viene completata.<br/> |



 

## <a name="remarks"></a>Commenti

Assegnare un **asyncActionCompletedHandler** a un [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) per ricevere una notifica al completamento dell'azione asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

