---
description: Il metodo SetMediaTimes imposta le ore di arresto e avvio dei supporti.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: Metodo IAMTimelineSrc::SetMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5de058e31da605b96f7b013c03e9c0d020daa11ec676618b4a13f5ff92e701f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154927"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>Metodo IAMTimelineSrc::SetMediaTimes

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SetMediaTimes` metodo imposta le ore di arresto e avvio del supporto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Inizia* 
</dt> <dd>

Ora di inizio del supporto, in unità da 100 nanosecondi.

</dd> <dt>

*Stop* 
</dt> <dd>

Tempo di arresto dei supporti, in unità da 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Gli orari dei supporti sono gli orari di arresto e avvio relativi al file multimediale originale. Impostare sempre gli orari dei contenuti multimediali quando si aggiunge un'origine video o audio alla sequenza temporale. In caso contrario, potrebbero verificarsi problemi di rendering. L'ora di arresto deve essere maggiore dell'ora di inizio.

Per usare un fotogramma fermo da un'origine video, impostare l'ora di arresto su una quantità frazionaria superiore all'ora di inizio, ad esempio 100 nanosecondi. Impostandoli sullo stesso valore si verifica un errore di rendering.

Se la durata della sequenza temporale non corrisponde alla durata del supporto, l'origine si estende o si riduce di conseguenza. In questo modo la riproduzione del clip è più lenta o più veloce rispetto alla frequenza di creazione. Lo spostamento del passo si verificherà in un'origine audio. Per altre informazioni, vedere [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

È possibile specificare la durata del file di origine chiamando il [**metodo SetMediaLength.**](iamtimelinesrc-setmedialength.md) Se si imposta un tempo di arresto multimediale che supera la durata, DES tronca l'ora di arresto.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




