---
description: Il metodo TransAdd aggiunge una transizione all'oggetto. Un oggetto può avere più transizioni, ma non devono sovrapporsi nel tempo. Le transizioni devono rientrare nei limiti temporali dell'oggetto.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'Metodo IAMTimelineTransable:: TransAdd (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332965"
---
# <a name="iamtimelinetransabletransadd-method"></a>Metodo IAMTimelineTransable:: TransAdd

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `TransAdd` metodo aggiunge una transizione all'oggetto. Un oggetto può avere più transizioni, ma non devono sovrapporsi nel tempo. Le transizioni devono rientrare nei limiti temporali dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTrans* 
</dt> <dd>

Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della transizione da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                   | Descrizione                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Impossibile inserire la transizione.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | *pTrans* non è un puntatore a una transizione.<br/> |



 

## <a name="remarks"></a>Commenti

Se la transizione si sovrappone a una transizione esistente, il metodo restituisce E \_ INVALIDARG.

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

[**Interfaccia IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




