---
description: Il metodo SpliceWithNext unisce l'oggetto di origine a un altro oggetto di origine.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: Metodo IAMTimelineSrc::SpliceWithNext (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ffde9c7bb0416f2b296f7a7c347a058734430be33ef4ecde59e7e39cd6e845f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154832"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>Metodo IAMTimelineSrc::SpliceWithNext

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SpliceWithNext` metodo unisce l'oggetto di origine a un altro oggetto di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNext* 
</dt> <dd>

Puntatore [**all'interfaccia IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine da unire all'origine corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori restituiti possibili sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argomento non valido.<br/>                                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | L'oggetto specificato *dal parametro pNext* non è un oggetto di origine.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Argomento del puntatore **NULL.**<br/>                                    |



 

## <a name="remarks"></a>Commenti

Come attualmente implementato, questo metodo elimina tutti gli effetti su *pNext.*

Perché questo metodo riesca, *pNext* deve essere un frame di corrispondenza dell'oggetto di origine corrente, definito come segue:

-   Deve condividere lo stesso file di origine.
-   L'ora di inizio del supporto deve corrispondere all'ora di arresto del supporto dell'origine corrente.
-   La velocità di riproduzione deve essere la stessa. La frequenza di riproduzione è la durata dei file multimediali divisa per la durata della sequenza temporale.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




