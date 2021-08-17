---
title: Funzione RoFailFastWithErrorContextInternal2
description: Genera un'eccezione non continuabile nel processo corrente e consente anche di includere contesto di errore aggiuntivo non ancora acquisito dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: a2e8e2e357b7c4768596ca36cb48cdf1bb2cfdbd839ecc6949a607975d6000c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560627"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>Funzione RoFailFastWithErrorContextInternal2

Genera un'eccezione non continuabile nel processo corrente e consente anche di includere contesto di errore aggiuntivo non ancora acquisito dal sistema operativo.

## <a name="syntax"></a>Sintassi

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a>Parametri

`hrError`

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

HRESULT **associato** all'errore corrente. L'eccezione viene generata per qualsiasi valore *di hrError*.

`cStowedExceptions`

Tipo: **[ULONG](../../winprog/windows-data-types.md)**

Numero di elementi nella *matrice aStowedExceptionPointers.*

`aStowedExceptionPointers`

Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Matrice di puntatori a [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) strutture . Ogni struttura contiene informazioni che descrivono un'eccezione stowed. Le informazioni in queste strutture vengono quindi inviate a Segnalazione errori Windows (WER) insieme alle informazioni sulle eccezioni stowed acquisite dalla piattaforma.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

**RoFailFastWithErrorContextInternal2** non è associato a una libreria di importazione né a un file di intestazione. È possibile chiamarlo prima usando la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (per caricare ) e quindi chiamando la funzione GetProcAddress per recuperare l'indirizzo di `ComBase.dll` **RoFailFastWithErrorContextInternal2.** [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Per altre informazioni, vedere [Funzione RoFailFastWithErrorContext.](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | N/A |
| **Libreria** | N/A |
| **DLL** | ComBase.dll |

## <a name="see-also"></a>Vedi anche

* [Funzione RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)