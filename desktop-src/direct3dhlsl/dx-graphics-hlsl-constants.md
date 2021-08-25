---
title: Costanti dello shader (HLSL)
description: In Shader Model 4 le costanti shader vengono archiviate in una o più risorse del buffer in memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- constant buffer
- buffer di trama
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a6b2ffa9168e870aeb405badb6ff71b0a4a59b23d76947e56a9c085ed0107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726551"
---
# <a name="shader-constants-hlsl"></a>Costanti dello shader (HLSL)

In Shader Model 4 le costanti shader vengono archiviate in una o più risorse del buffer in memoria. Possono essere organizzati in due tipi di buffer: buffer costanti (cbuffer) e buffer di trama (tbuffer). I buffer costanti sono ottimizzati per l'utilizzo di variabili costanti, caratterizzato da un accesso a bassa latenza e da un aggiornamento più frequente dalla CPU. Per questo motivo, a queste risorse si applicano restrizioni aggiuntive per dimensioni, layout e accesso. I buffer di trama sono accessibili come trame e hanno prestazioni migliori per i dati indicizzati arbitrariamente. Indipendentemente dal tipo di risorsa in uso, non esiste alcun limite al numero di buffer costanti o di trame che un'applicazione può creare.

La dichiarazione di un buffer costante o di un buffer di trama è molto simile a una dichiarazione di struttura in C, con l'aggiunta delle parole chiave **register** e **packoffset** per l'assegnazione manuale di registri o la creazione di dati di pacchetto.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Nome* \] \[: **register**(b \# ) { \] *VariableDeclaration* \[ : **packoffset**(c \# .xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[in \] Tipo di buffer.



| BufferType | Descrizione     |
|------------|-----------------|
| cbuffer    | constant buffer |
| tbuffer    | buffer di trama  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

\[in \] Facoltativo, stringa ASCII contenente un nome di buffer univoco.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b \# )
</dt> <dd>

\[in \] Parola chiave Facoltativa, usata per inserire manualmente i dati costanti. Le costanti possono essere imballate in un registro solo in un buffer costante, in cui il registro iniziale viene fornito dal numero di registro ( *\#* ).

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[nella \] dichiarazione di variabile, simile a una dichiarazione di membro di struttura. Può trattarsi di qualsiasi tipo HLSL o oggetto effetto (ad eccezione di una trama o di un oggetto campionatore).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# .xyzw)
</dt> <dd>

\[in \] Parola chiave Facoltativa, usata per inserire manualmente i dati costanti. Le costanti possono essere imballate in qualsiasi buffer costante, in cui il numero di registro è specificato da ( *\#* ). L'impacchettamento dei componenti secondari (con xyzw swizzling) è disponibile per le costanti le cui dimensioni rientrano in un singolo registro (non attraversare un limite di registro). Ad esempio, non è stato possibile inserire un float4 in un singolo registro a partire dal componente y perché non rientra in un registro a quattro componenti.

</dd> </dl>

## <a name="remarks"></a>Commenti

I buffer costanti riducono la larghezza di banda necessaria per aggiornare le costanti shader consentendo il raggruppamento e il commit delle costanti shader contemporaneamente anziché effettuare singole chiamate per eseguire il commit di ogni costante separatamente.

Un buffer costante è una risorsa buffer specializzata a cui si accede come un buffer. Ogni buffer costante può contenere fino a 4096 [vettori](dx-graphics-hlsl-vector.md); ogni vettore contiene fino a quattro valori a 32 bit. È possibile associare fino a 14 buffer costanti per ogni fase della pipeline (2 slot aggiuntivi sono riservati per l'uso interno).

Un buffer di trama è una risorsa buffer specializzata a cui si accede come una trama. L'accesso alla trama (rispetto all'accesso al buffer) può avere prestazioni migliori per i dati indicizzati arbitrariamente. È possibile associare fino a 128 buffer di trama per ogni fase della pipeline.

Una risorsa buffer è progettata per ridurre al minimo il sovraccarico dell'impostazione delle costanti shader. Il framework degli effetti (vedere [**l'interfaccia ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gestirà l'aggiornamento dei buffer delle costanti e delle trame oppure è possibile usare l'API Direct3D per aggiornare i buffer (per informazioni, vedere Copia e accesso ai dati delle risorse [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) Un'applicazione può anche copiare dati da un altro buffer,ad esempio una destinazione di rendering o una destinazione di output di flusso, in un buffer costante.

Per altre informazioni sull'uso dei buffer costanti in un'applicazione D3D10, vedere Tipi di risorse [(Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e Creazione di risorse [buffer (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)

Per altre informazioni sull'uso dei buffer costanti in un'applicazione D3D11, vedere Introduzione ai [buffer in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) e [Procedura: Creare un buffer costante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)

Un buffer costante non richiede che [una vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) sia associata alla pipeline. Un buffer di trama, tuttavia, richiede una visualizzazione e deve essere associato a uno slot di trama (o deve essere associato a [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) quando si usa un effetto).

Esistono due modi per imballare i dati delle costanti: usando le parole chiave [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) e [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

Differenze tra Direct3D 9 e Direct3D 10 e 11:

- A differenza dell'allocazione automatica delle costanti in Direct3D 9, che non ha eseguito il packing e ha invece assegnato ogni variabile a un set di registri float4, le variabili costanti HLSL seguono le regole di packing in Direct3D 10 e 11.



 

### <a name="organizing-constant-buffers"></a>Organizzazione dei buffer costanti

I buffer costanti riducono la larghezza di banda necessaria per aggiornare le costanti shader consentendo il raggruppamento e il commit delle costanti shader contemporaneamente anziché effettuare singole chiamate per eseguire il commit di ogni costante separatamente.

Il modo migliore per usare in modo efficiente i buffer costanti consiste nell'organizzare le variabili dello shader in buffer costanti in base alla rispettiva frequenza di aggiornamento. Ciò consente a un'applicazione di ridurre al minimo la larghezza di banda necessaria per l'aggiornamento delle costanti shader. Ad esempio, uno shader potrebbe dichiarare due buffer costanti e organizzare i dati in ognuno in base alla frequenza di aggiornamento: i dati che devono essere aggiornati per ogni oggetto (ad esempio una matrice globale) vengono raggruppati in un buffer costante che può essere aggiornato per ogni oggetto. Questo è separato dai dati che caratterizzano una scena e pertanto è probabile che siano aggiornati molto meno spesso (quando la scena cambia).


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

Sono disponibili due buffer costanti predefiniti, $Global e $Param. Le variabili inserite nell'ambito globale vengono aggiunte in modo implicito al $Global cbuffer, usando lo stesso metodo di pacchetto usato per cbuffer. I parametri uniformi nell'elenco di parametri di una funzione vengono visualizzati nel buffer $Param costante quando uno shader viene compilato all'esterno del framework degli effetti. Quando vengono compilate all'interno del framework effetti, tutte le uniformi devono essere risolte in variabili definite nell'ambito globale.

## <a name="examples"></a>Esempio

Ecco un esempio di [Skinning10 Sample che](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) è un buffer di trama costituito da una matrice di matrici.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



Questa dichiarazione di esempio assegna manualmente un buffer costante per iniziare da un registro specifico e include anche elementi specifici in base ai sottocomponenti.


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

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

