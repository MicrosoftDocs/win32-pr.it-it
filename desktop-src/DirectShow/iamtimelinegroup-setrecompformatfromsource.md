---
description: Il metodo SetRecompFormatFromSource imposta il formato di ricompressione video usando il formato di compressione da un file di origine.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Metodo IAMTimelineGroup:: SetRecompFormatFromSource (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331623"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>Metodo IAMTimelineGroup:: SetRecompFormatFromSource

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetRecompFormatFromSource` metodo imposta il formato di ricompressione video usando il formato di compressione da un file di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSource* 
</dt> <dd>

Puntatore all'interfaccia [**IAMTimelineSrc**](iamtimelinesrc.md) dell'oggetto di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce valori **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                             | Descrizione                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                                                                                    |
| <dl> <dt>**E \_ Nessuna \_ sequenza temporale**</dt> </dl>          | Il gruppo non si trova all'interno di una sequenza temporale.<br/>                                                         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>           | Memoria insufficiente.<br/>                                                                        |
| <dl> <dt>**\_puntatore E**</dt> </dl>               | Argomento puntatore **null** .<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido. Il gruppo non è un gruppo video oppure il file di origine non contiene alcun flusso video.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo trova il file di origine associato a *pSource*, recupera il tipo di supporto del primo flusso video nel file e imposta il formato di compressione del gruppo che utilizza tale tipo. Per ulteriori informazioni sui formati di compressione, vedere [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).

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

 

 




