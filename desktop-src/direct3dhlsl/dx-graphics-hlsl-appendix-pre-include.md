---
title: " include (direttiva)"
description: Direttiva per il preprocessore che inserisce il contenuto del file specificato nel programma di origine nel punto in cui viene visualizzata la direttiva.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- includere la direttiva HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993437"
---
# <a name="include-directive"></a>\#include (direttiva)

Direttiva per il preprocessore che inserisce il contenuto del file specificato nel programma di origine nel punto in cui viene visualizzata la direttiva.


| \#Includi "*filename*"       |
|------------------------------|
| \#Includi *nome file* <> |

## <a name="parameters"></a>Parametri

| Elemento | Descrizione |
|------|-------------|
| *nomefile* | Nome del file da includere, facoltativamente preceduto da una specifica di directory. Il nome file deve specificare un file esistente. |

## <a name="remarks"></a>Commenti

La \# direttiva include causa la sostituzione della direttiva dall'intero contenuto del file specificato. Il preprocessore arresta la ricerca non appena trova un file con il nome specificato; Se si specifica un percorso completo e non ambiguo per il file, il preprocessore esegue la ricerca solo nel percorso specificato.

> [!NOTE]
> Lo [strumento di compilazione degli effetti](/windows/desktop/direct3dtools/fxc) ha un gestore di inclusione incorporato che usa l'opzione/i. Tuttavia, quando si esegue il compilatore dall'API, è possibile fornire un gestore di inclusione personalizzato implementando l'interfaccia ID3DXInclude.

La differenza tra le due forme di sintassi è l'ordine in cui il preprocessore cerca i file di intestazione quando il percorso viene specificato in modo incompleto, come illustrato nella tabella seguente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forma di sintassi</th>
<th>Modello di ricerca del preprocessore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#Includi <b>&quot;</b> <em>nome file</em><b>&quot;</b></td>
<td>Cerca il file di inclusione:
<ol>
<li>nella stessa directory del file che contiene la direttiva #include.</li>
<li>nelle directory dei file che contengono una direttiva #include per il file che contiene la direttiva #include.</li>
<li>nei percorsi specificati dall'opzione del compilatore/I nell'ordine in cui sono elencati.</li>
<li><p>nei percorsi specificati dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencati.</p>
<blockquote>
[!NOTE]<br />
La variabile di ambiente INCLUDE viene ignorata in un ambiente di sviluppo. Vedere la documentazione dell'ambiente di sviluppo per informazioni su come impostare i percorsi di inclusione per il progetto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#Includi <b><</b> <em>nome file</em><b>></b></td>
<td>Cerca il file di inclusione:
<ol>
<li>nei percorsi specificati dall'opzione del compilatore/I nell'ordine in cui sono elencati.</li>
<li><p>nei percorsi specificati dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencati.</p>
<blockquote>
[!NOTE]<br />
La variabile di ambiente INCLUDE viene ignorata in un ambiente di sviluppo. Vedere la documentazione dell'ambiente di sviluppo per informazioni su come impostare i percorsi di inclusione per il progetto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Esempio

L'esempio seguente fa sì che il preprocessore sostituisca la \# direttiva include con il contenuto di stdio. h. Poiché nell'esempio viene usato il formato della parentesi angolare, il preprocessore cercherà il file solo nelle directory elencate dall'opzione del compilatore/I e nella variabile di ambiente INCLUDE.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Vedi anche

- [Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [Interfaccia ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Effect-strumento compilatore](/windows/desktop/direct3dtools/fxc)