---
title: Proprietà IMsRdpClientNonScriptable5 GetRemoteMonitorsBoundingBox
description: Specifica il rettangolo di delimitazione del monitoraggio remoto.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Proprietà GetRemoteMonitorsBoundingBox Servizi Desktop remoto
- Proprietà GetRemoteMonitorsBoundingBox Servizi Desktop remoto , interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b308bf95389dcf043e87565be365ec69ecc34500ac187ee11a679349f18ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129889"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>Proprietà IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox

Specifica il rettangolo di delimitazione del monitoraggio remoto.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a>Valore proprietà

Riceve il bordo sinistro del rettangolo.

Riceve il bordo superiore del rettangolo.

Riceve il bordo destro del rettangolo.

Riceve il bordo inferiore del rettangolo.

## <a name="remarks"></a>Commenti

Tutte le coordinate sono in coordinate dello schermo virtuale, che sono relative all'angolo superiore sinistro del monitor primario. Se non si tratta del monitoraggio primario, alcuni o tutti questi valori possono essere negativi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





