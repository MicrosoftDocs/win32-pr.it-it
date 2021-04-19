---
description: Il metodo GetDefaultFPS recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine. Il motore di rendering utilizza questo valore se non è in grado di determinare la frequenza dei fotogrammi dall'origine originale.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'Metodo IAMTimelineSrc:: GetDefaultFPS (qedit. h)'
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
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324261"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>Metodo IAMTimelineSrc:: GetDefaultFPS

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetDefaultFPS` metodo recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine. Il motore di rendering utilizza questo valore se non è in grado di determinare la frequenza dei fotogrammi dall'origine originale.

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

Riceve la frequenza dei fotogrammi predefinita, in frame al secondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

La frequenza dei fotogrammi predefinita non è obbligatoria se il formato di file specifica la frequenza dei fotogrammi. Questo è il caso di formati audio e video.

Se l'origine è un'immagine bitmap o JPEG, il motore di rendering la usa come prima immagine in una sequenza di bitmap indipendente dal dispositivo (DIB), con una frequenza di fotogrammi uguale alla frequenza dei fotogrammi predefinita. Per eseguire il rendering di un'immagine statica, anziché una sequenza DIB, impostare la frequenza dei fotogrammi predefinita su 0.

Se l'origine è un GIF, non impostare la frequenza dei fotogrammi. Per gif animate, il file GIF specifica il ritardo tra le singole immagini.

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

 

 




