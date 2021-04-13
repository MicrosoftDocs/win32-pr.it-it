---
title: Metodo IConfigAsfWriter2 ResetMultiPassState
description: Il metodo ResetMultiPassState Reimposta il filtro quando viene annullato un passaggio di codifica per la pre-elaborazione prima del completamento.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Metodo ResetMultiPassState Windows Media Format
- Metodo ResetMultiPassState Windows Media Format, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399513"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>Metodo IConfigAsfWriter2:: ResetMultiPassState

Il metodo **ResetMultiPassState** Reimposta il filtro quando viene annullato un passaggio di codifica per la pre-elaborazione prima del completamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Il metodo è riuscito.<br/>                  |
| <dl> <dt>**VFW \_ E \_ non \_ arrestato**</dt> </dl> | Il filtro non si trova in uno stato interrotto.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato per reimpostare lo stato interno del filtro ogni volta che viene annullato un passaggio di codifica per la pre-elaborazione prima che il filtro riceva un evento di **\_ \_ completamento della pre-elaborazione EC** . Non è necessario chiamare questo metodo se il passaggio di codifica per la pre-elaborazione viene completato senza errori.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

