---
description: Specifica un filtro di compressione da usare quando si esegue il rendering del gruppo specificato.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'Metodo ISmartRenderEngine:: SetGroupCompressor (qedit. h)'
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
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333431"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a>Metodo ISmartRenderEngine:: SetGroupCompressor

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Specifica un filtro di compressione da usare quando si esegue il rendering del gruppo specificato.

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

Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di compressione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

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

[**Interfaccia ISmartRenderEngine**](ismartrenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




