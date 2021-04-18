---
title: OP_CERT_PART
description: Definizione di OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300651"
---
# <a name="op_cert_part-structure"></a>Struttura OP_CERT_PART

Contiene i file PFX serializzati e gli archivi certificati.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a>Members

### <a name="cpfxstores"></a>cPfxStores

Contiene il numero di elementi in pPfxStores.

### <a name="ppfxstores"></a>pPfxStores

Contiene una matrice di strutture di OP_CERT_PFX_STORE.

### <a name="csststores"></a>cSstStores

Contiene il numero di elementi in pSstStores.

### <a name="psststores"></a>pSstStores

Contiene una matrice di strutture di OP_CERT_SST_STORE.

### <a name="extension"></a>Estensione

Riservato per usi futuri e deve contenere tutti zeri.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_ \_ Archivio pfx del certificato op \_**](odj-op_cert_pfx_store.md)

[**\_Archivio di \_ SST del certificato op \_**](odj-op_cert_sst_store.md)

[**\_BLOB op**](odj-op_blob.md)

