---
title: DRV_LOAD messaggio (Mmsystem.h)
description: Notifica al driver che è stato caricato. Il driver deve assicurarsi che siano presenti tutti i driver hardware e di supporto necessari per il corretto funzionamento.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD messaggio Windows Multimediali
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
ms.openlocfilehash: d74b8d0663e96f0dc700739c7b8b5f9304d478ed02bf9493f24d03a506c14a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678711"
---
# <a name="drv_load-message"></a>Messaggio DRV \_ LOAD

Notifica al driver che è stato caricato. Il driver deve assicurarsi che siano presenti tutti i driver hardware e di supporto necessari per il corretto funzionamento.

## <a name="parameters"></a>Parametri

Il *parametro hdrvr* è sempre zero. I *parametri dwDriverId*, *lParam1* e *lParam2* non vengono usati.

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo o zero in caso contrario.

## <a name="remarks"></a>Commenti

Il **messaggio DRV \_ LOAD** è sempre il primo messaggio ricevuto da un driver di dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> <dt>

[Messaggi del driver installabili](installable-driver-messages.md)
</dt> </dl>

 

 





