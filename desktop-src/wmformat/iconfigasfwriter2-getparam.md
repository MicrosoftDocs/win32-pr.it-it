---
title: Metodo GetParam IConfigAsfWriter2
description: Il metodo GetParam recupera il valore corrente del parametro di configurazione del filtro specificato.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Metodo GetParam windows Media Format
- Metodo GetParam windows Media Format , interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2 windows Media Format , metodo GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a411e4b1896174e25a1f671f3f42fd83c1376713f10e9e4cb2b2d2186b3d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809141"
---
# <a name="iconfigasfwriter2getparam-method"></a>Metodo IConfigAsfWriter2::GetParam

Il **metodo GetParam** recupera il valore corrente del parametro di configurazione del filtro specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* \[ Pollici\]
</dt> <dd>

Specifica il parametro da recuperare. Deve essere un valore definito [ \_ nell'enumerazione AM \_ ASFWRITERCONFIG \_ PARAM.](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))

</dd> <dt>

*pdwParam1* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che recupera il valore del parametro specificato in *dwParam*.

</dd> <dt>

*pdwParam2* \[ Cambio\]
</dt> <dd>

Non usato, deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se non riesce, restituisce un **codice di errore HRESULT.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 