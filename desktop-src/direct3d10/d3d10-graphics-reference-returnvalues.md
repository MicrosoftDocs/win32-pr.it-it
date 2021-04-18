---
description: La tabella seguente contiene i codici restituiti dalle funzioni API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Codici restituiti Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304714"
---
# <a name="direct3d-10-return-codes"></a>Codici restituiti Direct3D 10

La tabella seguente contiene i codici restituiti dalle funzioni API.



| HRESULT                                         | Descrizione                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_File di errore D3D10 \_ \_ non \_ trovato                  | Impossibile trovare il file.                                                                                                                               |
| \_Errore D3D10 \_ troppi \_ \_ \_ oggetti stato \_ univoco | Troppe istanze univoche di un determinato tipo di [oggetto di stato](d3d10-graphics-programming-guide-api-features-state-objects.md).          |
| \_INVALIDCALL D3DERR                             | La chiamata al metodo non è valida. Il parametro di un metodo, ad esempio, non può essere un puntatore valido.                                                             |
| \_WASSTILLDRAWING D3DERR                         | L'operazione blit precedente che sta trasferendo informazioni da o verso questa superficie non è completa.                                                   |
| E \_ non riescono                                         | Si è tentato di creare un dispositivo con il [livello di debug](d3d10-graphics-programming-guide-api-features-layers.md) abilitato e il livello non è installato. |
| E \_ INVALIDARG                                   | Un parametro non valido è stato passato alla funzione di restituzione.                                                                                            |
| E \_ OutOfMemory                                  | Direct3D non è riuscito ad allocare memoria sufficiente per completare la chiamata.                                                                                   |
| E \_ NOTIMPL                                      | La chiamata al metodo non viene implementata con la combinazione di parametri passata.                                                                              |
| S \_ false                                        | Valore di operazione riuscita alternativo, che indica un completamento positivo ma non standard (il significato esatto dipende dal contesto).                                 |
| \_OK                                           | Non si sono verificati errori.                                                                                                                                    |



 

Per scrivere codice che gestisce [i valori HRESULT](../winprog/windows-data-types.md) in modo affidabile, usare le macro SUCCEEDED (HR) e failed (HR).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Informazioni di riferimento su Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
