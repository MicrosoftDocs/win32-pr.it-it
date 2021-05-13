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
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840642"
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
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/> |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                   |



 

 
