---
description: Il metodo GetNextTrans recupera la prima transizione visualizzata all'ora specificata o successiva.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: Metodo IAMTimelineTransable::GetNextTrans (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 892f8e0f4af39250d62da9ed662c22867f98ebfc32baeaa0f341ead2eef665a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131081"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>Metodo IAMTimelineTransable::GetNextTrans

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetNextTrans` metodo recupera la prima transizione visualizzata all'ora specificata o successiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppTrans* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di transizione.

</dd> <dt>

*Pinout* 
</dt> <dd>

Puntatore a una variabile che specifica il tempo in unità di 100 nanosecondi. In input, questo valore specifica l'ora da cui trovare la transizione. Nell'output, se viene recuperata una transizione, questo valore viene impostato sull'ora di arresto della transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il metodo recupera una transizione oppure S FALSE se non trova una \_ transizione. In caso contrario, restituisce **un valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

L'ora di inizio della transizione potrebbe essere minore dell'ora specificata in *pInOut*, se la transizione si estende sull'ora specificata.

Se il metodo restituisce S \_ OK, [**l'interfaccia IAMTimelineObj**](iamtimelineobj.md) restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

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

[**Interfaccia IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




