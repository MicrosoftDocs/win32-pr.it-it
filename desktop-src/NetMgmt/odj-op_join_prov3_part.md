---
title: OP_JOINPROV3_PART
description: Definizione di OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104399877"
---
# <a name="op_joinprov3_part-structure"></a>Struttura OP_JOINPROV3_PART

Contiene informazioni aggiuntive utilizzate per la configurazione di un client aggiunto a un dominio.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>Members

### <a name="rid"></a>Sbarazzarsi

Deve essere impostato sull'identificatore relativo del SID dell'account del computer

### <a name="lpsid"></a>lpSid

Deve essere impostato sul SID dell'account del computer in formato stringa.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)
