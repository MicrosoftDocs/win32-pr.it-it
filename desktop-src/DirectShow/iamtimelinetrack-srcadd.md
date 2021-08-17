---
description: Il metodo SrcAdd aggiunge un'origine alla traccia.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: Metodo IAMTimelineTrack::SrcAdd (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e705f840a073ee6796776f6f68c7b57df0bd972facf8f7a586792519735bfb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998751"
---
# <a name="iamtimelinetracksrcadd-method"></a>Metodo IAMTimelineTrack::SrcAdd

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SrcAdd` metodo aggiunge un'origine alla traccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrc* 
</dt> <dd>

Puntatore all'interfaccia [**IAMTimelineObj dell'oggetto di**](iamtimelineobj.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo. Restituisce E \_ NOINTERFACE se l'oggetto non è un oggetto di origine. In caso contrario, restituisce **un valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Impostare le ore di inizio e di arresto dell'origine prima di chiamare questo metodo. Chiamare [**IAMTimelineObj::SetStartStop.**](iamtimelineobj-setstartstop.md)

Attualmente, DES non può eseguire il rendering simultaneo di più di 75 origini compresse con codec VCM (Video Compression Manager). Inoltre, se il progetto nel suo complesso contiene più di 75 origini di questo tipo, è necessario usare la riconnessione dinamica o DES non può visualizzare in anteprima il progetto. Per altre informazioni, vedere [**IRenderEngine::SetDynamicReconnectLevel.**](irenderengine-setdynamicreconnectlevel.md)

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

[**Interfaccia IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




