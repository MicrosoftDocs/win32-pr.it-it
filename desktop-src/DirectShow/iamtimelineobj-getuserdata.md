---
description: Il metodo GetUserData recupera i dati persistenti definiti dall'applicazione.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'Metodo IAMTimelineObj:: GetUserData (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331516"
---
# <a name="iamtimelineobjgetuserdata-method"></a>Metodo IAMTimelineObj:: GetUserData

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetUserData` metodo recupera i dati persistenti definiti dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Puntatore a un buffer che riceve i dati. Per determinare le dimensioni del buffer da allocare, impostare questo parametro su **null**. La dimensione richiesta viene restituita in *psize*.

</dd> <dt>

*pSize* 
</dt> <dd>

Riceve le dimensioni dei dati in byte.

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




