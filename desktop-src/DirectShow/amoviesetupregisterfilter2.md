---
description: La funzione AMovieSetupRegisterFilter2 registra il merito, i pin e i tipi di supporto del filtro nel registro di sistema tramite l'interfaccia IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Funzione AMovieSetupRegisterFilter2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331706"
---
# <a name="amoviesetupregisterfilter2-function"></a>AMovieSetupRegisterFilter2 (funzione)

La funzione **AMovieSetupRegisterFilter2** registra il merito, i pin e i tipi di supporto del filtro nel registro di sistema tramite l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*psetupdata* 
</dt> <dd>

Puntatore ai dati [**del \_ filtro AMOVIESETUP**](amoviesetup-filter.md) .

</dd> <dt>

*pIFM2* 
</dt> <dd>

Puntatore all'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

</dd> <dt>

*bRegister* 
</dt> <dd>

Valore che indica se registrare il filtro. **True** indica che registra il filtro, **false** indica che è stata annullata la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

La funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) chiama questa funzione helper per registrare un filtro dopo la registrazione del server com.

In genere, un filtro userà [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) e non chiamerà direttamente questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dllsetup. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di installazione DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




