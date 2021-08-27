---
description: Il metodo GetDefaultFPS recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine. Il motore di rendering usa questo valore se non è in grado di determinare la frequenza dei fotogrammi dall'origine originale.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: Metodo IAMTimelineSrc::GetDefaultFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 92154a4c97c46307a764a7dba22ff2e003621db59cdb962ff025635022a5384b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131211"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>Metodo IAMTimelineSrc::GetDefaultFPS

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetDefaultFPS` metodo recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine. Il motore di rendering usa questo valore se non è in grado di determinare la frequenza dei fotogrammi dall'origine originale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFPS* 
</dt> <dd>

Riceve la frequenza fotogrammi predefinita, in fotogrammi al secondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

La frequenza fotogrammi predefinita non è necessaria se il formato di file specifica la frequenza dei fotogrammi. Questo è il caso dei formati audio e video.

Se l'origine è un'immagine bitmap o JPEG, il motore di rendering la usa come prima immagine in una sequenza DIB (Device-Independent Bitmap), con una frequenza di fotogrammi uguale alla frequenza fotogrammi predefinita. Per eseguire il rendering di un'immagine statica, anziché di una sequenza DIB, impostare la frequenza fotogrammi predefinita su 0.

Se l'origine è un file GIF, non impostare la frequenza dei fotogrammi. Per le GIF animate, il file GIF specifica il ritardo tra ogni immagine.

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

 

 




