---
title: OP_BLOB
description: Definizione di OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104399881"
---
# <a name="op_blob-structure"></a>Struttura OP_BLOB

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

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)
