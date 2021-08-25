---
title: Metodo IConfigAsfWriter2 ResetMultiPassState
description: Il metodo ResetMultiPassState reimposta il filtro quando un passaggio di codifica di pre-elaborazione viene annullato prima del completamento.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Metodo ResetMultiPassState windows Media Format
- Metodo ResetMultiPassState windows Media Format , interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2 formato multimediale windows, metodo ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f10563ed716b6b33258fe57ff8129bff78b401170db1512566015d0b05d54dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839871"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>Metodo IConfigAsfWriter2::ResetMultiPassState

Il **metodo ResetMultiPassState** reimposta il filtro quando un passaggio di codifica di pre-elaborazione viene annullato prima del completamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Il metodo è riuscito.<br/>                  |
| <dl> <dt>**VFW \_ E \_ NON \_ ARRESTATO**</dt> </dl> | Il filtro non era in stato arrestato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato per reimpostare lo stato interno del filtro ogni volta che un passaggio di codifica di pre-elaborazione viene annullato prima che il filtro abbia ricevuto un evento **EC \_ PREPROCESS \_ COMPLETE.** Non è necessario chiamare questo metodo se il passaggio di codifica di pre-elaborazione viene completato senza errori.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

