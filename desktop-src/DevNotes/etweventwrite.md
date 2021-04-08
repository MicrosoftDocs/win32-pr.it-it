---
description: 'Altre informazioni su: funzione EtwEventWrite'
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
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049236"
---
# <a name="etweventwrite-function"></a>EtwEventWrite (funzione)

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

*EventDescriptor*
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

La funzione EtwEventWrite e le strutture restituite sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows a un'altra. Per mantenere la compatibilità dell'applicazione, è preferibile usare invece le funzioni pubbliche.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | ntetw. h |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
