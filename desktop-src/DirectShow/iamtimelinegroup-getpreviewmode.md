---
description: Il metodo GetPreviewMode recupera la modalità di anteprima per il gruppo.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'Metodo IAMTimelineGroup:: GetPreviewMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333682"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a>Metodo IAMTimelineGroup:: GetPreviewMode

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetPreviewMode` metodo recupera la modalità di anteprima per il gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfPreview* 
</dt> <dd>

Riceve un valore booleano che indica la modalità di anteprima. Se **true**, il gruppo è in modalità di anteprima. Se **false**, il gruppo è in modalità di creazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

In modalità di anteprima, i frame vengono eliminati durante le transizioni o gli effetti lenti per sincronizzare il video con l'audio. Il video potrebbe sembrare frammentato come risultato. In modalità di creazione, viene eseguito il rendering di ogni fotogramma. La modalità di creazione è appropriata per la scrittura di file; per l'anteprima su schermo, il video potrebbe non essere sincronizzato con l'audio.

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




