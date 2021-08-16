---
title: Metodo SetParam IConfigAsfWriter2
description: Il metodo SetParam imposta il valore del parametro di configurazione del filtro specificato.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Metodo SetParam windows Media Format
- Metodo SetParam windows Media Format , interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2 windows Media Format , metodo SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e7c73831ec45e6e0b65444e93e976fe349a2d4576d578f3399c60c399628cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847499"
---
# <a name="iconfigasfwriter2setparam-method"></a>Metodo IConfigAsfWriter2::SetParam

Il **metodo SetParam** imposta il valore del parametro di configurazione del filtro specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* \[ Pollici\]
</dt> <dd>

Specifica il parametro da impostare. Deve essere un valore definito [ \_ nell'enumerazione AM \_ ASFWRITERCONFIG \_ PARAM.](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))

</dd> <dt>

*dwParam1* \[ Pollici\]
</dt> <dd>

Specifica il valore da assegnare al *parametro dwParam.*

</dd> <dt>

*dwParam2* \[ Pollici\]
</dt> <dd>

Non usato; deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se non riesce, restituisce un **codice di errore HRESULT.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 