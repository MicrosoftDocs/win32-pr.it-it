---
description: Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.
title: Metodo IMultiMonitorDockingSite::SetMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: c79a2ec497e8eaaafead20e6fa01e10844f9c4786a158f869fe16e4eee19e7c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032399"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>Metodo IMultiMonitorDockingSite::SetMonitor

Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*punkSrc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntatore all'oggetto che implementa [**l'interfaccia IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per cui viene modificato il monitoraggio.

</dd> <dt>

*hMonNew* \[ Pollici\]
</dt> <dd>

Tipo: **HMONITOR**

Handle per il monitoraggio che sostituisce il monitoraggio predefinito esistente.

</dd> <dt>

*phMonOld* \[ Cambio\]
</dt> <dd>

Tipo: **HMONITOR \***

Quando questa funzione viene restituita, contiene un puntatore all'handle del monitoraggio predefinito precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                   |



 

 
