---
title: Proprietà GetRemoteMonitorsBoundingBox di IMsRdpClientNonScriptable5
description: Specifica il rettangolo di delimitazione del monitor remoto.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GetRemoteMonitorsBoundingBox
- Servizi Desktop remoto proprietà GetRemoteMonitorsBoundingBox, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà GetRemoteMonitorsBoundingBox
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
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964509"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>Proprietà IMsRdpClientNonScriptable5:: GetRemoteMonitorsBoundingBox

Specifica il rettangolo di delimitazione del monitor remoto.

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

Tutte le coordinate si trovano nelle coordinate dello schermo virtuale, che sono relative all'angolo superiore sinistro del monitor primario. Se non si tratta del monitoraggio principale, alcuni o tutti questi valori potrebbero essere negativi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





