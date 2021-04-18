---
description: Il metodo GetDefaultTransition recupera la transizione predefinita. Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'Metodo IAMTimeline:: GetDefaultTransition (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331097"
---
# <a name="iamtimelinegetdefaulttransition-method"></a>Metodo IAMTimeline:: GetDefaultTransition

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetDefaultTransition` metodo recupera la transizione predefinita. Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Riceve il GUID della transizione predefinita.

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




