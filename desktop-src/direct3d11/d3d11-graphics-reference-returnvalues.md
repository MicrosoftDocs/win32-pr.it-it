---
title: Codici restituiti Direct3D 11
description: Codici restituiti dalle funzioni API.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d932c3ce3828f375e90bf322af6c42dc112b845f44dfe22f0d0988930129efea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990041"
---
# <a name="direct3d-11-return-codes"></a>Codici restituiti Direct3D 11

Codici restituiti dalle funzioni API.

| HRESULT | Descrizione |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) | Impossibile trovare il file. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) | Sono presenti troppe istanze univoche di un particolare tipo di oggetto stato. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) | Sono presenti troppe istanze univoche di un particolare tipo di oggetto vista. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) | La prima chiamata a [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) dopo [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) o [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) per risorsa non è stata D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (sostituito con DXGI_ERROR_INVALID_CALL) (0x887A0001) | La chiamata al metodo non è valida. Ad esempio, il parametro di un metodo potrebbe non essere un puntatore valido. |
| D3DERR_WASSTILLDRAWING (sostituito con DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A) | L'operazione blit precedente che trasferisce informazioni da o verso questa superficie è incompleta. |
| E_FAIL (0x80004005) | Si è tentato di creare un dispositivo con il livello di debug abilitato e il livello non è installato. |
| E_INVALIDARG (0x80070057) | È stato passato un parametro non valido alla funzione restituita. |
| E_OUTOFMEMORY (0x8007000E) | Direct3D non è stato in grado di allocare memoria sufficiente per completare la chiamata. |
| E_NOTIMPL (0x80004001) | La chiamata al metodo non viene implementata con la combinazione di parametri passata. |
| S_FALSE ((HRESULT)1L) | Valore di esito positivo alternativo, che indica un completamento riuscito ma non standard (il significato preciso dipende dal contesto). |
| S_OK ((HRESULT)0L) | Non si sono verificati errori. |

Per altri codici restituiti, [vedere DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Argomenti correlati

* [Riferimenti per Direct3D 11](d3d11-graphics-reference.md)