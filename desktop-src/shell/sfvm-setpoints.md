---
description: Imposta i punti degli oggetti attualmente selezionati sull'oggetto dati nei comandi Copy e Cut. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_SETPOINTS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234087"
---
# <a name="sfvm_setpoints-message"></a>SFVM \_ messaggi di setpoint

Imposta i punti degli oggetti attualmente selezionati sull'oggetto dati nei comandi **Copy** e **Cut** . Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdtobj* \[ in\]
</dt> <dd>Puntatore a un <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> dei comandi **Copy** e **Cut** .</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre zero.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
