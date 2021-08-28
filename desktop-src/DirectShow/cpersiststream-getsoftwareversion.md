---
description: Recupera la versione del software per questo flusso.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Metodo CPersistStream.GetSoftwareVersion (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0ba5e9f3fd3dc5e8f021e40c9cb70d95a136ae7c09d6f43826e436a32854170
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084271"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>Metodo CPersistStream.GetSoftwareVersion

Recupera la versione del software per questo flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** contenente il numero di versione. Ogni volta che il formato del flusso viene modificato, questa funzione deve essere modificata per restituire un numero maggiore di prima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




