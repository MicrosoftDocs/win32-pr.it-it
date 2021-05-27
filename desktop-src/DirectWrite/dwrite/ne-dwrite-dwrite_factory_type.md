---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Specifica il tipo di oggetto factory DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 51cfbb274d681bb35b806f49aef13cc4a220ee26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550306"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>DWRITE_FACTORY_TYPE enumerazione (dwrite.h)

Specifica il tipo di oggetto factory DirectWrite.

> [!IMPORTANT]
> Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md) DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme. Per altre informazioni ed esempi di codice, vedi [Panoramica di DWriteCore.](../dwritecore-overview.md)

## <a name="syntax"></a>Sintassi
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a>Costanti

| Nome | Descrizione |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Indica che la factory DirectWrite è una factory condivisa e che consente il riutilizzo dei dati dei tipi di carattere memorizzati nella cache tra più componenti in-process. Tali factory sfruttano anche i componenti di memorizzazione nella cache dei tipi di carattere tra processi per ottenere prestazioni migliori. |
| DWRITE_FACTORY_TYPE_ISOLATED | Indica che l'oggetto factory DirectWrite è isolato. Gli oggetti creati dalla factory isolata non interagiscono con lo stato DirectWrite interno da altri componenti. |
| DWRITE_FACTORY_TYPE_ISOLATED2 | Indica che l'oggetto factory DirectWrite è limitato. Gli oggetti creati da una factory con restrizioni non usano né modificano lo stato interno o i dati memorizzati nella cache usati da altre factory. Inoltre, la raccolta di tipi di carattere di sistema contiene solo tipi di carattere noti.|

## <a name="examples"></a>Esempio

Vedere [l'argomento di panoramica DWriteCore](../dwritecore-overview.md) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="remarks"></a>Commenti

Un oggetto factory DirectWrite contiene informazioni sullo stato interno, ad esempio la registrazione del caricatore dei tipi di carattere e i dati dei tipi di carattere memorizzati nella cache. Nella maggior parte dei casi è consigliabile usare l'oggetto factory condiviso, perché consente a più componenti che usano DirectWrite di condividere informazioni interne sullo stato DirectWrite, riducendo così l'utilizzo della memoria. In alcuni casi, tuttavia, è preferibile ridurre l'impatto di un componente sul resto del processo, ad esempio un plug-in da un'origine non attendibile, tramite sandboxing e isolamento dal resto dei componenti del processo. In questi casi, è consigliabile usare una factory isolata per il componente sandbox.

Una factory con restrizioni è più bloccata rispetto a una factory isolata. Non interagisce in alcun modo con una cache dei tipi di carattere tra processi o persistenti. Inoltre, la raccolta di tipi di carattere di sistema restituita da questa factory include solo tipi di carattere noti. Se si passa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versione di DWrite precedente a DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) restituisce **E_INVALIDARG**.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10, Project Dispositivi [app Win32] |
| **Intestazione** | dwrite.h (includere dwrite_core.h) |