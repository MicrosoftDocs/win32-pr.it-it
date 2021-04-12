---
title: OP_JOINPROV2_PART
description: Definizione di OP_JOINPROV2_PART IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104118631"
---
# <a name="op_joinprov2_part-structure"></a>Struttura OP_JOINPROV2_PART

Contiene informazioni aggiuntive utilizzate per la configurazione di un client aggiunto a un dominio.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a>Members

### <a name="dwflags"></a>dwFlags

Deve essere impostato su zero o su uno dei valori seguenti:

|Valore|Significato|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|Il sito specificato in lpSiteName deve essere considerato il sito permanente per il client.|

### <a name="lpnetbiosname"></a>lpNetbiosName

Contiene il nome NetBIOS dell'account del computer in formato Unicode.

### <a name="lpsitename"></a>lpSiteName

Contiene il nome del sito Active Directory che il client deve utilizzare.

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

Contiene il nome di dominio DNS primario che il client deve utilizzare.

### <a name="dwreserved"></a>dwReserved

Riservato per un utilizzo futuro e deve essere impostato su 0.

### <a name="lpreserved"></a>lpReserved

Riservato per utilizzi futuri e deve essere impostato su NULL.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)
