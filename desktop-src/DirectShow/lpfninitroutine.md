---
description: Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Puntatore a funzione LPFNInitRoutine (Combase.h)
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
ms.openlocfilehash: c07f22b9dc261fe9d7b073a1f1ab93aa49e482fb70c53288aeaf606e6be9aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685081"
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

*bLoad* 
</dt> <dd>

**TRUE** quando viene caricata la DLL, **FALSE** quando la DLL viene scaricata.

</dd> <dt>

*rclsid* 
</dt> <dd>

Puntatore all'interfaccia della riga di comando dell'oggetto, specificata nella variabile membro [**\_ ClsID CFactoryTemplate::m.**](cfactorytemplate-m-clsid.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo puntatore a funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




