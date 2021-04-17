---
title: Metodo getparat IConfigAsfWriter2
description: Il metodo getparat Recupera il valore corrente del parametro di configurazione del filtro specificato.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Metodo getparat Windows Media Format
- Metodo getparat Windows Media Format, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo getparat
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300256"
---
# <a name="iconfigasfwriter2getparam-method"></a>Metodo IConfigAsfWriter2:: getparat

Il metodo **Getparat** Recupera il valore corrente del parametro di configurazione del filtro specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* \[ in\]
</dt> <dd>

Specifica il parametro da recuperare. Deve essere un valore definito nell'enumerazione [ \_ \_ \_ param ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*pdwParam1* \[ out\]
</dt> <dd>

Puntatore a una variabile che recupera il valore del parametro specificato in *dwParam*.

</dd> <dt>

*pdwParam2* \[ out\]
</dt> <dd>

Non utilizzato, deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: separat**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 