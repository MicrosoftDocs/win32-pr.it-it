---
description: Il metodo SpliceWithNext unisce l'oggetto di origine a un altro oggetto di origine.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'Metodo IAMTimelineSrc:: SpliceWithNext (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325179"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>Metodo IAMTimelineSrc:: SpliceWithNext

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SpliceWithNext` metodo unisce l'oggetto di origine a un altro oggetto di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNext* 
</dt> <dd>

Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine da aggiungere all'origine corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Tra i possibili valori restituiti sono inclusi i seguenti:



| Codice restituito                                                                                   | Descrizione                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argomento non valido.<br/>                                             |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L'oggetto specificato dal parametro *pNext* non è un oggetto di origine.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null** .<br/>                                    |



 

## <a name="remarks"></a>Commenti

Come attualmente implementato, questo metodo elimina tutti gli effetti su *pNext*.

Affinché questo metodo abbia esito positivo, *pNext* deve essere un frame di corrispondenza dell'oggetto di origine corrente, definito nel modo seguente:

-   Deve condividere lo stesso file di origine.
-   L'ora di inizio del supporto deve essere uguale all'ora di arresto del supporto dell'origine corrente.
-   La velocità di riproduzione deve essere la stessa. La velocità di riproduzione è durata media divisa per la durata della sequenza temporale.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




