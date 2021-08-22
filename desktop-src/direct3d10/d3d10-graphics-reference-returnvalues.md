---
description: La tabella seguente contiene i codici restituiti dalle funzioni API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Codici restituiti Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c7e7bca25d240bf7775a6f4d6476148e3749e283ab4f8fb3511bf8b53bb711
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282801"
---
# <a name="direct3d-10-return-codes"></a>Codici restituiti Direct3D 10

La tabella seguente contiene i codici restituiti dalle funzioni API.



| HRESULT                                         | Descrizione                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILE DEGLI ERRORI D3D10 \_ \_ NON \_ \_ TROVATO                  | Impossibile trovare il file.                                                                                                                               |
| ERRORE D3D10 \_ TROPPI OGGETTI DI STATO \_ \_ \_ \_ \_ UNIVOCI | Sono presenti troppe istanze univoche di un particolare tipo di [oggetto di stato.](d3d10-graphics-programming-guide-api-features-state-objects.md)          |
| D3DERR \_ INVALIDCALL                             | La chiamata al metodo non è valida. Ad esempio, il parametro di un metodo potrebbe non essere un puntatore valido.                                                             |
| D3DERR \_ WASSTILLDRAWING                         | L'operazione blit precedente che sta trasferendo informazioni da o verso questa superficie è incompleta.                                                   |
| E \_ FAIL                                         | Si è tentato di creare un dispositivo con il [livello di debug](d3d10-graphics-programming-guide-api-features-layers.md) abilitato e il livello non è installato. |
| E \_ INVALIDARG                                   | Un parametro non valido è stato passato alla funzione restituita.                                                                                            |
| E \_ OUTOFMEMORY                                  | Direct3D non è stato in grado di allocare memoria sufficiente per completare la chiamata.                                                                                   |
| E \_ NOTIMPL                                      | La chiamata al metodo non viene implementata con la combinazione di parametri passata.                                                                              |
| S \_ FALSE                                        | Valore alternativo di operazione riuscita, che indica un completamento corretto ma non standard (il significato preciso dipende dal contesto).                                 |
| S \_ OK                                           | Non si sono verificati errori.                                                                                                                                    |



 

Per scrivere codice che gestisce in modo affidabile i valori [HRESULT,](../winprog/windows-data-types.md) usare le macro SUCCEEDED(hr) e FAILED(hr).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Informazioni di riferimento per Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
