---
description: Il Metodo ClearProps Cancella tutti i dati della proprietà dal setter della proprietà. L'applicazione può impostare i nuovi dati della proprietà dopo la chiamata a questa funzione.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'Metodo IPropertySetter:: ClearProps (qedit. h)'
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
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325484"
---
# <a name="ipropertysetterclearprops-method"></a>Metodo IPropertySetter:: ClearProps

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ClearProps` metodo cancella tutti i dati della proprietà dal setter della proprietà. L'applicazione può impostare i nuovi dati della proprietà dopo la chiamata a questa funzione.

La cancellazione dei dati della proprietà non comporta il ripristino dei valori originali delle proprietà dell'oggetto. Impedisce semplicemente a DirectShow di applicare eventuali altre modifiche. I valori delle proprietà vengono applicati in fase di esecuzione quando viene eseguito il rendering del progetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




