---
description: Il metodo InitialThreadProc chiama la routine del thread principale.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: Metodo CAMThread.InitialThreadProc (Wxutil. h)
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
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330545"
---
# <a name="camthreadinitialthreadproc-method"></a>Metodo tialThreadProc CAMThread.Ini

Il `InitialThreadProc` metodo chiama la routine del thread principale.

## <a name="syntax"></a>Sintassi


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PV* 
</dt> <dd>

`this` puntatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore DWORD** restituito da [**CAMThread:: ThreadProc**](camthread-threadproc.md). La classe derivata definisce questo valore.

## <a name="remarks"></a>Commenti

Il metodo [**CAMThread:: create**](camthread-create.md) usa questo metodo per la routine thread quando crea il thread. Usa il `this` puntatore come argomento del thread.

Questo metodo chiama il metodo [**CAMThread:: CoInitializeHelper**](camthread-coinitializehelper.md) e quindi ThreadProc.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




