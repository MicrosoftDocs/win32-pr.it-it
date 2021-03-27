---
description: Ottiene il monitoraggio predefinito corrente.
title: 'Metodo IMultiMonitorDockingSite:: getmonitor'
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
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994944"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>Metodo IMultiMonitorDockingSite:: getmonitor

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

*punkSrc* \[ in\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntatore all'oggetto che implementa l'interfaccia [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per la quale viene richiesto il monitoraggio.

</dd> <dt>

*phMon* \[ out\]
</dt> <dd>

Tipo: **HMONITOR \** _

Quando la funzione restituisce un risultato, contiene un puntatore all'handle del monitor predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                   |



 

 
