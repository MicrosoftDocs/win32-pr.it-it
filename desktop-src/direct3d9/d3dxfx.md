---
description: Opzioni per il salvataggio e la creazione di effetti.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123387"
---
# <a name="d3dxfx"></a>D3DXFX

Opzioni per il salvataggio e la creazione di effetti.

Le costanti nella tabella seguente sono definite in d3dx9effect. h.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Flag di salvataggio e ripristino dello stato degli effetti</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Nessun stato viene salvato quando si chiama l' <a href="id3dxeffect--begin.md"><strong>inizio</strong></a> o il ripristino quando si chiama <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Un stateblock Salva lo stato quando si chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Un stateblock Salva lo stato (eccetto gli shader e le costanti shader) quando si chiama l'oggetto <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e si ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="odd">
<td>Flag di creazione effetti</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>L'effetto sarà non clonabile e non conterrà dati binari dello shader. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> non restituirà puntatori a funzioni shader. L'impostazione di questo flag riduce l'utilizzo della memoria da parte del 50% perché elimina la necessità che il sistema degli effetti mantenga una copia degli shader in memoria. Questo flag viene usato da <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>e <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Consente l'allocazione di una risorsa effetto nello spazio degli indirizzi di uppder di un computer. Una limitazione importante è che non è possibile usare stringhe e handle in modo interscambiabile. Ad esempio, il codice seguente non funzionerà più. <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

Al contrario, è necessario usare un metodo come [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) per archiviare l'handle del parametro, che viene quindi usato per passare le variabili all'effetto.</td>
</tr>
</tbody>
</table>



 

Le costanti nella tabella seguente non sono definite per impostazione predefinita e devono essere definite dallo sviluppatore.



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L'effetto del preprocessore \# definisce | Descrizione                                                                                                                                                                                                                          |
| \_Handle LARGEADDRESS \_ D3DXFX   | Definire questo valore prima di includere d3dx9. h in modo che l'applicazione non venga compilata quando si tenta di passare le stringhe nei parametri D3DXHANDLE. Ciò consentirà di garantire che le informazioni valide vengano passate al runtime. |
| Flag del linker effetti            | Descrizione                                                                                                                                                                                                                          |
| \_compatibile con indirizzi di grandi dimensioni \_          | Se si imposta il flag del linker \_ con un indirizzo di grandi dimensioni \_ = 1, l'applicazione può allocare risorse oltre il limite di 2 GB di indirizzi, se necessario.                                                                                      |



 

Il sistema degli effetti usa i blocchi di stato per salvare e ripristinare lo stato automaticamente. Per ulteriori informazioni sui blocchi di stato, vedere state [Blocks Save and Restore state (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti effetto](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



