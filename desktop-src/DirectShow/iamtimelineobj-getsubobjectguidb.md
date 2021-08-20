---
description: Il metodo GetSubObjectGUIDB recupera il GUID del sottooggetto associato a questo oggetto sequenza temporale. Questo metodo equivale a IAMTimelineObj::GetSubObjectGUID, ma riceve un valore BSTR.
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: Metodo IAMTimelineObj::GetSubObjectGUIDB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79cf7c6a0b3f162f3f3baee2a46cfc0c2c2b61271b19e57549c73b4faa0594bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155382"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a>Metodo IAMTimelineObj::GetSubObjectGUIDB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetSubObjectGUIDB` metodo recupera il GUID del sottooggetto associato a questo oggetto sequenza temporale. Questo metodo equivale a [**IAMTimelineObj::GetSubObjectGUID,**](iamtimelineobj-getsubobjectguid.md)ma riceve un **valore BSTR.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve una stringa che rappresenta il GUID del sottooggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la stringa. L'applicazione deve **chiamare SysFreeString** per liberare la memoria.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




