---
description: Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Puntatore alla funzione LPFNInitRoutine (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327417"
---
# <a name="lpfninitroutine-function-pointer"></a>Puntatore alla funzione LPFNInitRoutine

Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.

## <a name="syntax"></a>Sintassi


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bLoading* 
</dt> <dd>

**True** quando la dll viene caricata, **false** quando la dll viene scaricata.

</dd> <dt>

*rclsid* 
</dt> <dd>

Puntatore al CLISD dell'oggetto, specificato nella variabile membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo puntatore a funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




