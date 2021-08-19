---
description: Il metodo ClearProps cancella tutti i dati delle proprietà dal setter di proprietà. L'applicazione può impostare nuovi dati di proprietà dopo aver chiamato questa funzione.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: Metodo IPropertySetter::ClearProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dfe5db4d7ae1f4a2d7a070a3d735264e61dfbdb621f99b9cbb2e1040213b56c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818590"
---
# <a name="ipropertysetterclearprops-method"></a>Metodo IPropertySetter::ClearProps

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `ClearProps` metodo cancella tutti i dati delle proprietà dal setter di proprietà. L'applicazione può impostare nuovi dati di proprietà dopo aver chiamato questa funzione.

La cancellazione dei dati della proprietà non ripristina i valori originali delle proprietà dell'oggetto. Impedisce semplicemente DirectShow di applicare altre modifiche. I valori delle proprietà vengono applicati in fase di esecuzione durante il rendering del progetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




