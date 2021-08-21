---
description: 'Costruttore CBaseControlWindow.CBaseControlWindow : metodo costruttore.'
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Costruttore CBaseControlWindow.CBaseControlWindow (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4944d121c4fe99ee36c893a4d51ca0cd72344dfa47dde17629f5ca2a1ce3fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660766"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>Costruttore CBaseControlWindow.CBaseControlWindow

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntatore all'oggetto filtro multimediale proprietario.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Puntatore alla sezione critica da usare per il blocco.

</dd> <dt>

*Pname* 
</dt> <dd>

Puntatore alla descrizione dell'oggetto.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore **all'interfaccia IUnknown di** controllo, se l'oggetto fa parte di un'aggregazione; in caso contrario, deve essere **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un valore HRESULT che indica l'esito positivo o negativo del metodo del costruttore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




