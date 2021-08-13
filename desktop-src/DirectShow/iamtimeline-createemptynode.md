---
description: Il metodo CreateEmptyNode crea un nuovo oggetto sequenza temporale.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: Metodo IAMTimeline::CreateEmptyNode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f98073c7e3a4be7fa57858440e540769eef50c44fae4ddcaed459146bfc788a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389141"
---
# <a name="iamtimelinecreateemptynode-method"></a>Metodo IAMTimeline::CreateEmptyNode

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `CreateEmptyNode` metodo crea un nuovo oggetto sequenza temporale.

Usare questo metodo per creare oggetti sequenza temporale, anziché la **funzione CoCreateInstance,** perché questo metodo esegue routine di inizializzazione importanti. Ogni oggetto creato da questo metodo supporta almeno [**l'interfaccia IAMTimelineObj,**](iamtimelineobj.md) insieme ad altre interfacce specifiche di tale tipo di oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppObj* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) del nuovo oggetto.

</dd> <dt>

*Tipo* 
</dt> <dd>

Membro del tipo [**enumerato TIMELINE \_ MAJOR \_ TYPE,**](timeline-major-type.md) che specifica il tipo di oggetto da creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Non aggiungere il nuovo oggetto a un'altra istanza della sequenza temporale. Ogni oggetto in una sequenza temporale deve essere creato da tale sequenza temporale.

Se il metodo ha esito positivo, [**l'interfaccia IAMTimelineObj**](iamtimelineobj.md) restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




