---
title: ODJ_BLOB
description: Definizione di ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104474591"
---
# <a name="odj_blob-structure"></a>Struttura ODJ_BLOB

Specifica una struttura che contiene una struttura di ODJ_WIN7BLOB serializzata o una struttura OP_PACKAGE serializzata.

## <a name="syntax"></a>Sintassi

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Members

### <a name="ulodjformat"></a>ulODJFormat

Specifica la versione logica della struttura e deve essere impostata su uno dei valori seguenti:

|Valore|Significato|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|I byte contenuti in pBlob devono contenere una struttura ODJ_WIN7_BLOB serializzata.|
|ODJ_WIN8_FORMAT (0x00000002)|I byte contenuti in pBlob devono contenere una struttura OP_PACKAGE serializzata.|

### <a name="cbblob"></a>cbBlob

Deve essere impostato sul numero di byte nella matrice pBlob.

### <a name="pblob"></a>pBlob

Punta a un buffer di byte contenente una struttura serializzata come specificato da ulODJFormat sopra.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

