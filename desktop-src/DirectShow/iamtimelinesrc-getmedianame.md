---
description: Il metodo GetMediaName recupera il nome del file di origine rappresentato da questo oggetto di origine.
ms.assetid: 6f468628-10e1-4746-9c3a-6dae9aa3f6ad
title: Metodo IAMTimelineSrc::GetMediaName (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9919e89c61a07f9dd4c539bfb2bd04cbaefde1be3f06eae501a1c03c8df285bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131091"
---
# <a name="iamtimelinesrcgetmedianame-method"></a>Metodo IAMTimelineSrc::GetMediaName

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetMediaName` metodo recupera il nome del file di origine rappresentato da questo oggetto di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve il nome del file.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




