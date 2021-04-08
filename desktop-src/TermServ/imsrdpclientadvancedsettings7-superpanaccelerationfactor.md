---
title: Proprietà SuperPanAccelerationFactor di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore che indica il fattore di accelerazione SuperPan. Il fattore di accelerazione SuperPan determina la rapidità con cui lo schermo esegue il Pan in modalità SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SuperPanAccelerationFactor
- Servizi Desktop remoto proprietà SuperPanAccelerationFactor, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà SuperPanAccelerationFactor
- Servizi Desktop remoto proprietà SuperPanAccelerationFactor, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964979"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a>Proprietà IMsRdpClientAdvancedSettings7:: SuperPanAccelerationFactor

Specifica o recupera un valore che indica il fattore di accelerazione SuperPan. Il fattore di accelerazione SuperPan determina la rapidità con cui lo schermo esegue il Pan in modalità SuperPan. Il fattore di accelerazione è il numero di pixel che la visualizzazione schermo scorre in una determinata direzione per ogni pixel del movimento del mouse da parte del client.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a>Valore proprietà

Fattore di accelerazione SuperPan da impostare. Il fattore di accelerazione SuperPan è il numero di pixel che la visualizzazione schermo scorre in una determinata direzione per ogni pixel del movimento del mouse.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su SuperPan, vedere [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





