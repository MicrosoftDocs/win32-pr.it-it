---
description: Il metodo SetDefaultFPS imposta la frequenza dei fotogrammi predefinita dell'oggetto di origine.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Metodo IAMTimelineSrc:: SetDefaultFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330184"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>Metodo IAMTimelineSrc:: SetDefaultFPS

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetDefaultFPS` metodo imposta la frequenza dei fotogrammi predefinita dell'oggetto di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FPS* 
</dt> <dd>

Frequenza fotogrammi predefinita, in frame al secondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo oppure E \_ INVALIDARG se la frequenza dei fotogrammi specificata è minore di zero.

## <a name="remarks"></a>Commenti

Il motore di rendering utilizza questo valore se non è in grado di determinare la frequenza dei fotogrammi dal file di origine originale.

Chiamare questo metodo solo per i file di origine senza una frequenza dei fotogrammi predefinita. Per i file bitmap e JPEG, la frequenza dei fotogrammi predefinita è zero, che fa sì che l'origine venga sottoposta a rendering come immagine ancora. Per usare l'immagine come primo fotogramma in una sequenza DIB, impostare la frequenza dei fotogrammi su un valore maggiore di zero. Per ulteriori informazioni, vedere [utilizzo delle origini](working-with-sources.md).

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

 

 




