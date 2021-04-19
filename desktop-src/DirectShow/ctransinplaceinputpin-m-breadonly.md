---
Description: Flag che specifica se il flusso di input è di sola lettura. Il filtro upstream specifica queste informazioni quando chiama il metodo NotifyAllocator. Per impostazione predefinita, il valore è FALSE.
ms.assetid: d5a71c00-326c-45b4-b9c5-b67a0fe71bf5
title: 'Membro CTransInPlaceInputPin:: m_bReadOnly (Transip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bReadOnly
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2f66296c08b2461440e0615b225c62405fd99a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326197"
---
# <a name="ctransinplaceinputpinm_breadonly-member"></a>Membro bReadOnly di CTransInPlaceInputPin:: m \_

Flag che specifica se il flusso di input è di sola lettura. Il filtro upstream specifica queste informazioni quando chiama il metodo [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md) . Per impostazione predefinita, il valore è **false**.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bReadOnly;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




