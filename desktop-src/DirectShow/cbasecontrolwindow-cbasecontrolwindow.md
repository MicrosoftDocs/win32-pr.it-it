---
description: Metodo del costruttore.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Costruttore CBaseControlWindow. CBaseControlWindow (Ctlutil. h)
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
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325939"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>Costruttore CBaseControlWindow. CBaseControlWindow

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

*pName* 
</dt> <dd>

Puntatore alla descrizione dell'oggetto.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** di controllo, se l'oggetto fa parte di un'aggregazione. in caso contrario, deve essere **null**.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore HRESULT che indica l'esito positivo o negativo del metodo del costruttore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




