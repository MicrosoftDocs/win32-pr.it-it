---
description: Metodo del costruttore.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Costruttore CMsgThread. CMsgThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328835"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>Costruttore CMsgThread. CMsgThread

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMsgThread();
```



## <a name="parameters"></a>Parametri

Questo costruttore non ha parametri.

## <a name="remarks"></a>Commenti

La costruzione di un oggetto thread di messaggio non crea automaticamente il thread. Per creare il thread, è necessario chiamare la funzione membro [**CMsgThread:: CreateThread**](cmsgthread-createthread.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




