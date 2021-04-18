---
title: Codici restituiti Direct3D 12
description: Di seguito sono riportati i codici restituiti dalle funzioni API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300260"
---
# <a name="direct3d-12-return-codes"></a>Codici restituiti Direct3D 12

Di seguito sono riportati i codici restituiti dalle funzioni API. Per ulteriori codici restituiti, vedere [DXGI \_ Error](/windows/desktop/direct3ddxgi/dxgi-error).



| HRESULT                                                                  | Descrizione                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_Adattatore errore \_ D3D12 \_ non \_ trovato                                        | L'oggetto PSO memorizzato nella cache specificato è stato creato in una scheda diversa e non può essere riutilizzato nell'adapter corrente.          |
| Versione del driver di errore D3D12 non \_ \_ \_ \_ corrispondente                                  | L'oggetto PSO memorizzato nella cache specificato è stato creato in una versione di driver diversa e non può essere riutilizzato nell'adapter corrente.  |
| D3DERR \_ INVALIDCALL (sostituito con DXGI \_ errore \_ chiamata non valida \_ )           | La chiamata al metodo non è valida. Il parametro di un metodo, ad esempio, non può essere un puntatore valido.                             |
| D3DERR \_ WASSTILLDRAWING (sostituito con DXGI \_ errore durante il \_ \_ \_ disegno) | L'operazione blit precedente che sta trasferendo informazioni da o verso questa superficie non è completa.                   |
| E \_ non riescono                                                                  | Si è tentato di creare un dispositivo con il livello di debug abilitato e il livello non è installato.                             |
| E \_ INVALIDARG                                                            | Un parametro non valido è stato passato alla funzione di restituzione.                                                             |
| E \_ OutOfMemory                                                           | Direct3D non è riuscito ad allocare memoria sufficiente per completare la chiamata.                                                   |
| E \_ NOTIMPL                                                               | La chiamata al metodo non viene implementata con la combinazione di parametri passata.                                               |
| S \_ false                                                                 | Valore di operazione riuscita alternativo, che indica un completamento positivo ma non standard (il significato esatto dipende dal contesto). |
| \_OK                                                                    | Non si sono verificati errori.                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 