---
title: OP_PACKAGE_PART_COLLECTION
description: Definizione di OP_PACKAGE_PART_COLLECTION IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104047549"
---
# <a name="op_package_part_collection-structure"></a>Struttura OP_PACKAGE_PART_COLLECTION

Specifica una struttura che contiene una matrice di strutture di OP_PACKAGE_PART.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a>Members

### <a name="cparts"></a>cParts

Contiene il numero di elementi in pParts.

### <a name="pparts"></a>pParts

Contiene una matrice di strutture di OP_PACKAGE_PART.

### <a name="extension"></a>Estensione

Riservato per utilizzi futuri e deve essere impostato su tutti zeri.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_parte pacchetto \_ op**](odj-op_package_part.md)

[**\_BLOB op**](odj-op_blob.md)

