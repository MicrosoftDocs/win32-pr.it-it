---
UID: ''
title: Funzione CaptureStackBackTrace
description: Acquisisce un'analisi dello stack di nuovo risalendo lo stack.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0b6cad22d7a52908c3aa02bef7e23a57899e421f87bda00660519750de742919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279502"
---
# <a name="capturestackbacktrace-function"></a>Funzione CaptureStackBackTrace

## <a name="description"></a>Descrizione

Acquisisce una traccia dello stack risalendo lo stack e registrando le informazioni per ogni frame.

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>Parametri

### <a name="framestoskip-in"></a>FramesToSkip [in]

Numero di frame da ignorare dall'inizio della traccia indietro.

### <a name="framestocapture-in"></a>FramesToCapture [in]

Numero di frame da acquisire.
È possibile acquisire fino a **frame MAXUSHORT.**

**Windows Server 2003 e Windows XP:**  La somma dei *parametri FramesToSkip* *e FramesToCapture* deve essere minore di 63.

### <a name="backtrace-out"></a>BackTrace [out]

Matrice di puntatori acquisiti dall'analisi dello stack corrente.

### <a name="backtracehash-out-optional"></a>BackTraceHash [out, facoltativo]

Valore che può essere utilizzato per organizzare le tabelle hash.
Se questo parametro è **NULL,** non viene calcolato alcun valore hash.

Questo valore viene calcolato in base ai valori dei puntatori restituiti nella matrice BackTrace.
Due analisi dello stack identiche genereranno valori hash identici.

## <a name="returns"></a>Restituisce

Numero di frame acquisiti.

## <a name="remarks"></a>Commenti

La **funzione CaptureStackBackTrace** è definita come funzione **RtlCaptureStackBackTrace** (la definizione è inclusa in Windows SDK a partire da Windows Vista).
Per altre informazioni, vedere WinBase.h e WinNT.h.

## <a name="see-also"></a>Vedere anche
