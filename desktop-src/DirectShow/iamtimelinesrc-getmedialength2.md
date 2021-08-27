---
description: Il metodo GetMediaLength2 recupera la lunghezza dei supporti di questo oggetto di origine. Questo metodo equivale a IAMTimelineSrc::GetMediaLength, ma accetta valori REFTIME.
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: Metodo IAMTimelineSrc::GetMediaLength2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 951e7909d55517489c77190434bf677ccdd8bee8dc1238ecd247d117a551610a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131111"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a>Metodo IAMTimelineSrc::GetMediaLength2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetMediaLength2` metodo recupera la lunghezza dei supporti di questo oggetto di origine. Questo metodo equivale a [**IAMTimelineSrc::GetMediaLength,**](iamtimelinesrc-getmedialength.md)ma accetta [**valori REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLength* 
</dt> <dd>

Riceve la lunghezza del supporto in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                     | Descrizione                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ NOTDETERMINED**</dt> </dl> | Gli orari dei supporti non sono impostati su questo oggetto.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>       | Argomento del puntatore **NULL.**<br/>              |



 

## <a name="remarks"></a>Commenti

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

 

 




