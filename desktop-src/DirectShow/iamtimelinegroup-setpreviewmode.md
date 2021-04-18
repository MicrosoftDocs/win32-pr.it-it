---
description: Il metodo SetPreviewMode imposta la modalità di anteprima per il gruppo.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'Metodo IAMTimelineGroup:: SetPreviewMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331625"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>Metodo IAMTimelineGroup:: SetPreviewMode

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo SetPreviewMode imposta la modalità di anteprima per il gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fPreview* 
</dt> <dd>

Modalità di anteprima. Se **true**, il gruppo è in modalità di anteprima. Se **false**, il gruppo è in modalità di creazione.

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

 

 




