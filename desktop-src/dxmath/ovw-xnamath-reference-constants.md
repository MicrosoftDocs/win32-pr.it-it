---
description: Le costanti seguenti vengono fornite dalla libreria DirectXMath.
ms.assetid: a206fe22-12c8-ac2b-ee37-20cfff35841a
title: Costanti della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb63bc687dd6bf3cc1dcc5e1801b500761480c7b8443b7a786a05211b9fb729d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118500388"
---
# <a name="directxmath-library-constants"></a>Costanti della libreria DirectXMath

Le costanti seguenti vengono fornite dalla libreria DirectXMath.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DIRECTXMATH_VERSION<br/></td>
<td>Versione della libreria DirectXMath. La versione di anteprima iniziale è la 300, la Windows 8 finale è la 303, la Windows 8.1 versione è 305. Le versioni di XNA Math erano 200, 201, 202, 203, 204 e così via. Viene definito come simbolo del preprocessore.<br/></td>
</tr>
<tr class="even">
<td>XM_PI<br/></td>
<td>Rappresentazione ottimale di π.<br/></td>
</tr>
<tr class="odd">
<td>XM_2PI<br/></td>
<td>Rappresentazione ottimale di 2*π.<br/></td>
</tr>
<tr class="even">
<td>XM_1DIVPI<br/></td>
<td>Rappresentazione ottimale di 1/π.<br/></td>
</tr>
<tr class="odd">
<td>XM_1DIV2PI<br/></td>
<td>Rappresentazione ottimale di 2/π.<br/></td>
</tr>
<tr class="even">
<td>XM_PIDIV2<br/></td>
<td>Rappresentazione ottimale di π/2.<br/></td>
</tr>
<tr class="odd">
<td>XM_PIDIV4<br/></td>
<td>Rappresentazione ottimale di π/4.<br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_0X<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente X del primo argomento del vettore in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_0Y<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente Y del primo argomento del vettore in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_0Z<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente Z del primo argomento del vettore in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_0W<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente W del primo argomento vector in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_1X<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente X del secondo argomento vector in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_1Y<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente Y del secondo argomento vector in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_1Z<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente Z del secondo argomento vector in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_1W<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute.</strong></a> Ciò indica che il componente W del secondo argomento vector in <strong>XMVectorPermute</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="even">
<td>XM_SELECT_0<br/></td>
<td>Costante utilizzata per costruire un vettore di controllo usato <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect"><strong>con XMVectorSelect.</strong></a> Indica che il componente del primo argomento vector in <strong>XMVectorSelect</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente al relativo indice nel vettore di controllo.<br/> Ad esempio, un vettore di controllo con XM_SELECT_0 come secondo componente copia il secondo componente del primo vettore nel secondo componente del vettore di risultato. <br/></td>
</tr>
<tr class="odd">
<td>XM_SELECT_1<br/></td>
<td>Costante utilizzata per costruire un vettore di controllo usato <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect"><strong>con XMVectorSelect.</strong></a> Indica che il componente del secondo argomento vector in <strong>XMVectorSelect</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente al relativo indice nel vettore di controllo. <br/> Ad esempio, un vettore di controllo con XM_SELECT_1 come secondo componente copia il secondo componente del secondo vettore nel secondo componente del vettore di risultato. <br/></td>
</tr>
<tr class="even">
<td>XM_SWIZZLE_X<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle.</strong></a> Ciò indica che il componente X dell'argomento vector di <strong>XMVectorSwizzle</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato.<br/></td>
</tr>
<tr class="odd">
<td>XM_SWIZZLE_Y<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle.</strong></a> Ciò indica che il componente Y dell'argomento vector di <strong>XMVectorSwizzle</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="even">
<td>XM_SWIZZLE_Z<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle.</strong></a> Ciò indica che il componente Z dell'argomento vector in <strong>XMVectorSwizzle</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="odd">
<td>XM_SWIZZLE_W<br/></td>
<td>Costante utilizzata come indice di elemento con <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle.</strong></a> Ciò indica che il componente W dell'argomento vector di <strong>XMVectorSwizzle</strong> deve essere copiato nella posizione di indice in un vettore di risultato corrispondente all'elemento specificato. <br/></td>
</tr>
<tr class="even">
<td>XM_CRMASK_CR6<br/></td>
<td>Maschera per ottenere un risultato di confronto, che in genere viene recuperato usando una versione di registrazione di una funzione DirectXMath, ad <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>esempio XMVector4EqualR.</strong></a> L'esempio seguente ottiene il risultato del confronto dalla variabile CR:
<pre class="syntax" data-space="preserve"><code>uint32_t val = ((CR) & XM_CRMASK_CR6);</code></pre>
<br/></td>
</tr>
<tr class="odd">
<td>XM_CRMASK_CR6TRUE<br/></td>
<td>Maschera per ottenere un risultato di confronto e verificare se è un valore true logico. Il valore viene in genere recuperato usando una versione di registrazione di una funzione DirectXMath, ad <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>esempio XMVector4EqualR.</strong></a> L'esempio controlla se la variabileq CR è true:
<pre class="syntax" data-space="preserve"><code>bool val = (((CR) & XM_CRMASK_CR6FALSE) == XM_CRMASK_CR6FALSE);</code></pre>
Vedere anche <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonanytrue"><strong>XMComparisonAnyTrue,</strong></a> <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonalltrue"><strong>XMComparisonAllTrue</strong></a>e <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonmixed"><strong>XMComparisonMixed</strong></a><br/></td>
</tr>
<tr class="even">
<td>XM_CRMASK_CR6FALSE<br/></td>
<td>Maschera per ottenere un risultato di confronto e verificare se è un valore logico false. Il valore viene in genere recuperato usando una versione di registrazione di una funzione matematica DirectXMath, ad <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>esempio XMVector4EqualR.</strong></a> L'esempio controlla se la variabile CR è false:
<pre class="syntax" data-space="preserve"><code>bool val = (((CR) & XM_CRMASK_CR6FALSE) == XM_CRMASK_CR6FALSE);</code></pre>
Vedere anche <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonanyfalse"><strong>XMComparisonAnyFalse,</strong></a> <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonallfalse"><strong>XMComparisonAllFalse</strong></a> e <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonmixed"><strong>XMComparisonMixed</strong></a><br/></td>
</tr>
<tr class="odd">
<td>XM_CRMASK_CR6BOUNDS<br/></td>
<td>Maschera per ottenere un risultato di confronto e verificare se il risultato indica che alcuni input non sono stati vincolati. Il valore viene in genere recuperato usando una versione di registrazione di una funzione DirectXMath, ad <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>esempio XMVector4EqualR.</strong></a> L'esempio controlla se la variabile CR indica e lo stato fuori dai limiti.
<pre class="syntax" data-space="preserve"><code>bool val = (((CR) & XM_CRMASK_CR6BOUNDS) == XM_CRMASK_CR6BOUNDS);</code></pre>
Vedere anche <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonallinbounds"><strong>XMComparisonAllInBounds</strong></a> e <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonanyoutofbounds"><strong>XMComparisonAnyOutOfBounds</strong></a><br/></td>
</tr>
<tr class="even">
<td>Colors::AliceBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::ColorsWhite</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Acqua</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Acquamarina</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Azure</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Tema</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Bisque</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Nero</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::ColorshedAlmond</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Blu</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::BlueViolet</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Brown</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::BurlyWood</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::CadetBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::Chartreuse</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Chocolate</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Coral</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::FlowflowerBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::Tuttosilk</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::Nalson</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Ciano</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkCyan</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkGoldenrod</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkGray</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkGreen</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkKhaki</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkMagenta</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkOliveGreen</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkOrange</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkOrchid</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkRed</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkSalmon</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkSeaGreen</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkSlateBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkSlateGray</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D arkTurquoise</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D arkViolet</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D eepPink</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D eepSkyBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::D imGray</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::D odgerBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Firebrick</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::ColorsWhite</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::ForestGreen</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Fuchsia</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::Gainsboro</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::GhostWhite</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Gold</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::Goldenrod</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Grigio</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Verde</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::GreenYellow</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::Honeydew</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::HotPink</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::IndiaRed</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Indigo</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Ivory</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Temaki</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Lavender</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::LavenderBlush</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::LawnGreen</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::ColorsChiffon</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::LightBlue</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::LightCoral</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::LightCyan</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::LightGoldenrodYellow</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Verde chiaro</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::LightGray</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colors::LightPink</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::LightSalmon</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::LightSeaGreen</td>
<td>Costanti per le definizioni dei colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::LightSkyBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::LightSlateGray</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::LightSteelBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::LightYellow</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Lime</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::LimeGreen</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Lino</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Magenta</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Maroon</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::MediumAquamarine</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::MediumBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::MediumOrchid</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::MediumPurple</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::MediumSeaGreen</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::MediumSlateBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::MediumSpringGreen</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::MediumTurquoise</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::MediumVioletRed</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::MidnightBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::MintCream</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::MistyRose</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Moccasin</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::NavajoWhite</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Blu blu</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::OldLace</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Olive</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::OliveDrab</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Arancione</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::OrangeRed</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Orchidea</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::P aleGoldenrod</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::P aleGreen</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::P aleTurquoise</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::P aleVioletRed</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::P apayaWhip</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::P eachPuff</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::P eru</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::P ink</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::P lum</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::P owderBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::P urple</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Rosso</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::RosyBrown</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::RoyalBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colors::SaddleBrown</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Salmon</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::SandyBrown</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::SeaGreen</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::SeaShell</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Sienna</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Silver</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::SkyBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::SlateBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::SlateGray</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Snow</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::SpringGreen</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::SteelBlue</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Tan</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Teal</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Thistle</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Tomato</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Trasparente</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Turchese</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Viola</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::Tutto</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Bianco</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::WhiteSmoke</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="odd">
<td>Colori::Giallo</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
<tr class="even">
<td>Colori::YellowGreen</td>
<td>Costanti per le definizioni di colori .NET standard. Questi valori sono dati R, G, B che possono essere usati come XMVECTOR o passati direttamente al metodo Clear dell'API Direct3D 10.x/Direct3D 11.</td>
</tr>
</tbody>
</table>



 

> [!Note]
>
> Tutte le costanti Colors sono definite nello spazio colori [sRGB](https://en.wikipedia.org/wiki/SRGB) standard(così come i colori .NET e i colori HTML sicuri per il Web). Per il rendering corretto con gamma con spazio colore lineare, i valori devono essere regolati leggermente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

<span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[Informazioni di riferimento sulla programmazione DirectXMath](ovw-xnamath-reference.md)
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla programmazione DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 
