---
title: OP_CERT_SST_STORE
description: Definizione di OP_CERT_SST_STORE IDL
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104400012"
---
# <a name="op_cert_sst_store-structure"></a>Struttura OP_CERT_SST_STORE

Contiene un archivio certificati serializzato.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a>Members

### <a name="storelocation"></a>StoreLocation

Contiene un identificatore per l'archivio certificati dai [**percorsi dell'archivio di sistema**](../seccrypto/system-store-locations.md).

### <a name="pstorename"></a>pStoreName

Contiene il nome dell'archivio.

### <a name="cbsst"></a>cbSst

Contiene la dimensione di pSst in byte.

### <a name="psst"></a>pSst

Contiene un archivio certificati serializzato (vedere [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)