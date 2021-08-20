---
UID: ''
title: Funzione InterlockedPushListSList
description: Inserisce un elenco collegato in modo indocino all'inizio di un altro elenco collegato.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: f2a13003b1b850431bac87a2ca02bbf093bc67dc9207e317b2c602bde83e15b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959238"
---
# <a name="interlockedpushlistslist-function"></a>Funzione InterlockedPushListSList

## <a name="description"></a>Descrizione

Inserisce un elenco collegato in modo indocino all'inizio di un altro elenco collegato.
L'accesso agli elenchi è sincronizzato in un sistema multiprocessore.

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a>Parametri

### <a name="listhead-in-out"></a>ListHead [in, out]

Puntatore a **SLIST_HEADER** struttura che rappresenta l'inizio di un elenco collegato.
L'elenco specificato dai *parametri List* e *ListEnd* viene inserito all'inizio dell'elenco.

### <a name="list-in-out"></a>List [in, out]

Puntatore a [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) struttura che rappresenta il primo elemento dell'elenco da inserire.

### <a name="listend-in-out"></a>ListEnd [in, out]

Puntatore a [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) struttura che rappresenta l'ultimo elemento dell'elenco da inserire.

### <a name="count-in"></a>Conteggio [in]

Numero di elementi nell'elenco da inserire.

## <a name="returns"></a>Restituisce

Il valore restituito è il primo elemento precedente nell'elenco specificato dal *parametro ListHead.*
Se in precedenza l'elenco era vuoto, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Tutti gli elementi dell'elenco devono essere allineati in **MEMORY_ALLOCATION_ALIGNMENT** limite; In caso contrario, questa funzione si comporterà in modo imprevedibile.
Vedere **_aligned_malloc**.

**Windows 8 e Windows Server 2012:**  Questa funzione è stata sostituita da [InterlockedPushListSListEx.](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
Durante la compilazione con **NTDDI_VERSION** impostato su **NTDDI_WIN8** o superiore, le chiamate a **InterlockedPushListSList** andranno invece a **InterlockedPushListSListEx.**

## <a name="see-also"></a>Vedi anche

[Elenchi collegati in modo singly interlocked](/windows/desktop/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[InterlockedPushEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[InterlockedFlushSList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Uso di elenchi collegati in modo inevaso](/windows/desktop/Sync/using-singly-linked-lists)
