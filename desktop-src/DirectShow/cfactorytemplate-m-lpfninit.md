---
description: Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL. Può essere NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Membro CFactoryTemplate:: m_lpfnInit (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329820"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>Membro lpfnInit di CFactoryTemplate:: m \_

Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL. Può essere **null**.

## <a name="syntax"></a>Sintassi


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Osservazioni

Il tipo di puntatore a funzione è [**LPFNInitRoutine**](lpfninitroutine.md). Se si specifica questa funzione nella DLL, la funzione del punto di ingresso della DLL la chiama con i parametri seguenti:

-   *bLoading*: **true** quando la dll viene caricata, **false** quando la dll viene scaricata.
-   *rclsid*: puntatore al CLISD dell'oggetto, specificato nella variabile membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




