---
description: Il metodo SetCutsOnly specifica se viene eseguito il rendering della transizione come taglia. In tal caso, la transizione viene eseguita immediatamente in corrispondenza del punto di taglio. Se il rendering di una transizione richiede molto tempo, è possibile visualizzarne l'anteprima come un'anteprima di riduzione per la velocità.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'Metodo IAMTimelineTrans:: SetCutsOnly (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333794"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>Metodo IAMTimelineTrans:: SetCutsOnly

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetCutsOnly` metodo specifica se viene eseguito il rendering della transizione come taglia. In tal caso, la transizione viene eseguita immediatamente in corrispondenza del punto di taglio. Se il rendering di una transizione richiede molto tempo, è possibile visualizzarne l'anteprima come un'anteprima di riduzione per la velocità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Val* 
</dt> <dd>

Specifica se eseguire il rendering della transizione come taglia. Se **true**, viene eseguito il rendering della transizione come taglia istantanea. Se **false**, viene eseguito il rendering della transizione sulla durata normale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il rendering di una transizione come taglia non è compatibile con lo scambio degli input. Vedere [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md). Se si chiama `SetCutsOnly` con un valore **true**, viene temporaneamente sostituita l'impostazione **SetSwapInputs** . L'impostazione solo per i tagli è pensata per l'anteprima, quindi questa limitazione non influisce sull'output dei file, ma è sufficiente ricordare di chiamare `SetCutsOnly` con il valore **false** prima di scrivere il file.

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




