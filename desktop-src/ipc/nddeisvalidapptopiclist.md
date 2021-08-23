---
description: Determina se un'applicazione e una stringa di argomento (&\# 0034; AppName \| TopicName&\# 0034;) usa la sintassi corretta.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Funzione NDdeIsValidAppTopicList (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: f7b70d3e33f67c8c0a457f85df91e83e374a3ef4d0f0b1a0af1c5c41ea81c2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611131"
---
# <a name="nddeisvalidapptopiclist-function"></a>Funzione NDdeIsValidAppTopicList

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Determina se un'applicazione e una stringa di argomento ("*AppName* \| *TopicName*") utilizzano la sintassi corretta.

## <a name="syntax"></a>Sintassi


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*targetTopic* \[ Pollici\]
</dt> <dd>

Puntatore all'applicazione e alla stringa dell'argomento da convalidare. Questo parametro non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il *parametro targetTopic* ha una sintassi valida, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Questa funzione viene chiamata anche da [**NDdeShareAdd**](nddeshareadd.md) quando crea la condivisione DDE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>      |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Nomi Unicode e ANSI<br/>   | **NDdeIsValidAppTopicListW** (Unicode) e **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica delle Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




