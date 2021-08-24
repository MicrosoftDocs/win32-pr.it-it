---
description: Scrive un evento completo in una sessione.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 1fd25931e6a58b97e052ecd7da43bd651688d2bf726d8b5ba2acd84ce820be7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653430"
---
# <a name="etweventwritefull-function"></a>Funzione EtwEventWriteFull

[La funzione EtwEventWriteFull e le strutture restituite sono interne al sistema operativo e soggette a modifiche da una versione di Windows a un'altra.]

Scrive un evento completo in una sessione.

## <a name="syntax"></a>Sintassi

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
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

*EventProperty*
</dt> <dd>

Flag fornito dall'utente.

</dd> <dt>

*ActivityId*
</dt> <dd>

ID attività.

</dd> <dt>

*RelatedActivityId*
</dt> <dd>

ID attività correlata.

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

La funzione EtwEventWriteFull e le strutture restituite sono interne al sistema operativo e soggette a modifiche da una versione di Windows a un'altra. Per mantenere la compatibilità dell'applicazione, è meglio usare le funzioni pubbliche.


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
