---
description: Il metodo OnFrames deve essere implementato dal monitoraggio. MCSVC chiama questo metodo quando il buffer di acquisizione è pieno o è trascorsa l'ora di aggiornamento.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: Metodo IMonitor::OnFrames (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a4138c35384753c8df79728a61decf78bf302d0dc9c0a71ca9f787d76a70a620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779171"
---
# <a name="imonitoronframes-method"></a>Metodo IMonitor::OnFrames

Il **metodo OnFrames** deve essere implementato dal monitoraggio. MCSVC chiama questo metodo quando il buffer di acquisizione è pieno o è trascorsa l'ora di aggiornamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Evento* \[ Pollici\]
</dt> <dd>

[UPDATE \_ Struttura EVENT](update-event.md) che contiene le informazioni sui frame usate per aggiornare gli eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è S \_ OK (uguale a NOERROR). MCSVC passa il valore restituito all'NPP per l'elaborazione.

Se il metodo ha esito negativo, il valore restituito è un codice di errore. MCSVC passa il valore restituito all'NPP per l'elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




