---
description: Il metodo SetOutputBuffering specifica il numero di fotogrammi sottoposti a rendering in anticipo durante l'anteprima.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: Metodo IAMTimelineGroup::SetOutputBuffering (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8187918a4f6d04df9c8c0eaff387a092f18181071ce6ba41c83de44fcb095bbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915191"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>Metodo IAMTimelineGroup::SetOutputBuffering

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SetOutputBuffering` metodo specifica il numero di fotogrammi sottoposti a rendering in anticipo durante l'anteprima.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nBuffer* \[ Pollici\]
</dt> <dd>

Numero di frame da bufferare durante l'anteprima. Deve essere maggiore o uguale a due.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Un buffer più grande richiede più memoria, ma può comportare un'anteprima più uniforme, soprattutto durante gli effetti o le transizioni che richiedono più tempo per il rendering. Il buffer predefinito è 30 fotogrammi.

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




