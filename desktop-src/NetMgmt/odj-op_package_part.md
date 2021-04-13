---
title: OP_PACKAGE_PART
description: Definizione di OP_PACKAGE_PART IDL
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104224570"
---
# <a name="op_package_part-structure"></a>Struttura OP_PACKAGE_PART

Definisce una struttura che contiene un set di dati identificato da un GUID.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a>Members

### <a name="parttype"></a>PartType

Identifica la struttura serializzata contenuta nella parte per la tabella seguente:

|PartType|Significato|
| --- | --- |
|GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}|Contiene una struttura di ODJ_WIN7_BLOB serializzata.|
|GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}|Contiene una struttura di OP_JOIN_PROV2_PART serializzata.|
|GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}|Contiene una struttura di OP_JOIN_PROV3_PART serializzata.|
|GUID_CERT_PROVIDER {9c0971e9-832F-4873-8e87-ef1419d4781e}|Contiene una struttura di OP_CERT_PART serializzata.|
|GUID_POLICY_PROVIDER {68fb602a-0C09-48ce-b75f-07b7bd58f7ec}|Contiene una struttura di OP_POLICY_PART serializzata.|

### <a name="ulflags"></a>ulFlags

Deve essere impostato su zero o più dei flag seguenti:

|Valore|Significato|
| --- | --- |
|OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)|Questa parte del pacchetto è considerata essenziale. Se il consumer non riconosce questa parte del pacchetto o non è in grado di elaborarla correttamente, l'operazione complessiva deve avere esito negativo.|

### <a name="part"></a>Parte

Contiene una struttura serializzata in una struttura OP_BLOB. La struttura specifica è determinata da PartType.

### <a name="extension"></a>Estensione

Riservato per utilizzi futuri e deve essere impostato su tutti zeri.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_BLOB op**](odj-op_blob.md)
