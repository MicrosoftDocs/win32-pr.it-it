---
description: Ottiene il monitoraggio predefinito corrente.
title: Metodo IMultiMonitorDockingSite::GetMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 63609dc545e8f69ae2023e6659158297a65fdb7b549071126702b163c04555f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661891"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>Metodo IMultiMonitorDockingSite::GetMonitor

Ottiene il monitoraggio predefinito corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*punkSrc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntatore all'oggetto che implementa [**l'interfaccia IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per cui viene richiesto il monitoraggio.

</dd> <dt>

*phMon* \[ Cambio\]
</dt> <dd>

Tipo: **HMONITOR \***

Quando la funzione viene restituita, contiene un puntatore all'handle del monitoraggio predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                   |



 

 
