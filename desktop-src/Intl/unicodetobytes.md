---
UID: ''
title: UnicodeToBytes (funzione)
description: Converte i caratteri Unicode in GB18030 byte.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "103719951"
---
# <a name="unicodetobytes-function"></a>UnicodeToBytes (funzione)

## <a name="description"></a>Descrizione

Deprecato. Converte i caratteri Unicode in GB18030 byte.

**Nota**  Quando si convertono i caratteri Unicode in GB18030 byte, un'applicazione da eseguire in Windows Vista e versioni successive deve usare la funzione [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>Parametri

### <a name="lpwidecharstr-in"></a>lpWideCharStr [in]

Puntatore alla stringa Unicode da convertire.

### <a name="cchwidechar-in"></a>cchWideChar [in]

Numero di caratteri della stringa Unicode da convertire.

### <a name="lpmultibytestr-in"></a>lpMultiByteStr [in]

Puntatore al buffer multibyte di destinazione.
Se *lpMultiByteStr* è 0, viene restituito il numero di byte del risultato GB18030 e non viene eseguita alcuna conversione.

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

Numero di byte del buffer multibyte di destinazione.
Se *cchMultiByte* è 0, viene restituito il numero di byte del risultato GB18030 e non viene eseguita alcuna conversione.

## <a name="returns"></a>Restituisce

Restituisce il numero di byte dei caratteri multibyte generati, in caso di esito positivo.

## <a name="remarks"></a>Commenti

## <a name="see-also"></a>Vedi anche

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
