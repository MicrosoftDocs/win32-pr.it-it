---
description: La funzione GetProtocolFromTable restituisce un handle a un protocollo&\# 8212; in base a una tabella e a un valore di continuità specificati.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Funzione GetProtocolFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966461"
---
# <a name="getprotocolfromtable-function"></a>GetProtocolFromTable (funzione)

La funzione **GetProtocolFromTable** restituisce un handle a un protocollo basato su una tabella e un valore di continuità specificati.

## <a name="syntax"></a>Sintassi


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hTable* \[ in\]
</dt> <dd>

Handle per una tabella con continuità.

</dd> <dt>

*ItemToFind* \[ in\]
</dt> <dd>

Valore utilizzato per individuare il protocollo in una tabella con continuità. Il valore deve essere disponibile nei dati del protocollo.

</dd> <dt>

*lpInstData* \[ out\]
</dt> <dd>

Se disponibile nella tabella uniforme, i dati dell'istanza per il protocollo successivo. I dati dell'istanza non possono essere più lunghi di un \_ ptr DWORD di lunghezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle del protocollo.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Quando si implementa la funzione di esportazione [RecognizeFrame](recognizeframe.md) , viene utilizzata la funzione **GetProtocolFromTable** per ottenere un handle per il protocollo successivo. La funzione **GetProtocolFromTable** viene chiamata per recuperare un handle dal protocollo successivo se il protocollo identifica il protocollo che segue.

**Dati dell'istanza**

I dati dell'istanza possono essere dati di lunghezza minore o uguale a un \_ ptr DWORD o un puntatore ai dati, ad esempio dati di frame non elaborati, che non devono essere allocati o liberati dal parser.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




