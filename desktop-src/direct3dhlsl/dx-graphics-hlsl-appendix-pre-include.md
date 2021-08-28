---
title: " Direttiva include"
description: Direttiva del preprocessore che inserisce il contenuto del file specificato nel programma di origine nel punto in cui viene visualizzata la direttiva.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- Direttiva include HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 079ae2680a2610993c3cd54ac64afdfcbafa25c9
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627467"
---
# <a name="include-directive"></a>\#Direttiva include

Direttiva del preprocessore che inserisce il contenuto del file specificato nel programma di origine nel punto in cui viene visualizzata la direttiva.


| \#include "*filename*"       |
|------------------------------|
| \#include <*filename*> |

## <a name="parameters"></a>Parametri

| Elemento | Descrizione |
|------|-------------|
| *nomefile* | Nome file del file da includere, preceduto facoltativamente da una specifica di directory. Il nome file deve specificare un file esistente. |

## <a name="remarks"></a>Commenti

La \# direttiva include causa la sostituzione della direttiva con l'intero contenuto del file specificato. Il preprocessore interrompe la ricerca non appena trova un file con il nome specificato. Se si specifica un percorso completo e non ambiguo per il file, il preprocessore cerca solo il percorso specificato.

> [!NOTE]
> Lo [strumento Effect-Compiler include](/windows/desktop/direct3dtools/fxc) un gestore di inclusione predefinito che usa l'opzione /I. Tuttavia, quando si esegue il compilatore dall'API, è possibile fornire un gestore di inclusione personalizzato implementando l'interfaccia ID3DXInclude.

La differenza tra le due forme di sintassi è l'ordine in cui il preprocessore cerca i file di intestazione quando il percorso viene specificato in modo incompleto, come illustrato nella tabella seguente.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Forma di sintassi</th>
<th>Criterio di ricerca del preprocessore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#include <b>&quot;</b> <em></em> filename<b>&quot;</b></td>
<td>Cerca il file di inclusione:
<ol>
<li>nella stessa directory del file che contiene la direttiva #include.</li>
<li>nelle directory di tutti i file che contengono una direttiva #include per il file che contiene la direttiva #include.</li>
<li>nei percorsi specificati dall'opzione del compilatore /I, nell'ordine in cui sono elencati.</li>
<li><p>in percorsi specificati dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencati.</p>
<blockquote>
[!NOTE]<br />
La variabile di ambiente INCLUDE viene ignorata in un ambiente di sviluppo. Per informazioni su come impostare i percorsi di inclusione per il progetto, vedere la documentazione dell'ambiente di sviluppo.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#include <b><</b> <em></em> filename<b>></b></td>
<td>Cerca il file di inclusione:
<ol>
<li>nei percorsi specificati dall'opzione del compilatore /I, nell'ordine in cui sono elencati.</li>
<li><p>in percorsi specificati dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencati.</p>
<blockquote>
[!NOTE]<br />
La variabile di ambiente INCLUDE viene ignorata in un ambiente di sviluppo. Per informazioni su come impostare i percorsi di inclusione per il progetto, vedere la documentazione dell'ambiente di sviluppo.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Esempio

Nell'esempio seguente il preprocessore sostituisce la \# direttiva include con il contenuto di stdio.h. Poiché nell'esempio viene utilizzato il formato parentesi uncinata, il preprocessore cerca il file solo nelle directory elencate dall'opzione del compilatore /I e dalla variabile di ambiente INCLUDE.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Vedi anche

- [Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [Interfaccia ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Strumento compilatore effetti](/windows/desktop/direct3dtools/fxc)
