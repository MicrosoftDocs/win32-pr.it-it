---
description: "Il metodo SplitAt2 suddivide l'oggetto all'ora specificata. Questo metodo è equivalente a IAMTimelineSplittable:: SplitAt, ma accetta un valore REFTIME."
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'Metodo IAMTimelineSplittable:: SplitAt2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325722"
---
# <a name="iamtimelinesplittablesplitat2-method"></a>Metodo IAMTimelineSplittable:: SplitAt2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SplitAt2` metodo suddivide l'oggetto all'ora specificata. Questo metodo è equivalente a [**IAMTimelineSplittable:: SplitAt**](iamtimelinesplittable-splitat.md), ma accetta un valore [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Time* 
</dt> <dd>

Ora in cui dividere l'oggetto, relativo all'inizio della sequenza temporale, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I possibili valori sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Niente da dividere.<br/>                       |
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | L'oggetto non esiste in questo momento.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

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

[**Interfaccia IAMTimelineSplittable**](iamtimelinesplittable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




