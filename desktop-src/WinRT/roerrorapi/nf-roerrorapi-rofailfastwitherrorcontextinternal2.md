---
title: RoFailFastWithErrorContextInternal2 (funzione)
description: Genera un'eccezione non continuabile nel processo corrente e consente anche di includere un contesto di errore aggiuntivo non ancora acquisito dal sistema operativo.
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
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300596"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>RoFailFastWithErrorContextInternal2 (funzione)

Genera un'eccezione non continuabile nel processo corrente e consente anche di includere un contesto di errore aggiuntivo non ancora acquisito dal sistema operativo.

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

**HRESULT** associato all'errore corrente. L'eccezione viene generata per qualsiasi valore di *hrError*.

`cStowedExceptions`

Tipo: **[ULONG](../../winprog/windows-data-types.md)**

Numero di elementi nella matrice *aStowedExceptionPointers* .

`aStowedExceptionPointers`

Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Matrice di puntatori a strutture di [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) . Ogni struttura contiene informazioni che descrivono un'eccezione riposta. Le informazioni contenute in queste strutture vengono quindi inviate a Segnalazione errori Windows (WER) insieme alle informazioni rilevate sulle eccezioni acquisite dalla piattaforma.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

**RoFailFastWithErrorContextInternal2** non è associato a una libreria di importazione né a un file di intestazione. È possibile chiamare il metodo usando prima la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (per caricare `ComBase.dll` ), quindi chiamando la funzione [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare l'indirizzo di **RoFailFastWithErrorContextInternal2**.

Per altre informazioni, vedere [funzione RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | N/D |
| **Libreria** | N/D |
| **DLL** | ComBase.dll |

## <a name="see-also"></a>Vedi anche

* [RoFailFastWithErrorContext (funzione)](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)