---
description: Ottiene il risultato di un'azione asincrona.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: Metodo IAsyncAction::GetResults
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 62196c7f8ded67bed0ecdb3ea33420de54301bbd379615126ada158ea9e725ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561053"
---
# <a name="iasyncactiongetresults-method"></a>Metodo IAsyncAction::GetResults

Ottiene il risultato di un'azione asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questo metodo restituisce sempre **S \_ OK**.

## <a name="remarks"></a>Commenti

La chiamata **al metodo GetResults** non ha alcun effetto se l'implementazione corrente ha un tipo dinamico [**di IAsyncAction.**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
