---
description: Il metodo get \_ ErrorLog recupera il log degli errori corrente per questo oggetto.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: Metodo IAMSetErrorLog::get_ErrorLog (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ca9104ea1ea526719401d8974de51d356acb91b3c6539992fbcbe42c8a36d39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102731"
---
# <a name="iamseterrorlogget_errorlog-method"></a>Metodo IAMSetErrorLog::get \_ ErrorLog

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `get_ErrorLog` metodo recupera il log degli errori corrente per questo oggetto .

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMErrorLog del**](iamerrorlog.md) log degli errori. Se la sequenza temporale non ha un log degli errori, il valore viene impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se il valore restituito in *pVal* non è **NULL,** [**l'interfaccia IAMErrorLog**](iamerrorlog.md) ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

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

[**Interfaccia IAMSetErrorLog**](iamseterrorlog.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




