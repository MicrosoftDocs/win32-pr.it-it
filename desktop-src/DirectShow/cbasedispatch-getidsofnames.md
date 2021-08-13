---
description: 'Metodo CBaseDispatch.GetIDsOfNames: il metodo GetIDsOfNames esegue il mapping di un set di nomi a un set corrispondente di DISPID.'
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Metodo CBaseDispatch.GetIDsOfNames (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9153dd2412018321374f558539690d5d146d8547d6247874bf5c1c79f1d4d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660028"
---
# <a name="cbasedispatchgetidsofnames-method"></a>Metodo CBaseDispatch.GetIDsOfNames

Il `GetIDsOfNames` metodo esegue il mapping di un set di nomi a un set corrispondente di DISPID.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Riid* 
</dt> <dd>

Riferimento a un identificatore di interfaccia (IID) che specifica l'interfaccia.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Indirizzo di una matrice di stringhe di caratteri wide che contengono i nomi di cui eseguire il mapping.

</dd> <dt>

*cNames* 
</dt> <dd>

Dimensione della matrice specificata dal *parametro rgszNames.*

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare i nomi. Può essere **NULL.**

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntatore a una matrice che riceve i DISPID. Ogni elemento di riceve un identificatore che corrisponde a uno dei nomi passati nel *parametro rgszNames.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                         | Descrizione                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione completata.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Memoria insufficiente.<br/>                     |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl> | Uno o più nomi non erano noti.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo si comporta come **il metodo IDispatch::GetIDsOfNames,** ma il *parametro riid* specifica l'interfaccia in cui recuperare i DISPID. Nella versione **IDispatch** il *parametro riid* è riservato.

Se il metodo restituisce DISP E UNKNOWNNAME, i DISPID restituiti contengono DISPID UNKNOWN per ogni voce \_ che corrisponde a un nome \_ \_ sconosciuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




