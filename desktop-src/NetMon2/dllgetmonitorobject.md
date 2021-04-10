---
description: La funzione DllGetMonitorObject deve essere implementata dal monitoraggio. MCSVC chiama questa funzione per creare un'istanza del monitoraggio.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Funzione di callback DllGetMonitorObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884866"
---
# <a name="dllgetmonitorobject-callback-function"></a>Funzione di callback DllGetMonitorObject

La funzione **DllGetMonitorObject** deve essere implementata dal monitoraggio. MCSVC chiama questa funzione per creare un'istanza del monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

UUID dei monitoraggi, illustrato di seguito, come definito nel file di intestazione IMonitor. h. Se viene fornito un UUID non valido, la funzione ha esito negativo e il monitoraggio deve restituire E \_ nointerface.

``` syntax
IID_IMonitor
```

</dd> <dt>

*ppObj* \[ out\]
</dt> <dd>

Puntatore a un puntatore che riceve l'interfaccia richiesta in *riid*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).

Se la funzione ha esito negativo, il valore restituito è un codice di errore. Quando viene restituito un codice di errore, MCSVC non crea l'oggetto di monitoraggio e il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) non viene chiamato sul puntatore a interfaccia.

## <a name="remarks"></a>Commenti

La funzione **DllGetMonitorObject** viene chiamata ogni volta che il MCSVC tenta di creare un'istanza del monitoraggio. Questa funzione presenta intenzionalmente una forte somiglianza con la funzione [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) più comune. La differenza principale consiste nel fatto che un CLSID non viene passato a **DllGetMonitorObject**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

