---
title: Messaggio DRV_LOAD (mmsystem. h)
description: Notifica al driver che è stato caricato. Il driver deve verificare che siano presenti hardware e driver di supporto necessari per il corretto funzionamento.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964917"
---
# <a name="drv_load-message"></a>\_Messaggio di caricamento DRV

Notifica al driver che è stato caricato. Il driver deve verificare che siano presenti hardware e driver di supporto necessari per il corretto funzionamento.

## <a name="parameters"></a>Parametri

Il parametro *hdrvr* è sempre zero. I parametri *dwDriverId*, *lParam1* e *lParam2* non vengono usati.

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo o zero.

## <a name="remarks"></a>Commenti

Il messaggio di **\_ caricamento DRV** è sempre il primo messaggio ricevuto da un driver di dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> <dt>

[Messaggi di driver installabili](installable-driver-messages.md)
</dt> </dl>

 

 





