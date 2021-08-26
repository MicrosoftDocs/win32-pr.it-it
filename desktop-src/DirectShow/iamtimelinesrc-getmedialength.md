---
description: Il metodo GetMediaLength recupera la lunghezza dei supporti di questo oggetto di origine.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: Metodo IAMTimelineSrc::GetMediaLength (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72aeb68b3b3f9b31dc9ba00b2ffe8d82e2df8f8c5271abffcbd7737fa65203ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131181"
---
# <a name="iamtimelinesrcgetmedialength-method"></a>Metodo IAMTimelineSrc::GetMediaLength

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetMediaLength` metodo recupera la lunghezza dei supporti di questo oggetto di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLength* 
</dt> <dd>

Riceve la lunghezza del supporto in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                     | Descrizione                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ NOTDETERMINED**</dt> </dl> | I tempi dei supporti non sono impostati su questo oggetto.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>       | Argomento del puntatore **NULL.**<br/>              |



 

## <a name="remarks"></a>Commenti

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




