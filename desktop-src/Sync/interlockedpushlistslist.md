---
UID: ''
title: Funzione InterlockedPushListSList
description: Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente.
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
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2020
ms.locfileid: "104398779"
---
# <a name="interlockedpushlistslist-function"></a>Funzione InterlockedPushListSList

## <a name="description"></a>Descrizione

Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente.
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

Puntatore a una struttura **SLIST_HEADER** che rappresenta l'intestazione di un elenco collegato singolarmente.
L'elenco specificato dall'elenco *e dai* parametri di *ascolto* viene inserito all'inizio dell'elenco.

### <a name="list-in-out"></a>Elenco [in, out]

Puntatore a una struttura [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) che rappresenta il primo elemento dell'elenco da inserire.

### <a name="listend-in-out"></a>In ascolto [in, out]

Puntatore a una struttura [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) che rappresenta l'ultimo elemento dell'elenco da inserire.

### <a name="count-in"></a>Count [in]

Numero di elementi nell'elenco da inserire.

## <a name="returns"></a>Restituisce

Il valore restituito è il primo elemento precedente nell'elenco specificato dal parametro *listhead* .
Se l'elenco è stato precedentemente vuoto, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Tutti gli elementi dell'elenco devono essere allineati su un limite di **MEMORY_ALLOCATION_ALIGNMENT** ; in caso contrario, questa funzione si comporterà in modo imprevedibile.
Vedere **_aligned_malloc**.

**Windows 8 e Windows Server 2012:**  Questa funzione è stata sostituita da [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).
Quando si esegue la compilazione con **NTDDI_VERSION** impostato su **NTDDI_WIN8** o versione successiva, le chiamate a **InterlockedPushListSList** andranno invece a **InterlockedPushListSListEx** .

## <a name="see-also"></a>Vedi anche

[Elenchi collegati singolarmente con Interlocking](/windows/desktop/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[InterlockedPushEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[InterlockedFlushSList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Uso di elenchi collegati singolarmente](/windows/desktop/Sync/using-singly-linked-lists)
