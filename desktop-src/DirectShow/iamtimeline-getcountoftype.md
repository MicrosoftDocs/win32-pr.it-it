---
description: Il metodo GetCountOfType recupera il numero di oggetti del tipo specificato contenuti in un gruppo specificato e in tutti i relativi elementi figlio.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: Metodo IAMTimeline::GetCountOfType (Qedit.h)
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
ms.openlocfilehash: 8e9eb896f00752c5d9369cf494e7b1426347f82a7ebe2aac74f7822a936c2ffb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401062"
---
# <a name="iamtimelinegetcountoftype-method"></a>Metodo IAMTimeline::GetCountOfType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo recupera il numero di oggetti del tipo specificato contenuti `GetCountOfType` in un gruppo specificato e in tutti i relativi elementi figlio.

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

*Pval* 
</dt> <dd>

Riceve il numero di oggetti del tipo specificato contenuti nel gruppo e in tutte le relative tracce virtuali, in modo ricorsivo.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Riceve il conteggio restituito in *pVal* più il numero di composizioni ricercate, inclusa questa.

</dd> <dt>

*MajorType* 
</dt> <dd>

Membro del tipo [**enumerato TIMELINE \_ MAJOR \_ TYPE,**](timeline-major-type.md) che specifica il tipo di oggetto da contare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                  | Descrizione                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Numero di gruppo non valido.<br/>      |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | Argomento del puntatore **NULL.**<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo equivale a chiamare [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) nel gruppo specificato. Per altre informazioni, vedere la sezione Osservazioni di tale metodo.

In genere, un'applicazione non chiamerà questo metodo. Viene chiamato internamente dal motore di rendering.

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

 

 




