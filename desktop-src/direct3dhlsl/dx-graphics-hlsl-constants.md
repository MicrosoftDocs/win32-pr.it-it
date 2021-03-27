---
title: Costanti dello shader (HLSL)
description: Nel modello di Shader 4, le costanti dello shader vengono archiviate in una o più risorse del buffer in memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- buffer costante
- buffer trama
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739431"
---
# <a name="shader-constants-hlsl"></a>Costanti dello shader (HLSL)

Nel modello di Shader 4, le costanti dello shader vengono archiviate in una o più risorse del buffer in memoria. Possono essere organizzati in due tipi di buffer: buffer costanti (cBuffers) e buffer di trama (tbuffers). I buffer costanti sono ottimizzati per l'utilizzo costante-variabile, caratterizzato dall'accesso con latenza inferiore e dall'aggiornamento più frequente dalla CPU. Per questo motivo, per queste risorse si applicano le restrizioni aggiuntive relative a dimensioni, layout e accesso. I buffer di trama sono accessibili come le trame ed eseguono le prestazioni migliori per i dati indicizzati in modo arbitrario. Indipendentemente dal tipo di risorsa in uso, non esiste alcun limite al numero di buffer costanti o di buffer di trama che un'applicazione può creare.

La dichiarazione di un buffer costante o di un buffer di trama ha un aspetto molto simile a una dichiarazione di struttura in C, con l'aggiunta delle parole chiave **Register** e **packoffset** per l'assegnazione manuale di registri o di pacchetti di dati.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Nome* \] \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[nel \] tipo di buffer.



| BufferType | Descrizione     |
|------------|-----------------|
| cbuffer    | buffer costante |
| tbuffer    | buffer trama  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

\[in \] una stringa ASCII facoltativa contenente un nome di buffer univoco.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**registra**(b \# )
</dt> <dd>

\[nella \] parola chiave Optional utilizzata per inserire manualmente i dati costanti. Le costanti possono essere compresse in un registro solo in un buffer costante, dove il registro iniziale viene fornito dal numero di registro ( *\#* ).

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[nella \] dichiarazione di variabile, simile a una dichiarazione di membro di struttura. Può trattarsi di qualsiasi tipo di HLSL o oggetto effetto (ad eccezione di una trama o di un oggetto campionatore).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)
</dt> <dd>

\[nella \] parola chiave Optional utilizzata per inserire manualmente i dati costanti. Le costanti possono essere compresse in qualsiasi buffer costante, in cui il numero di registro è fornito da ( *\#* ). La compressione dei componenti secondari (usando xyzw swizzling) è disponibile per le costanti le cui dimensioni rientrano in un unico registro (non superare un limite di registro). Ad esempio, un float4 non può essere compresso in un unico registro che inizia con il componente y, perché non si adatterebbe a un registro a quattro componenti.

</dd> </dl>

## <a name="remarks"></a>Commenti

I buffer costanti consentono di ridurre la larghezza di banda necessaria per aggiornare le costanti dello shader consentendo il raggruppamento e il commit delle costanti dello shader, anziché eseguire chiamate singole per eseguire il commit di ogni costante separatamente.

Un buffer costante è una risorsa di buffer specializzata a cui si accede come un buffer. Ogni buffer costante può avere fino a 4096 [vettori](dx-graphics-hlsl-vector.md); ogni vettore contiene valori fino a 4 32 bit. È possibile associare fino a 14 buffer costanti per fase della pipeline. 2 slot aggiuntivi sono riservati per uso interno.

Un buffer di trama è una risorsa di buffer specializzata a cui si accede come una trama. L'accesso alla trama (rispetto all'accesso al buffer) può migliorare le prestazioni per i dati indicizzati in modo arbitrario. È possibile associare fino a 128 buffer di trama per fase della pipeline.

Una risorsa di buffer è progettata per ridurre al minimo l'overhead dovuto all'impostazione delle costanti dello shader. Il Framework degli effetti (vedere [**interfaccia ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gestirà l'aggiornamento dei buffer di trama e costanti, oppure è possibile usare l'API Direct3D per aggiornare i buffer. per informazioni, vedere [copia e accesso ai dati delle risorse (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) . Un'applicazione può anche copiare dati da un altro buffer, ad esempio una destinazione di rendering o una destinazione di output di flusso, in un buffer costante.

Per altre informazioni sull'uso di buffer costanti in un'applicazione D3D10, vedere [tipi di risorse (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e [creazione di risorse di buffer (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).

Per informazioni su Morel sull'uso di buffer costanti in un'applicazione D3D11, vedere [Introduzione ai buffer in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) e [procedura: creare un buffer costante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Un buffer costante non richiede l'associazione di una [vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) alla pipeline. Un buffer di trama, tuttavia, richiede una visualizzazione e deve essere associato a uno slot di trama (oppure deve essere associato a [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) quando si utilizza un effetto).

Esistono due modi per comprimere i dati delle costanti: usando le parole chiave [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) e [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10 e 11:<br/> A differenza dell'allocazione automatica di costanti in Direct3D 9, che non hanno eseguito la compressione e assegnavano invece ogni variabile a un set di registri float4, le variabili costanti HLSL seguono le regole di compressione in Direct3D 10 e 11.<br/> |



 

### <a name="organizing-constant-buffers"></a>Organizzazione dei buffer costanti

I buffer costanti consentono di ridurre la larghezza di banda necessaria per aggiornare le costanti dello shader consentendo il raggruppamento e il commit delle costanti dello shader, anziché eseguire chiamate singole per eseguire il commit di ogni costante separatamente.

Il modo migliore per usare in modo efficiente i buffer costanti consiste nell'organizzare le variabili dello shader in buffer costanti in base alla rispettiva frequenza di aggiornamento. Questo consente a un'applicazione di ridurre al minimo la larghezza di banda necessaria per l'aggiornamento delle costanti dello shader. Uno shader, ad esempio, può dichiarare due buffer costanti e organizzare i dati in ognuno in base alla relativa frequenza di aggiornamento: i dati che devono essere aggiornati in base all'oggetto, ad esempio una matrice globale, vengono raggruppati in un buffer costante che può essere aggiornato per ogni oggetto. Questo è separato dai dati che caratterizzano una scena ed è quindi probabile che vengano aggiornati molto meno spesso (quando cambia la scena).


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a>Buffer costanti predefiniti

Sono disponibili due buffer costanti predefiniti, $Global e $Param. Le variabili inserite nell'ambito globale vengono aggiunte in modo implicito alla $Global cbuffer, usando lo stesso metodo di compressione usato per cBuffers. I parametri uniformi nell'elenco di parametri di una funzione vengono visualizzati nel buffer costante $Param quando uno shader viene compilato all'esterno del Framework effetti. Quando vengono compilati all'interno del Framework degli effetti, tutte le uniformi devono essere risolte in variabili definite nell'ambito globale.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio dell' [esempio Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) che rappresenta un buffer di trama costituito da una matrice di matrici.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



In questa dichiarazione di esempio viene assegnata manualmente un buffer costante per iniziare a un particolare registro e vengono inoltre inseriti elementi specifici in base ai sottocomponenti.


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

