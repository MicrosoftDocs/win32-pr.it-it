---
title: OP_PACKAGE
description: Definizione di OP_PACKAGE IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300648"
---
# <a name="op_package-structure"></a>Struttura OP_PACKAGE

Contiene una struttura che contiene un OP_PACKAGE_COLLECTION serializzato.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a>Members

### <a name="encryptiontype"></a>EncryptionType

Riservato per utilizzi futuri e deve essere impostato su GUID_NULL.

### <a name="encryptioncontext"></a>EncryptionContext

Riservato per utilizzi futuri e deve essere impostato su tutti zeri.

### <a name="wrappedpartcollection"></a>WrappedPartCollection

Struttura di OP_BLOB contenente una struttura OP_PACKAGE_COLLECTION serializzata.

### <a name="cbdecryptedpartcollection"></a>cbDecryptedPartCollection

Riservato per utilizzi futuri e deve essere impostato su zero.

### <a name="extension"></a>Estensione

Riservato per utilizzi futuri e deve essere impostato su tutti zeri.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_BLOB op**](odj-op_blob.md)

[**\_raccolta pacchetti \_ op**](odj-op_package_collection.md)
