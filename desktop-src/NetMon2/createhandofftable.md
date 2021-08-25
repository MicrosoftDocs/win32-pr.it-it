---
description: La funzione CreateHandoffTable crea una tabella handoff che include le informazioni sul set di handoff archiviate nel file INI del parser.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Funzione CreateHandoffTable (Netmon.h)
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
ms.openlocfilehash: 70709223d5dcebcae819389feb8623006b793126a911fc674491b1d665268056
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911201"
---
# <a name="createhandofftable-function"></a>Funzione CreateHandoffTable

La **funzione CreateHandoffTable** crea una [*tabella handoff*](h.md) che include le informazioni sul set di handoff archiviate nel file INI del parser.

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

*secName* \[ Pollici\]
</dt> <dd>

Stringa che indica la sezione del file INI in cui si trovano le informazioni sul set di handoff.

</dd> <dt>

*iniFile* \[ Pollici\]
</dt> <dd>

Stringa che include il nome del file INI del parser.

</dd> <dt>

*hTable* \[ Cambio\]
</dt> <dd>

Handle a una **struttura HANDOFFTABLE** creata e gestita da Network Monitor.

</dd> <dt>

*nMaxProtocolEntries* \[ Pollici\]
</dt> <dd>

Numero che specifica il numero massimo di voci che la tabella handoff può elaborare.

</dd> <dt>

*base* \[ Pollici\]
</dt> <dd>

Base numerica dei numeri dei set di handoff archiviati nel file INI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è il numero di voci nella tabella handoff.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

La tabella handoff creata da Network Monitor si basa sulle informazioni fornite nell'INI del parser. L'handle restituito alla tabella handoff può quindi essere usato per ottenere un handle per uno dei protocolli inclusi nella tabella. Per ottenere un handle di uno di questi protocolli, chiamare [GetProtocolFromTable](getprotocolfromtable.md).

Si noti che l'applicazione parser non accede mai direttamente alla **struttura HANDOFFTABLE.** Questa struttura viene creata e gestita da Network Monitor.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




