---
title: OP_BLOB
description: OP_BLOB IDL Definition
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 757df1549d1bdb0a9a87ee22373a1903a034a1e267d087d51dac46bb6bc5a762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796891"
---
# <a name="op_blob-structure"></a>OP_BLOB struttura

Contiene un buffer di byte opaco.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Members

### <a name="cbblob"></a>cbBlob

Specifica la dimensione di pBlob in byte.

### <a name="pblob"></a>pBlob

Punta a un buffer di byte.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)
