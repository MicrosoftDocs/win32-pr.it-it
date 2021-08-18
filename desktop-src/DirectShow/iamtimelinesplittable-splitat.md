---
description: Il metodo SplitAt suddivide l'oggetto all'ora specificata.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: Metodo IAMTimelineSplittable::SplitAt (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cdcedc25cf7f0998c6eac11de63f6e0d329e2ca8500576e0ad9e69cfc0bb3067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052411"
---
# <a name="iamtimelinesplittablesplitat-method"></a>Metodo IAMTimelineSplittable::SplitAt

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SplitAt` metodo suddivide l'oggetto all'ora specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Time* 
</dt> <dd>

Ora in cui dividere l'oggetto, rispetto all'inizio della sequenza temporale, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I possibili valori sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Niente da dividere.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | L'oggetto non esiste in questo momento.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Se si divide un'origine, un effetto o una transizione, questo metodo crea un secondo oggetto dello stesso tipo. L'oggetto originale viene troncato in corrispondenza della divisione specificata e il nuovo oggetto sostituisce la parte troncata. Il nuovo oggetto eredita tutte le stesse proprietà. In un oggetto di origine, il metodo suddivide anche tutti gli effetti che rientrano nel tempo di divisione.

La chiamata di questo metodo su una traccia suddivide tutte le origini, gli effetti e le transizioni contenuti nella traccia in corrispondenza del tempo di suddivisione specificato. Non crea una seconda traccia. Una traccia inizia all'ora zero ed è estesa all'infinito.

Per una traccia, se il tempo di divisione è successivo a tutti gli elementi della traccia, il metodo restituisce S \_ FALSE. Per qualsiasi altro oggetto, se il tempo di divisione non rientra nell'oggetto , il metodo restituisce E \_ INVALIDARG.

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

[**Interfaccia IAMTimelineSplittable**](iamtimelinesplittable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




