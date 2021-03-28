---
title: Sintassi delle variabili
description: Usare le regole di sintassi seguenti per dichiarare le variabili HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintassi variabile (DirectX HLSL)
- interpolazione, sintassi variabile (DirectX HLSL)
- Sintassi condivisa, variabile (DirectX HLSL)
- groupshared, sintassi variabile (DirectX HLSL)
- static, sintassi variabile (DirectX HLSL)
- Uniform, sintassi variabile (DirectX HLSL)
- Sintassi volatile, Variable (DirectX HLSL)
- Sintassi precisa, variabile (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "104993645"
---
# <a name="variable-syntax"></a>Sintassi delle variabili

Usare le regole di sintassi seguenti per dichiarare le variabili HLSL.



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Archiviazione \_* \] \[ *\_ Modificatore tipo* di classe \] *nome tipo* \[ *index* \] \[ *: Semantic* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[ *Annotazioni* \] \[ *= Iniziale \_ Valore* di                    \] |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Classe di archiviazione \_* 
</dt> <dd>

Modificatori della classe di archiviazione facoltativi che forniscono gli hint del compilatore sull'ambito e sulla durata delle variabili; i modificatori possono essere specificati in qualsiasi ordine.



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
<td>Contrassegna una variabile globale come input esterno per lo shader; si tratta del contrassegno predefinito per tutte le variabili globali. Non può essere combinato con <strong>static</strong>.</td>
</tr>
<tr class="even">
<td><strong>interpolazione</strong></td>
<td>Non interpolare gli output di un vertex shader prima di passarli a un pixel shader.</td>
</tr>
<tr class="odd">
<td><strong>preciso</strong></td>
<td>La parola chiave <strong>precisa</strong> quando viene applicata a una variabile limita tutti i calcoli utilizzati per produrre il valore assegnato a tale variabile nei modi seguenti:

*   Le operazioni separate vengono mantenute separate. Se, ad esempio, un'operazione MUL e Add potrebbe essere stata fusa in un'operazione MAD <strong>, impone</strong> che le operazioni rimangano separate. È invece necessario usare in modo esplicito la funzione intrinseca MAD.
*   L'ordine delle operazioni viene mantenuto. Se è possibile che l'ordine delle istruzioni sia stato mischiato per migliorare le prestazioni, <strong>precisa</strong> garantisce che il compilatore mantenga l'ordine come scritto.
*   Le operazioni non sicure IEEE sono limitate. Quando il compilatore potrebbe avere utilizzato operazioni matematiche veloci che non considerano i valori NaN (non un numero) e INF (infinito), <strong>precisamente</strong> impone che i requisiti IEEE relativi ai valori NaN e inf siano rispettati. Senza alcuna <strong>precisione</strong>, queste ottimizzazioni e operazioni matematiche non sono sicure IEEE.
*   Se si qualifica una variabile <strong>precisa</strong> , le operazioni che usano la variabile sono <strong>precise</strong>. Dato che la <strong>precisione</strong> viene propagata solo alle operazioni che contribuiscono ai valori assegnati alla variabile qualificata <strong>precisa</strong>, l'esecuzione corretta dei <strong>calcoli</strong> desiderati può risultare complessa, quindi è consigliabile contrassegnare gli output dello shader in modo <strong>preciso</strong> direttamente dove vengono dichiarati, sia che si trovino in un campo della struttura, che in un parametro di output o il tipo restituito della funzione entry.

La possibilità di controllare le ottimizzazioni in questo modo mantiene l'invarianza dei risultati per la variabile di output modificata disabilitando le ottimizzazioni che potrebbero influire sui risultati finali a causa delle differenze nelle differenze di precisione accumulate. È utile quando si desidera che gli shader per lo schema a mosaico mantengano le cuciture delle patch con l'acqua o i valori di profondità corrispondenti a più passaggi.

[Codice di esempio](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl): 
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
<td>Contrassegnare una variabile per la condivisione tra gli effetti; si tratta di un suggerimento per il compilatore.</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>Contrassegnare una variabile per la memoria condivisa del gruppo di thread per i compute shader. In D3D10 la dimensione totale massima di tutte le variabili con la classe di archiviazione groupshared è 16KB, in D3D11 la dimensione massima è 32 KB. Vedere gli esempi.</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>Contrassegnare una variabile locale in modo che venga inizializzata una sola volta e venga mantenute tra le chiamate di funzione. Se la dichiarazione non include un inizializzatore, il valore viene impostato su zero. Una variabile globale contrassegnata come <strong>statica</strong> non è visibile per un'applicazione.</td>
</tr>
<tr class="odd">
<td><strong>Uniform</strong></td>
<td>Contrassegnare una variabile i cui dati sono costanti durante l'esecuzione di uno shader, ad esempio un colore del materiale in un vertex shader. per impostazione predefinita, le variabili globali sono considerate <strong>uniformi</strong> .</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>Contrassegna una variabile che cambia di frequente; si tratta di un suggerimento per il compilatore. Questo modificatore di classe di archiviazione si applica solo a una variabile locale.<br/>
<blockquote>
[!Note]<br />
Il compilatore HLSL attualmente ignora questo modificatore di classe di archiviazione.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificatore di tipo*
</dt> <dd>

Modificatore di tipo variabile facoltativo.



| Valore             | Descrizione                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Contrassegnare una variabile che non può essere modificata da uno shader, pertanto deve essere inizializzata nella dichiarazione di variabile. Le variabili globali sono considerate **const** per impostazione predefinita (Elimina questo comportamento fornendo il flag/GEC al compilatore). |
| **riga \_ principale**    | Contrassegnare una variabile che archivia quattro componenti in una singola riga in modo che possano essere archiviati in un unico registro costante.                                                                                                                             |
| **colonna \_ principale** | Contrassegnare una variabile che archivia 4 componenti in una singola colonna per ottimizzare la matematica della matrice.                                                                                                                                                         |



 

> [!Note]  
> Se non si specifica un valore del modificatore di tipo, il compilatore usa la **colonna \_ Major** come valore predefinito.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Qualsiasi tipo di HLSL elencato in [tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md).

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nome* \[ *Indice* di\]
</dt> <dd>

Stringa ASCII che identifica in modo univoco una variabile shader. Per definire una matrice facoltativa, usare **index** per la dimensione della matrice, ovvero un numero intero positivo = 1.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantica*
</dt> <dd>

Informazioni facoltative sull'utilizzo dei parametri, utilizzate dal compilatore per collegare gli input e gli output dello shader. Per gli shader Vertex e pixel sono disponibili diverse [semantiche](dx-graphics-hlsl-semantics.md) predefinite. Il compilatore ignora la semantica a meno che non vengano dichiarate in una variabile globale o un parametro passato a uno shader.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Parola chiave facoltativa per la compressione manuale delle costanti shader. Vedere [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registro*
</dt> <dd>

Parola chiave facoltativa per l'assegnazione manuale di una variabile shader a un particolare registro. Vedere [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotazioni*
</dt> <dd>

Metadati facoltativi, sotto forma di stringa, collegati a una variabile globale. Un'annotazione viene utilizzata dal framework degli effetti e ignorata da HLSL; per visualizzare una sintassi più dettagliata, vedere [sintassi dell'annotazione](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valore iniziale*
</dt> <dd>

Valore iniziale facoltativo/i. il numero di valori deve corrispondere al numero di componenti nel *tipo*. Ogni variabile globale contrassegnata come **extern** deve essere inizializzata con un valore letterale. ogni variabile contrassegnata come **statica** deve essere inizializzata con una costante.

Le variabili globali non contrassegnate come **static** o **extern** non vengono compilate nello shader. Il compilatore non imposta automaticamente i valori predefiniti per le variabili globali e non può usarli nelle ottimizzazioni. Per inizializzare questo tipo di variabile globale, utilizzare la reflection per ottenere il relativo valore e quindi copiare il valore in un buffer costante. Ad esempio, è possibile usare il metodo [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) per ottenere la variabile, usare il metodo [**ID3D11ShaderReflectionVariable:: getdesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) per ottenere la descrizione della variabile shader e ottenere il valore iniziale dal membro **DefaultValue** della struttura [**\_ \_ \_ desc della variabile di d3d11 shader**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) . Per copiare il valore nel buffer costante, è necessario assicurarsi che il buffer sia stato creato con accesso in scrittura alla CPU ([**\_ \_ \_ scrittura di accesso alla CPU d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)). Per altre informazioni su come creare un buffer costante, vedere [procedura: creare un buffer costante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

È anche possibile usare il [Framework degli effetti](../direct3d11/d3d11-graphics-programming-guide-effects.md) per elaborare automaticamente la reflection e impostare il valore iniziale. Ad esempio, è possibile usare il metodo [**ID3DX11EffectPass:: Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .

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

HLSL consente ai thread di un compute shader di scambiare valori tramite memoria condivisa. HLSL fornisce le primitive di barriera, ad esempio [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), e così via, per garantire l'ordinamento corretto delle letture e scritture nella memoria condivisa nello shader ed evitare le gare di dati.

> [!Note]  
> L'hardware esegue thread in gruppi (distorsioni o front-end) e la sincronizzazione delle barriere può talvolta essere omessa per migliorare le prestazioni quando solo la sincronizzazione di thread appartenenti allo stesso gruppo è corretta. Questa omissione viene tuttavia sconsigliata per i motivi seguenti:
>
> -   Questa omissione genera codice non portabile, che potrebbe non funzionare su hardware e non funziona in rasterizzatori software che in genere eseguono i thread in gruppi più piccoli.
> -   I miglioramenti delle prestazioni che è possibile ottenere con questa omissione saranno minori rispetto all'uso della barriera all-thread.

 

In Direct3D 10 non viene sincronizzato alcun thread durante la scrittura in **groupshared**, quindi questo significa che ogni thread è limitato a una singola posizione in una matrice per la scrittura. Usare il valore del sistema [SV \_ groupIndex](dx-graphics-hlsl-semantics.md) per eseguire l'indicizzazione in questa matrice durante la scrittura per assicurarsi che non ci siano due thread in conflitto. In termini di lettura, tutti i thread hanno accesso all'intera matrice per la lettura.


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



### <a name="packing"></a>Compressione

Comprimere i sottocomponenti di vettori e scalari la cui dimensione è sufficientemente grande da impedire i limiti del registro di attraversamento. Ad esempio, sono tutti validi:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



Impossibile combinare tipi di compressione.

Analogamente alla parola chiave register, un packoffset può essere specifico della destinazione. La compressione dei sottocomponenti è disponibile solo con la parola chiave packoffset, non con la parola chiave register. All'interno di una dichiarazione cbuffer, la parola chiave register viene ignorata per le destinazioni Direct3D 10, perché si presuppone che sia per la compatibilità multipiattaforma.

Gli elementi compressi possono sovrapporsi e il compilatore non restituirà alcun errore o avviso. In questo esempio, element2 e Element3 si sovrappongono con element1. x e element1. y.


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

 

