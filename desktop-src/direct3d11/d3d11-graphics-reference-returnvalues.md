---
title: Codici restituiti Direct3D 11
description: Codici restituiti dalle funzioni API.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4130ed07faaabfd24bb48454d4e450f307c7a12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046881"
---
# <a name="direct3d-11-return-codes"></a>Codici restituiti Direct3D 11

Codici restituiti dalle funzioni API.

| HRESULT | Descrizione |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) | Impossibile trovare il file. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) | Troppe istanze univoche di un determinato tipo di oggetto di stato. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) | Troppe istanze univoche di un determinato tipo di oggetto visualizzazione. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) | La prima chiamata a [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) dopo [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) o [**sul ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) per risorsa non è stata D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (sostituito con DXGI_ERROR_INVALID_CALL) (0x887A0001) | La chiamata al metodo non è valida. Il parametro di un metodo, ad esempio, non può essere un puntatore valido. |
| D3DERR_WASSTILLDRAWING (sostituito con DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A) | L'operazione blit precedente che sta trasferendo informazioni da o verso questa superficie non è completa. |
| E_FAIL (0x80004005) | Si è tentato di creare un dispositivo con il livello di debug abilitato e il livello non è installato. |
| E_INVALIDARG (0x80070057) | Un parametro non valido è stato passato alla funzione di restituzione. |
| E_OUTOFMEMORY (0x8007000E) | Direct3D non è riuscito ad allocare memoria sufficiente per completare la chiamata. |
| E_NOTIMPL (0x80004001) | La chiamata al metodo non viene implementata con la combinazione di parametri passata. |
| S_FALSE ((HRESULT) 1L) | Valore di operazione riuscita alternativo, che indica un completamento positivo ma non standard (il significato esatto dipende dal contesto). |
| S_OK ((HRESULT) 0L) | Non si sono verificati errori. |

Per ulteriori codici restituiti, vedere [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Argomenti correlati

* [Riferimenti per Direct3D 11](d3d11-graphics-reference.md)