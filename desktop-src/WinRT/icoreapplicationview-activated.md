---
description: Si verifica quando viene attivata un'app di Windows Store.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Evento ICoreApplicationView:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226100"
---
# <a name="icoreapplicationviewactivated-event"></a>Evento ICoreApplicationView:: Activated

Si verifica quando viene attivata un'app di Windows Store.

## <a name="syntax"></a>Sintassi


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*gestore* \[ di in\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Non chiamare il metodo [**Exit**](/previous-versions//hh438368(v=vs.85)) dall'interno del *gestore*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                         |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                               |
| Intestazione<br/>                   | <dl> <dt>Windows. ApplicationModel. Core. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. Core. idl</dt> </dl> |



 

 
