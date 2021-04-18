---
description: 'Il metodo GetMediaLength2 recupera la lunghezza del supporto di questo oggetto di origine. Questo metodo è equivalente a IAMTimelineSrc:: GetMediaLength, ma accetta valori REFTIME.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'Metodo IAMTimelineSrc:: GetMediaLength2 (qedit. h)'
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
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324260"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a>Metodo IAMTimelineSrc:: GetMediaLength2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetMediaLength2` metodo recupera la lunghezza del supporto di questo oggetto di origine. Questo metodo è equivalente a [**IAMTimelineSrc:: GetMediaLength**](iamtimelinesrc-getmedialength.md), ma accetta valori [**REFTIME**](reftime.md) .

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

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                     | Descrizione                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | Esito positivo.<br/>                                |
| <dl> <dt>**E \_ NOTDETERMINED**</dt> </dl> | I tempi dei supporti non sono impostati per questo oggetto.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>       | Argomento puntatore **null** .<br/>              |



 

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




