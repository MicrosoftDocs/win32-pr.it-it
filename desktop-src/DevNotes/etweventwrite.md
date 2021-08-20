---
description: Altre informazioni sulla funzione EtwEventWrite
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: b8e06c2a0922038e37766f44c0b9fcd7c85bbb7fd4fa4bd0841192be9e4e9087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162102"
---
# <a name="etweventwrite-function"></a>Funzione EtwEventWrite

[La funzione EtwEventWrite e le strutture restituite sono interne al sistema operativo e soggette a modifiche da una versione di Windows a un'altra.]

Scrive un evento di base in una sessione.

## <a name="syntax"></a>Sintassi

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*RegHandle*
</dt> <dd>

RegHandle per il provider.

</dd> <dt>

*Eventdescriptor*
</dt> <dd>

Descrittore dell'evento da registrare.

</dd> <dt>

*UserDataCount*
</dt> <dd>

Numero di elementi di dati utente.

</dd> <dt>

*UserData*
</dt> <dd>

Puntatore a una matrice di elementi di dati utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Codice di errore Win32.


## <a name="remarks"></a>Commenti

La funzione EtwEventWrite e le strutture restituite sono interne al sistema operativo e soggette a modifiche da una versione di Windows a un'altra. Per mantenere la compatibilità dell'applicazione, è invece meglio usare le funzioni pubbliche.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | ntetw.h |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
