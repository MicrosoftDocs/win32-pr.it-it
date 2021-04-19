---
description: Il metodo CreateEmptyNode crea un nuovo oggetto sequenza temporale.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Metodo IAMTimeline:: CreateEmptyNode (qedit. h)'
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
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326802"
---
# <a name="iamtimelinecreateemptynode-method"></a>Metodo IAMTimeline:: CreateEmptyNode

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `CreateEmptyNode` metodo crea un nuovo oggetto sequenza temporale.

Utilizzare questo metodo per creare oggetti sequenza temporale anziché la funzione **CoCreateInstance** , perché questo metodo esegue routine di inizializzazione importanti. Ogni oggetto creato da questo metodo supporta almeno l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) , insieme ad altre interfacce specifiche per quel tipo di oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) del nuovo oggetto.

</dd> <dt>

*Tipo* 
</dt> <dd>

Membro del tipo enumerato della [**sequenza temporale \_ principale \_**](timeline-major-type.md) , che specifica il tipo di oggetto da creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Non aggiungere il nuovo oggetto a un'altra istanza della sequenza temporale. Ogni oggetto in una sequenza temporale deve essere creato da tale sequenza temporale.

Se il metodo ha esito positivo, l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




