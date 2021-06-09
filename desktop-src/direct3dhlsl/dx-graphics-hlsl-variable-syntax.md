---
title: Sintassi delle variabili
description: Usare le regole di sintassi seguenti per dichiarare le variabili HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintassi delle variabili (DirectX HLSL)
- nointerpolation, sintassi delle variabili (DirectX HLSL)
- shared, Variable Syntax (DirectX HLSL)
- groupshared, sintassi delle variabili (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- uniform, Variable Syntax (DirectX HLSL)
- volatile, sintassi delle variabili (DirectX HLSL)
- precise, Sintassi delle variabili (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 446444e09b0b6aff3e0ba8ca8b12cfbf6dc94128
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826069"
---
# <a name="variable-syntax"></a>Sintassi delle variabili

Usare le regole di sintassi seguenti per dichiarare le variabili HLSL.

\[*Archiviazione \_ Class* \] \[ *Type \_ Modifier* \] *Type Name* \[ *Index* \] \[ *: Semantic*: \] \[ *Packoffset*: \] \[ *Register* \] ;    \[  \] Annotazioni \[ *= Iniziale \_ Valore*                    \]



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Classe di \_ archiviazione* 
</dt> <dd>

Modificatori facoltativi della classe di archiviazione che forniscono al compilatore suggerimenti sull'ambito e sulla durata delle variabili; I modificatori possono essere specificati in qualsiasi ordine.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>extern</strong></td>
<td>Contrassegnare una variabile globale come input esterno per lo shader. si tratta del contrassegno predefinito per tutte le variabili globali. Non può essere combinato con <strong>statico.</strong></td>
</tr>
<tr class="even">
<td><strong>nointerpolation</strong></td>
<td>Non interpolare gli output di un vertex shader prima di passarli a un pixel shader.</td>
</tr>
<tr class="odd">
<td><strong>Preciso</strong></td>
<td>Se <strong>applicata</strong> a una variabile, la parola chiave precise limiterà i calcoli usati per produrre il valore assegnato a tale variabile nei modi seguenti:

*   Le operazioni separate vengono mantenute separate. Ad esempio, quando un'operazione mul e add potrebbe essere stata fusa in un'operazione di matto, <strong>precise</strong> forzano le operazioni a rimanere separate. È invece necessario usare in modo esplicito la funzione intrinseca di tipo "mad".
*   L'ordine delle operazioni viene mantenuto. Se l'ordine delle istruzioni potrebbe essere stato casuale per migliorare le <strong>prestazioni,</strong> la precisione garantisce che il compilatore manteni l'ordine così come è stato scritto.
*   Le operazioni non sicure IEEE sono limitate. Se il compilatore potrebbe aver usato operazioni matematiche veloci che non rispettano i valori <strong></strong> NaN (non un numero) e INF (infinito), la precisione forza il rispetto dei requisiti IEEE relativi ai valori NaN e INF. Senza <strong>precisione,</strong>queste ottimizzazioni e operazioni matematiche non sono sicure IEEE.
*   Qualificare una variabile <strong>precisa</strong> non rende precise le operazioni che usano la <strong>variabile</strong>. Poiché <strong>precise</strong> si propaga solo alle operazioni che contribuiscono ai valori assegnati alla variabile precisa qualificata, l'esecuzione corretta dei calcoli <strong></strong> desiderati può essere difficile, quindi è consigliabile contrassegnare gli output dello shader direttamente nel punto in cui vengono dichiarati, indipendentemente dal fatto che si tratta di un campo della struttura o di un parametro di output o del tipo restituito della funzione entry. <strong></strong> <strong></strong>

La possibilità di controllare le ottimizzazioni in questo modo mantiene l'invarianza dei risultati per la variabile di output modificata disabilitando le ottimizzazioni che potrebbero influire sui risultati finali a causa di differenze nelle differenze di precisione accumulate. È utile quando si vuole che gli shader per la tessellazione mantengano le schele di patch a tenuta d'acqua o corrispondano ai valori di profondità su più passaggi.

[Codice di esempio:](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl) 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><strong>condiviso</strong></td>
<td>Contrassegnare una variabile per la condivisione tra gli effetti; Si tratta di un suggerimento per il compilatore.</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>Contrassegnare una variabile per la memoria condivisa del gruppo di thread per gli shader di calcolo. In D3D10 la dimensione totale massima di tutte le variabili con la classe di archiviazione groupshared è 16 KB, in D3D11 la dimensione massima è 32 KB. Vedere gli esempi.</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>Contrassegnare una variabile locale in modo che sia inizializzata una sola volta e sia persistente tra le chiamate di funzione. Se la dichiarazione non include un inizializzatore, il valore viene impostato su zero. Una variabile globale contrassegnata <strong>come static</strong> non è visibile a un'applicazione.</td>
</tr>
<tr class="odd">
<td><strong>uniform</strong></td>
<td>Contrassegnare una variabile i cui dati sono costanti durante l'esecuzione di uno shader, ad esempio un colore materiale in un vertex shader. Le variabili globali sono considerate <strong>uniformi per</strong> impostazione predefinita.</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>Contrassegnare una variabile che cambia di frequente. Si tratta di un suggerimento per il compilatore. Questo modificatore di classe di archiviazione si applica solo a una variabile locale.<br/>
<blockquote>
[!Note]<br />
Il compilatore HLSL attualmente ignora questo modificatore di classe di archiviazione.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Modificatore di \_ tipo*
</dt> <dd>

Modificatore di tipo variabile facoltativo.



| Valore             | Descrizione                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Contrassegnare una variabile che non può essere modificata da uno shader, pertanto deve essere inizializzata nella dichiarazione della variabile. Le variabili globali sono considerate **const** per impostazione predefinita(eliminare questo comportamento fornendo il flag /Gec al compilatore). |
| **row \_ major**    | Contrassegnare una variabile che archivia quattro componenti in una singola riga in modo che possano essere archiviati in un unico registro costante.                                                                                                                             |
| **column \_ major** | Contrassegnare una variabile che archivia 4 componenti in una singola colonna per ottimizzare le operazioni matematiche della matrice.                                                                                                                                                         |



 

> [!Note]  
> Se non si specifica un valore di modificatore di tipo, il compilatore usa **column \_ major** come valore predefinito.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*digitare*
</dt> <dd>

Qualsiasi tipo HLSL elencato in [Tipi di dati (DirectX HLSL).](dx-graphics-hlsl-data-types.md)

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nome* \[ *Indice*\]
</dt> <dd>

Stringa ASCII che identifica in modo univoco una variabile shader. Per definire una matrice facoltativa, usare **index** per le dimensioni della matrice, ovvero un numero intero positivo = 1.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantica*
</dt> <dd>

Informazioni facoltative sull'utilizzo dei parametri, usate dal compilatore per collegare input e output dello shader. Esistono diverse semantiche [predefinite per](dx-graphics-hlsl-semantics.md) vertex shader e pixel shader. Il compilatore ignora la semantica a meno che non siano dichiarate in una variabile globale o un parametro passato in uno shader.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Parola chiave facoltativa per la creazione manuale di un pacchetto delle costanti shader. Vedere [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registro*
</dt> <dd>

Parola chiave facoltativa per l'assegnazione manuale di una variabile shader a un registro specifico. Vedere [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotazioni*
</dt> <dd>

Metadati facoltativi, sotto forma di stringa, associati a una variabile globale. Un'annotazione viene usata dal framework degli effetti e ignorata da HLSL; Per una sintassi più dettagliata, vedere Sintassi [delle annotazioni.](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax)

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Valore \_ iniziale*
</dt> <dd>

Valori iniziali facoltativi; il numero di valori deve corrispondere al numero di componenti nel *tipo*. Ogni variabile globale contrassegnata **come extern** deve essere inizializzata con un valore letterale. Ogni variabile contrassegnata **come static** deve essere inizializzata con una costante.

Le variabili globali non contrassegnate **come statiche** o **extern** non vengono compilate nello shader. Il compilatore non imposta automaticamente i valori predefiniti per le variabili globali e non può usarli nelle ottimizzazioni. Per inizializzare questo tipo di variabile globale, usare la reflection per ottenere il relativo valore e quindi copiare il valore in un buffer costante. Ad esempio, è possibile usare il metodo [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) per ottenere la variabile, usare il metodo [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) per ottenere la descrizione della variabile shader e ottenere il valore iniziale dal membro **DefaultValue** della struttura [**\_ \_ \_ DESC D3D11 SHADER VARIABLE.**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) Per copiare il valore nel buffer costante, è necessario assicurarsi che il buffer sia stato creato con l'accesso in scrittura della CPU [**(D3D11 \_ CPU \_ ACCESS \_ WRITE).**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag) Per altre informazioni su come creare un buffer costante, [vedere Procedura: Creare un buffer costante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)

È anche possibile usare il [framework degli effetti](../direct3d11/d3d11-graphics-programming-guide-effects.md) per elaborare automaticamente l'oggetto che riflette e imposta il valore iniziale. Ad esempio, è possibile usare il [**metodo ID3DX11EffectPass::Apply.**](/windows/desktop/direct3d11/id3dx11effectpass-apply)

</dd> </dl>

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi di dichiarazioni di variabili shader.


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a>Gruppo condiviso

HLSL consente ai thread di un compute shader di scambiare valori tramite memoria condivisa. HLSL fornisce primitive di barriera, ad esempio [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)e così via, per garantire l'ordinamento corretto delle operazioni di lettura e scrittura nella memoria condivisa nello shader ed evitare race di dati.

> [!Note]  
> L'hardware esegue thread in gruppi (warp o fronti d'onda) e la sincronizzazione delle barriere può talvolta essere omessa per aumentare le prestazioni quando è corretta solo la sincronizzazione dei thread che appartengono allo stesso gruppo. Tuttavia, questa omissione è fortemente sconsigliata per i motivi seguenti:
>
> -   Questa omissione comporta codice non portabile, che potrebbe non funzionare su alcuni componenti hardware e non funziona sui rasterizzatori software che in genere eseguono thread in gruppi più piccoli.
> -   I miglioramenti delle prestazioni che è possibile ottenere con questa omissione saranno minori rispetto all'uso della barriera all-thread.

 

In Direct3D 10 non è presente alcuna sincronizzazione dei thread durante la scrittura in gruppi, pertanto ogni thread è limitato a una singola posizione in una matrice per la scrittura. Usare il [valore di sistema SV \_ GroupIndex](dx-graphics-hlsl-semantics.md) per indicizzare questa matrice durante la scrittura per assicurarsi che due thread non possano entrare in conflitto. In termini di lettura, tutti i thread hanno accesso all'intera matrice per la lettura.


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a>Imballaggio

Sottocomponenti di tipo pack di vettori e scalari le cui dimensioni sono sufficientemente grandi da impedire l'attraversamento dei limiti del registro. Ad esempio, sono tutti validi:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



Impossibile combinare i tipi di pacchetto.

Analogamente alla parola chiave register, packoffset può essere specifico della destinazione. La creazione di sottocomponenti è disponibile solo con la parola chiave packoffset, non con la parola chiave register. All'interno di una dichiarazione cbuffer, la parola chiave register viene ignorata per le destinazioni Direct3D 10 come si presuppone per la compatibilità multipiattaforma.

Gli elementi pack possono sovrapporsi e il compilatore non restituirà alcun errore o avviso. In questo esempio, Element2 ed Element3 si sovrappongono a Element1.x e Element1.y.


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



Un esempio che usa packoffset è: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Variabili (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

