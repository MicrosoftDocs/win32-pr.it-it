---
description: Il metodo VTrackInsBefore inserisce una traccia virtuale nella composizione con la priorità specificata.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'Metodo IAMTimelineComp:: VTrackInsBefore (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332034"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a>Metodo IAMTimelineComp:: VTrackInsBefore

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `VTrackInsBefore` metodo inserisce una traccia virtuale nella composizione con la priorità specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della traccia virtuale.

</dd> <dt>

*Priorità* 
</dt> <dd>

Priorità con cui inserire la traccia virtuale oppure-1 per inserire la traccia virtuale alla fine dell'elenco di priorità. L'elenco di priorità determina quali clip sono visibili. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                   | Descrizione                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argomento non valido.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L'oggetto non è una traccia virtuale.<br/> |



 

## <a name="remarks"></a>Commenti

Ogni traccia virtuale nella composizione ha un livello di priorità univoco. I livelli di priorità sono compresi tra 0 e *n* -1, dove *n* è il numero di tracce virtuali nella composizione. Per i gruppi video, un track virtuale nasconde qualsiasi traccia virtuale con un livello di priorità inferiore, tranne nei punti in cui la traccia è vuota o contiene una transizione. È possibile considerare le tracce virtuali come livelli nella composizione finale. Track 1 viene sovrapposto all'inizio della traccia 0, Track 2 è sovrapposto a Track 1 e così via.

Se si specifica-1 per il parametro *Priority* , la traccia virtuale viene inserita alla fine dell'elenco, con un valore di priorità più alto rispetto alle tracce esistenti. Se si specifica un valore di priorità già esistente nella composizione, ogni traccia con una priorità uguale o maggiore viene spostata verso l'alto di un livello di priorità.

**Esempio**: Track A ha priorità 0 e Track B ha priorità 1. Se la traccia C viene inserita con priorità 0, tenere traccia di uno spostamento alla priorità 1, mentre Track B passa alla priorità 2.

Se la priorità specificata è maggiore del numero corrente di tracce nella composizione, il metodo ha esito negativo.

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

[**Interfaccia IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




