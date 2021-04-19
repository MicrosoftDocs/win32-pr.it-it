---
description: Determina se una stringa di applicazione e argomento (&\# 0034; AppName \| topicname&\# 0034;) Usa la sintassi corretta.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Funzione NDdeIsValidAppTopicList (nddeapi. h)
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
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317316"
---
# <a name="nddeisvalidapptopiclist-function"></a>NDdeIsValidAppTopicList (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Determina se un'applicazione e una stringa di argomento ("*appname* \| *topicName*") utilizzano la sintassi corretta.

## <a name="syntax"></a>Sintassi


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*targetTopic* \[ in\]
</dt> <dd>

Puntatore alla stringa dell'applicazione e dell'argomento da convalidare. Questo parametro non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il parametro *targetTopic* ha una sintassi valida, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Questa funzione viene chiamata anche da [**NDDEShareAdd**](nddeshareadd.md) quando crea la condivisione DDE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>      |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Nomi Unicode e ANSI<br/>   | **NDdeIsValidAppTopicListW** (Unicode) e **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




