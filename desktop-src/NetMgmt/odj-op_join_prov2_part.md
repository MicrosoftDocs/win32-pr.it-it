---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART definizione IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fa6853846695c02aabf85d0be865254608b9d4c00f39a372e99f1332e6eb4003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012459"
---
# <a name="op_joinprov2_part-structure"></a>OP_JOINPROV2_PART struttura

Contiene informazioni aggiuntive usate per la configurazione di un client aggiunto a un dominio.

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
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|Il sito specificato in lpSiteName DEVE essere considerato il sito permanente per il client.|

### <a name="lpnetbiosname"></a>lpNetbiosName

Contiene il nome Netbios dell'account computer in formato Unicode.

### <a name="lpsitename"></a>lpSiteName

Contiene il nome del sito di Active Directory che deve essere utilizzato dal client.

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

Contiene il nome di dominio DNS primario che deve essere utilizzato dal client.

### <a name="dwreserved"></a>dwReserved

Riservato per un uso futuro e deve essere impostato su 0.

### <a name="lpreserved"></a>lpReserved

Riservato per un uso futuro e deve essere impostato su NULL.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)
