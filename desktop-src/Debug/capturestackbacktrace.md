---
UID: ''
title: CaptureStackBackTrace (funzione)
description: Acquisisce una traccia dello stack indietro facendo scorrere lo stack.
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
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "106299329"
---
# <a name="capturestackbacktrace-function"></a>CaptureStackBackTrace (funzione)

## <a name="description"></a>Descrizione

Acquisisce una traccia dello stack indietro scorrendo lo stack e registrando le informazioni per ogni fotogramma.

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
È possibile acquisire fino a **MAXUSHORT** frame.

**Windows Server 2003 e Windows XP:**  La somma dei parametri *FramesToSkip* e *FramesToCapture* deve essere minore di 63.

### <a name="backtrace-out"></a>Backtrace [out]

Matrice di puntatori acquisiti dalla traccia dello stack corrente.

### <a name="backtracehash-out-optional"></a>BackTraceHash [out, optional]

Valore che può essere utilizzato per organizzare le tabelle hash.
Se questo parametro è **null**, non viene calcolato alcun valore hash.

Questo valore viene calcolato in base ai valori dei puntatori restituiti nella matrice di backtrace.
Due tracce dello stack identiche genereranno valori hash identici.

## <a name="returns"></a>Restituisce

Numero di frame acquisiti.

## <a name="remarks"></a>Commenti

La funzione **CaptureStackBackTrace** è definita come funzione **RtlCaptureStackBackTrace** (la definizione è inclusa nella Windows SDK a partire da Windows Vista).
Per ulteriori informazioni, vedere WinBase. h e WinNT. h.

## <a name="see-also"></a>Vedere anche
