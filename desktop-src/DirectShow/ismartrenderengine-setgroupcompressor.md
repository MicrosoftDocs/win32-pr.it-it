---
description: Specifica un filtro di compressione da utilizzare per il rendering del gruppo specificato.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: Metodo ISmartRenderEngine::SetGroupCompressor (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 002c1e9e6bbb2ea223fb208586b250455e2a1a6273babe2f8e38a51271ab8426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817162"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a>Metodo ISmartRenderEngine::SetGroupCompressor

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Specifica un filtro di compressione da utilizzare per il rendering del gruppo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gruppo* 
</dt> <dd>

Indice in base zero del gruppo.

</dd> <dt>

*pCompressor* 
</dt> <dd>

Puntatore [**all'interfaccia IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di compressione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

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

[**Interfaccia ISmartRenderEngine**](ismartrenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




