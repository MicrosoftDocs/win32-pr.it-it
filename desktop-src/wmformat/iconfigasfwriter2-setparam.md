---
title: IConfigAsfWriter2 (metodo separat)
description: Il metodo separat imposta il valore del parametro di configurazione del filtro specificato.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Metodo separat Windows Media Format
- Metodo Separator formato Windows Media, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo separat
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300112"
---
# <a name="iconfigasfwriter2setparam-method"></a>Metodo IConfigAsfWriter2:: separat

Il metodo **separat** imposta il valore del parametro di configurazione del filtro specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* \[ in\]
</dt> <dd>

Specifica il parametro da impostare. Deve essere un valore definito nell'enumerazione [ \_ \_ \_ param ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*dwParam1* \[ in\]
</dt> <dd>

Specifica il valore da assegnare al parametro *dwParam* .

</dd> <dt>

*dwParam2* \[ in\]
</dt> <dd>

Non utilizzato; deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 