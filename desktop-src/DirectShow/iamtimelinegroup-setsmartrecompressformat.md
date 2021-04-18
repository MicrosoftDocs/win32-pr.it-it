---
description: Il metodo SetSmartRecompressFormat specifica un formato di compressione video da usare per la ricompressione intelligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'Metodo IAMTimelineGroup:: SetSmartRecompressFormat (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331622"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a>Metodo IAMTimelineGroup:: SetSmartRecompressFormat

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetSmartRecompressFormat` metodo specifica un formato di compressione video da usare per la ricompressione intelligente.

La ricompressione intelligente non è supportata per i gruppi audio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a una struttura che descrive il formato di compressione. Attualmente, solo la struttura [**SCompFmt0**](scompfmt0.md) è valida. È necessario eseguire il cast di questo parametro a un puntatore di tipo **Long**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare il metodo [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) sullo stesso gruppo, per specificare un formato non compresso.

Se il `SetSmartRecompressFormat` metodo ha esito positivo, è possibile usare il motore di rendering intelligente per generare un flusso video compresso. Il video compresso avrà la larghezza, l'altezza e la frequenza dei fotogrammi specificati nel parametro *pFormat* . Questi valori eseguiranno l'override di quelli specificati per il formato non compresso nel metodo **SetMediaType** . Tuttavia, per sfruttare i vantaggi della ricompressione intelligente, i due formati devono corrispondere. In altre parole, i formati compressi e non compressi dovrebbero avere la stessa altezza, larghezza e frequenza dei fotogrammi.

Se il motore di rendering intelligente non riesce a produrre il formato compresso, produrrà invece un flusso video non compresso. In tal caso, il motore di rendering intelligente segnala un \_ \_ errore di \_ rendering del compressore di ID Dex \_ durante il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) . L'applicazione può rilevare questo errore tramite il metodo [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) . Per ulteriori informazioni, vedere [registrazione degli errori](logging-errors.md) e [rendering degli errori](rendering-errors.md).

Il formato di ricompressione intelligente non è permanente. Se in un'applicazione viene utilizzata la ricompressione intelligente, è necessario impostare il formato di ricompressione ogni volta che viene caricato un file di progetto.

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
</dt> <dt>

[Motore di rendering intelligente](smart-render-engine.md)
</dt> <dt>

[Scrittura di un progetto in un file](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




