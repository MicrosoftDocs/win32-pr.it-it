---
description: Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.
title: 'Metodo IMultiMonitorDockingSite:: tomonitor'
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
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995200"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>Metodo IMultiMonitorDockingSite:: tomonitor

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

*punkSrc* \[ in\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntatore all'oggetto che implementa l'interfaccia [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per la quale viene modificato il monitoraggio.

</dd> <dt>

*hMonNew* \[ in\]
</dt> <dd>

Tipo: **HMONITOR**

Handle per il monitoraggio che sostituisce il monitoraggio predefinito esistente.

</dd> <dt>

*phMonOld* \[ out\]
</dt> <dd>

Tipo: **HMONITOR \** _

Quando la funzione restituisce un risultato, contiene un puntatore all'handle del monitor predefinito precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                   |



 

 
