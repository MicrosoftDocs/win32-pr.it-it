---
description: Il metodo InitialThreadProc chiama la routine del thread principale.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Inimetodo tialThreadProc (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d12e8d41ac0c6e1fd2af06c21accbb5c62e4eb25f2fc3f6c36988101a9b64d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540301"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.Inimetodo tialThreadProc

Il `InitialThreadProc` metodo chiama la routine del thread principale.

## <a name="syntax"></a>Sintassi


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pv* 
</dt> <dd>

`this` Puntatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore DWORD** restituito da [**CAMThread::ThreadProc.**](camthread-threadproc.md) La classe derivata definisce questo valore.

## <a name="remarks"></a>Commenti

Il [**metodo CAMThread::Create**](camthread-create.md) usa questo metodo per la routine del thread quando crea il thread. Usa il `this` puntatore come argomento del thread.

Questo metodo chiama il [**metodo CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) e quindi ThreadProc.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




