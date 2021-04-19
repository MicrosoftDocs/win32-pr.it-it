---
description: Il metodo IsClassID determina se un CLSID corrisponde a questo modello di classe.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Metodo CFactoryTemplate. IsClassID (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329830"
---
# <a name="cfactorytemplateisclassid-method"></a>CFactoryTemplate. IsClassID, metodo

Il `IsClassID` metodo determina se un CLSID corrisponde a questo modello di classe.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rclsid* 
</dt> <dd>

Riferimento a un CLSID.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il *parametro rclsid* è lo stesso CLSID della variabile membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) . in caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




