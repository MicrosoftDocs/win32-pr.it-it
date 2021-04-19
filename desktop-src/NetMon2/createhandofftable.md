---
description: La funzione CreateHandoffTable crea una tabella che include le informazioni sul set di continuità archiviate nel file INI del parser.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Funzione CreateHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311629"
---
# <a name="createhandofftable-function"></a>CreateHandoffTable (funzione)

La funzione **CreateHandoffTable** crea una [*tabella*](h.md) che include le informazioni sul set di continuità archiviate nel file ini del parser.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Secname* \[ in\]
</dt> <dd>

Stringa che indica la sezione del file INI in cui si trovano le informazioni sul set di continuità.

</dd> <dt>

*iniFile* \[ in\]
</dt> <dd>

Stringa che include il nome del file INI del parser.

</dd> <dt>

*hTable* \[ out\]
</dt> <dd>

Handle per una struttura **HANDOFFTABLE** creata e gestita da Network Monitor.

</dd> <dt>

*nMaxProtocolEntries* \[ in\]
</dt> <dd>

Numero che specifica il numero massimo di voci che possono essere elaborate dalla tabella di continuità.

</dd> <dt>

di *base* \[ in\]
</dt> <dd>

Base numerica dei numeri di set di continuità archiviati nel file INI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è il numero di voci nella tabella con continuità.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

La tabella uniforme creata da Network Monitor si basa sulle informazioni fornite nell'INI del parser. Per ottenere un handle per uno dei protocolli inclusi nella tabella, è quindi possibile usare l'handle restituito alla tabella di continuità. Per ottenere un handle di uno di questi protocolli, chiamare [GetProtocolFromTable](getprotocolfromtable.md).

Si noti che l'applicazione del parser non accede mai direttamente alla struttura **HANDOFFTABLE** . Questa struttura viene creata e gestita da Network Monitor.

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

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




