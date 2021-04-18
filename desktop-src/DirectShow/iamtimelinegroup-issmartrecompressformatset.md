---
description: Il metodo IsSmartRecompressFormatSet determina se è stato impostato un formato di ricompressione intelligente per il gruppo.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'Metodo IAMTimelineGroup:: IsSmartRecompressFormatSet (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328613"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a>Metodo IAMTimelineGroup:: IsSmartRecompressFormatSet

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `IsSmartRecompressFormatSet` metodo determina se è stato impostato un formato di ricompressione intelligente per il gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* 
</dt> <dd>

Riceve un valore booleano che indica se è stato impostato un formato di compressione. Se **true**, è stato impostato un formato di compressione.

</dd> </dl>

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




