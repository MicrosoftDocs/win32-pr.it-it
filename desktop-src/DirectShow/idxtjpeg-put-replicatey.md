---
description: Il metodo put ReplicateY specifica il numero di volte in cui \_ il modello di cancellazione viene replicato verticalmente.
ms.assetid: f27e0d54-1d0f-42fe-9638-39f68b97f9c7
title: Metodo IDxtJpeg::p ut_ReplicateY (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 03c7f35ca5b12817045b537d45cc1abe71f3e8d5136b1db4ee7b46884ad5a568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316281"
---
# <a name="idxtjpegput_replicatey-method"></a>Metodo ReplicateY IDxtJpeg::p ut \_

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `put_ReplicateY` metodo specifica il numero di volte in cui il modello di cancellazione viene replicato verticalmente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ReplicateY(
  [in] long newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Numero di volte in cui il modello di cancellazione viene replicato verticalmente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

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

[**Interfaccia IDxtJpeg**](idxtjpeg.md)
</dt> </dl>

 

 




