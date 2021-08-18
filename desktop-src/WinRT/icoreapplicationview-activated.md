---
description: Si verifica quando viene Windows'app di Store.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: Evento ICoreApplicationView::Activated (Windows. ApplicationModel.Core.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e736d0fb5403fe76d6d402c261e6b7e5336dfc096d8c39d7b3300b93ab1332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560995"
---
# <a name="icoreapplicationviewactivated-event"></a>Evento ICoreApplicationView::Activated

Si verifica quando viene Windows'app di Store.

## <a name="syntax"></a>Sintassi


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*gestore* \[ Pollici\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Non chiamare il metodo [**Exit dall'interno**](/previous-versions//hh438368(v=vs.85)) del *gestore*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                         |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                               |
| Intestazione<br/>                   | <dl> <dt>Windows. ApplicationModel.Core.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.Core.idl</dt> </dl> |



 

 
