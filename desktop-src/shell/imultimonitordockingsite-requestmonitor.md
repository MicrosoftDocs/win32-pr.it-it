---
description: Verifica che il monitoraggio sia attivo e disponibile.
title: Metodo IMultiMonitorDockingSite::RequestMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841972"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>Metodo IMultiMonitorDockingSite::RequestMonitor

Verifica che il monitoraggio sia attivo e disponibile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*punkSrc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntatore all'oggetto che implementa [**l'interfaccia IDockingWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)

</dd> <dt>

*phMon* \[ Pollici\]
</dt> <dd>

Tipo: **HMONITOR \***

Puntatore all'handle del monitoraggio predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/> |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                   |



 

 
