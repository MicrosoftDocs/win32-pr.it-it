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
ms.openlocfilehash: 9e5eeb2b99455d81bae36f1c5f26ed38126122bb58a5b8964a47cfb205f71ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942901"
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

*RCSrc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntatore all'oggetto che implementa [**l'interfaccia IDockingWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)

</dd> <dt>

*phMon* \[ Pollici\]
</dt> <dd>

Tipo: **HMONITOR \***

Puntatore all'handle del monitor predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                   |



 

 
