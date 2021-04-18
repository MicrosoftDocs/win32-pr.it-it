---
description: Il metodo SplitAt suddivide l'oggetto all'ora specificata.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'Metodo IAMTimelineSplittable:: SplitAt (qedit. h)'
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
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329479"
---
# <a name="iamtimelinesplittablesplitat-method"></a>Metodo IAMTimelineSplittable:: SplitAt

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

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

Ora in cui dividere l'oggetto, relativo all'inizio della sequenza temporale, in unità 100-nanosecondi.

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

Se si suddivide un'origine, un effetto o una transizione, questo metodo crea un secondo oggetto dello stesso tipo. L'oggetto originale viene troncato in corrispondenza dell'ora di suddivisione specificata e il nuovo oggetto sostituisce la parte troncata. Il nuovo oggetto eredita tutte le stesse proprietà. In un oggetto di origine, il metodo suddivide anche tutti gli effetti che ricadeno sull'ora di divisione.

La chiamata di questo metodo su un track divide tutte le origini, gli effetti e le transizioni contenuti nella traccia in corrispondenza della fase di suddivisione specificata. Non crea una seconda traccia. Una traccia inizia al momento zero e si estende fino all'infinito.

Per una traccia, se il tempo di suddivisione è successivo a tutti gli elementi della traccia, il metodo restituisce \_ false. Per qualsiasi altro oggetto, se l'ora di divisione non rientra in un punto qualsiasi all'interno dell'oggetto, il metodo restituisce E \_ INVALIDARG.

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

 

 




