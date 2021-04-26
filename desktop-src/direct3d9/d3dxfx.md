---
description: Opzioni per il salvataggio e la creazione di effetti.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995078"
---
# <a name="d3dxfx"></a>D3DXFX

Opzioni per il salvataggio e la creazione di effetti.

Le costanti nella tabella seguente sono definite in d3dx9effect.h.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Flag di salvataggio e ripristino dello stato dell'effetto</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Non viene salvato alcuno stato quando si chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> o restored quando si chiama <a href="id3dxeffect--end.md"><strong>End.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Un blocco di stato salva lo stato quando si chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>End.</strong></a></td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Un blocco di stato salva lo stato (ad eccezione degli shader e delle costanti shader) quando chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>End.</strong></a></td>
</tr>
<tr class="odd">
<td>Flag di creazione degli effetti</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>L'effetto non sarà clonabile e non conterrà dati binari dello shader. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc non</strong></a> restituirà puntatori a funzione shader. L'impostazione di questo flag riduce l'utilizzo della memoria degli effetti di circa il 50% perché elimina la necessità che il sistema di effetti manteni una copia degli shader in memoria. Questo flag viene usato da <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>e <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Abilita l'allocazione di una risorsa effetto nello spazio degli indirizzi uppder di un computer. Una limitazione importante è che non è possibile usare stringhe e gestire in modo intercambiabile. Ad esempio, gli elementi seguenti non funzionano più. <span data-codelanguage=""></span>
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

È invece necessario usare un metodo come [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) per archiviare l'handle del parametro, che viene quindi usato per passare variabili all'effetto.</td>
</tr>
</tbody>
</table>



 

Le costanti nella tabella seguente non sono definite per impostazione predefinita e devono essere definite dallo sviluppatore.



| Definizione del \# preprocessore degli effetti | Descrizione                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXFX \_ LARGEADDRESS \_ HANDLE   | Definire questo valore prima di includere d3dx9.h in modo che l'applicazione non venga compilata quando si tenta di passare stringhe nei parametri D3DXHANDLE. Ciò consente di assicurarsi che le informazioni valide vengano passate al runtime. |
| Flag del linker degli effetti            | Descrizione                                                                                                                                                                                                                          |
| INFORMAZIONI \_ SU INDIRIZZI DI GRANDI \_ DIMENSIONI          | L'impostazione del flag del linker LARGE ADDRESS AWARE = 1 consentirà all'applicazione di allocare risorse oltre il limite \_ \_ di indirizzi di 2 GB quando necessario.                                                                                      |



 

Il sistema di effetti usa blocchi di stato per salvare e ripristinare automaticamente lo stato. Per altre informazioni sui blocchi di stato, vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti degli effetti](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



