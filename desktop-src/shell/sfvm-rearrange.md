---
description: Notifica a IShellView di ridisporre gli elementi. Usato dal messaggio \_ SHShellFolderView.
title: SFVM_REARRANGE messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 03bb5b8d39a85d8ce4fb6e76b75967a642361f502ce3bcb20ca49f276a5221de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941981"
---
# <a name="sfvm_rearrange-message"></a>Messaggio DI \_ RIDISPORRE SFVM

Notifica a [**IShellView di ridisporre**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) gli elementi. Usato da [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Passato a [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids). Per altre informazioni su questo parametro, vedere [**IShellFolder::CompareIDs.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




