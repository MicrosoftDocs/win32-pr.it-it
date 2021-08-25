---
title: Enumerazione VMMouseButton (VPCCOMInterfaces.h)
description: Specifica il pulsante del mouse.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- Enumerazione VMMouseButton Virtual PC
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4922942ee72971e1bd0d0aaa14336b09c7ede804f83b865779b851f4dfff463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006511"
---
# <a name="vmmousebutton-enumeration"></a>Enumerazione VMMouseButton

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Specifica il pulsante del mouse.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton \_ Left**
</dt> <dd>

Rappresenta il pulsante sinistro del mouse.

</dd> <dt>

<span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**VmMouseButton \_ Right**
</dt> <dd>

Rappresenta il pulsante destro del mouse.

</dd> <dt>

<span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**Centro \_ vmMouseButton**
</dt> <dd>

Pulsante centrale del mouse.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

