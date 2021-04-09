---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (DWrite. h)
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
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2020
ms.locfileid: "104047784"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>Enumerazione DWRITE_FACTORY_TYPE (DWrite. h)

Specifica il tipo di oggetto factory DirectWrite.

> [!IMPORTANT]
> Questa API è disponibile come parte dell'implementazione di DWriteCore di [DirectWrite](../direct-write-portal.md). DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme. Per altre informazioni ed esempi di codice, vedere [Panoramica di DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Sintassi
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a>Costanti

| Nome | Descrizione |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Indica che la factory DirectWrite è una factory condivisa e che consente il riutilizzo dei dati del tipo di carattere memorizzati nella cache tra più componenti in-process. Tali Factory sfruttano inoltre i componenti di caching dei tipi di carattere tra processi per ottenere prestazioni migliori. |
| DWRITE_FACTORY_TYPE_ISOLATED | Indica che l'oggetto factory DirectWrite è isolato. Gli oggetti creati dalla factory isolata non interagiscono con lo stato DirectWrite interno da altri componenti. |
| DWRITE_FACTORY_TYPE_RESTRICTED | Gli oggetti creati da una factory con restrizioni non usano né modificano lo stato interno o i dati memorizzati nella cache usati da altre Factory. Inoltre, la raccolta di tipi di carattere del sistema contiene solo tipi di carattere noti.|

## <a name="examples"></a>Esempio

Vedere l'argomento [Panoramica di DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Commenti

Un oggetto factory DirectWrite contiene informazioni sullo stato interno, ad esempio la registrazione del caricatore del tipo di carattere e i dati del tipo di carattere memorizzati nella cache. Nella maggior parte dei casi è consigliabile usare l'oggetto Factory condiviso, perché consente a più componenti che usano DirectWrite di condividere informazioni sullo stato DirectWrite interno, riducendo così l'utilizzo della memoria. Tuttavia, esistono casi in cui è consigliabile ridurre l'effetto di un componente sul resto del processo, ad esempio un plug-in da un'origine non attendibile, mediante sandboxing e isolamento dal resto dei componenti del processo. In questi casi, è necessario utilizzare una factory isolata per il componente creato mediante sandbox.

Una factory con restrizioni è più bloccata rispetto A una factory isolata. Non interagisce in alcun modo con una cache dei tipi di carattere incrociata o persistente. Inoltre, la raccolta di tipi di carattere del sistema restituita da questa Factory include solo tipi di carattere noti. Se si passa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versione di DWrite precedente a DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) restituisce **E_INVALIDARG**.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10, Project Reunion 0,1 versione provvisoria [app Win32] |
| **Intestazione** | DWrite. h (include dwrite_core. h) |
