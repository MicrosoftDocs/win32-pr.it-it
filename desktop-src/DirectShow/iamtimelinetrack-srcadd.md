---
description: Il metodo SrcAdd aggiunge un'origine alla traccia.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Metodo IAMTimelineTrack:: SrcAdd (qedit. h)'
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
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325619"
---
# <a name="iamtimelinetracksrcadd-method"></a>Metodo IAMTimelineTrack:: SrcAdd

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

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

Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo. Restituisce E \_ nointerface se l'oggetto non è un oggetto di origine. In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.

## <a name="remarks"></a>Commenti

Impostare l'ora di inizio e di fine dell'origine prima di chiamare questo metodo. (Chiamare [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md).)

Attualmente, DES non può eseguire contemporaneamente il rendering di più di 75 origini compresse con codec di Gestione compressione video (VCM). Inoltre, se il progetto contiene più di 75 origini di questo tipo, è necessario utilizzare la riconnessione dinamica oppure il programma DES non può visualizzare in anteprima il progetto. Per ulteriori informazioni, vedere [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**Interfaccia IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




