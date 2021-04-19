---
description: Il metodo GetCountOfType Recupera il numero di oggetti del tipo specificato contenuti in un gruppo specificato e in tutti i relativi elementi figlio.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'Metodo IAMTimeline:: GetCountOfType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326796"
---
# <a name="iamtimelinegetcountoftype-method"></a>Metodo IAMTimeline:: GetCountOfType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetCountOfType` metodo recupera il numero di oggetti del tipo specificato contenuti in un gruppo specificato e in tutti i relativi elementi figlio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gruppo* 
</dt> <dd>

Numero di indice del gruppo per il quale recuperare il conteggio.

</dd> <dt>

*pVal* 
</dt> <dd>

Riceve il numero di oggetti del tipo specificato contenuti nel gruppo e in tutte le relative tracce virtuali, in modo ricorsivo.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Riceve il conteggio restituito in *pval* più il numero di composizioni ricercate, incluso quello.

</dd> <dt>

*MajorType* 
</dt> <dd>

Membro del tipo enumerato della [**sequenza temporale \_ principale \_**](timeline-major-type.md) , che specifica il tipo di oggetto da contare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                  | Descrizione                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Numero di gruppo non valido.<br/>      |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/> |



 

## <a name="remarks"></a>Commenti

La chiamata a questo metodo equivale alla chiamata di [**IAMTimelineComp:: GetCountOfType**](iamtimelinecomp-getcountoftype.md) nel gruppo specificato. Per ulteriori informazioni, vedere la sezione Osservazioni di tale metodo.

In genere, un'applicazione non chiamerà questo metodo. Viene chiamato internamente dal motore di rendering.

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

 

 




