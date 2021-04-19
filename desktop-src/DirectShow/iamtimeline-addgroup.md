---
description: Il metodo AddGroup aggiunge un gruppo alla sequenza temporale.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'Metodo IAMTimeline:: AddGroup (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326807"
---
# <a name="iamtimelineaddgroup-method"></a>Metodo IAMTimeline:: AddGroup

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `AddGroup` metodo aggiunge un gruppo alla sequenza temporale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGroup* 
</dt> <dd>

Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) del gruppo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                   | Descrizione                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato superato il numero massimo di gruppi.<br/> |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L'oggetto non è un gruppo.<br/>         |



 

## <a name="remarks"></a>Commenti

Attualmente, le sequenze temporali supportano un massimo di 32 gruppi.

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

 

 




