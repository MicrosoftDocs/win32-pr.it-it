---
description: Il metodo SetPreviewMode imposta la modalità di anteprima per il gruppo.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: Metodo IAMTimelineGroup::SetPreviewMode (Qedit.h)
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
ms.openlocfilehash: 2f4c53372066ec28f3782fe53148eaba99489187c3be9b9ccf73195a7b1e6da9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756311"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>Metodo IAMTimelineGroup::SetPreviewMode

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

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

Modalità di anteprima. Se **TRUE,** il gruppo è in modalità di anteprima. Se **FALSE,** il gruppo è in modalità di creazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

In modalità di anteprima i fotogrammi vengono eliminati durante effetti lenti o transizioni per mantenere il video sincronizzato con l'audio. Di conseguenza, il video potrebbe risultare molto azzardato. In modalità di creazione viene eseguito il rendering di ogni frame. La modalità di creazione è appropriata per la scrittura di file. Per l'anteprima su schermo, il video potrebbe non essere sincronizzato con l'audio.

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




