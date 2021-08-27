---
description: Il metodo AddFoundLocation aggiunge una directory alla cache della directory.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: Metodo IMediaLocator::AddFoundLocation (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ba466338e6d148e3c39a6bed4f7db413ad444ee792a4fd49b6e1499f29f0403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051641"
---
# <a name="imedialocatoraddfoundlocation-method"></a>Metodo IMediaLocator::AddFoundLocation

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `AddFoundLocation` metodo aggiunge una directory alla cache della directory.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Directoryname* 
</dt> <dd>

Percorso della directory da aggiungere alla cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il localizzatore multimediale mantiene una cache di percorsi di directory in cui sono stati trovati correttamente i file nelle ricerche precedenti. Quando individua correttamente un file, aggiunge la directory alla cache.

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

[**Interfaccia IMediaLocator**](imedialocator.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




