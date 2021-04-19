---
description: Il metodo SetMediaTimes imposta l'ora di inizio e di fine del supporto.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'Metodo IAMTimelineSrc:: SetMediaTimes (qedit. h)'
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
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330179"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>Metodo IAMTimelineSrc:: SetMediaTimes

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetMediaTimes` metodo imposta l'ora di inizio e di fine del supporto.

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

Ora di inizio del supporto, in unità di 100 nanosecondi.

</dd> <dt>

*Stop* 
</dt> <dd>

Tempo di arresto del supporto, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

I tempi di supporto sono l'ora di arresto e di inizio rispetto al file multimediale originale. Impostare sempre i tempi dei supporti quando si aggiunge un'origine video o audio alla sequenza temporale. In caso contrario, potrebbero verificarsi problemi di rendering. L'ora di arresto deve essere successiva all'ora di inizio.

Per usare un frame ancora da un'origine video, impostare l'ora di arresto su un importo frazionario superiore all'ora di inizio, ad esempio 100 nanosecondi. Se vengono impostate sullo stesso valore, viene generato un errore di rendering.

Se la durata della sequenza temporale non corrisponde alla durata del supporto, l'origine si estende o compatta di conseguenza. In questo modo il clip riproduca più lentamente o più velocemente rispetto alla velocità creata. (Lo spostamento del pitch si verificherà in un'origine audio.) Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).

È possibile specificare la durata del file di origine chiamando il metodo [**SetMediaLength**](iamtimelinesrc-setmedialength.md) . Se si imposta un'ora di arresto del supporto che supera la durata, DES tronca l'ora di arresto.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




