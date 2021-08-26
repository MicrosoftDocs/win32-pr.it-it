---
description: Un codice FVF descrive il contenuto dei vertici archiviati interleaved in un singolo flusso di dati.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Codici FVF delle funzioni fisse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4fb691192fcc4dbd7dc42c4d6c00829c209f87f68ec32ea42f6c26ff4663c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069191"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Codici FVF delle funzioni fisse (Direct3D 9)

Un codice FVF descrive il contenuto dei vertici archiviati interleaved in un singolo flusso di dati. In genere specifica i dati che devono essere elaborati dalla pipeline di elaborazione dei vertici di funzione fissa. Si tratta di una dichiarazione di vertice di tipo precedente. per visualizzare lo stile di dichiarazione del vertice corrente, vedere [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

Le applicazioni Direct3D possono definire vertici del modello in diversi modi. Il supporto per le definizioni dei vertici flessibili, noti anche come formati di vertice flessibili o codici di formato dei vertici flessibili, consente all'applicazione di usare solo i componenti dei vertici necessari, eliminando i componenti che non vengono usati. Usando solo i componenti dei vertici necessari, l'applicazione può risparmiare memoria e ridurre al minimo la larghezza di banda di elaborazione necessaria per il rendering dei modelli. Viene descritto come vengono formattati i vertici usando una combinazione [di codici D3DFVF.](d3dfvf.md)

La specifica FVF include i formati per le dimensioni dei punti, specificati da D3DFVF \_ PSIZE. Queste dimensioni sono espresse in unità di spazio della fotocamera per i vertici non trasformati e accesi (TL) e in unità di spazio del dispositivo per i vertici TL.

I metodi di rendering [**dell'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) forniscono alle applicazioni C++ metodi che accettano una combinazione di questi flag e li usano per determinare come eseguire il rendering delle primitive. Fondamentalmente, questi flag indicano al sistema quali componenti dei vertici, ovvero posizione, pesi di fusione dei vertici, normali, colori e numero e formato delle coordinate di trama, l'applicazione usa e, indirettamente, quali parti della pipeline di rendering si vuole applicare a Direct3D. Inoltre, la presenza o l'assenza di un particolare flag di formato vertice comunica al sistema quali campi del componente vertice sono presenti in memoria e quali sono stati omessi.

Per determinare le limitazioni del dispositivo, è possibile eseguire una query su un dispositivo per i valori di D3DFVFCAPS \_ DONOTSTRIPELEMENTS e D3DFVFCAPS \_ TEXCOORDCOUNTMASK nel membro FVFCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

Le coordinate della trama possono essere dichiarate in formati diversi, consentendo l'indirizzamento delle trame usando solo una coordinata o fino a quattro coordinate di trama (per le coordinate di trama proiettate 2D). Per altre informazioni, vedere [Formati delle coordinate di trama (Direct3D 9).](texture-coordinate-formats.md) Usare il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) per creare modelli di bit che identificano i formati delle coordinate di trama utilizzati dal formato vertice.

Nessuna applicazione userà ogni componente. I campi W (RHW) e normali vertici reciproci si escludono a vicenda. Né la maggior parte delle applicazioni tenterà di usare tutti gli otto set di coordinate di trama, ma Direct3D ha questa capacità. Esistono diverse restrizioni sui flag che è possibile usare con altri flag. Ad esempio, non è possibile usare insieme i flag D3DFVF \_ XYZ e D3DFVF XYZRHW, perché ciò indica che l'applicazione descrive la posizione di un vertice con vertici sia non trasformati che \_ trasformati.

Per usare la fusione dei vertici indicizzata, il flag D3DFVF LASTBETA UBYTE4 deve essere visualizzato alla fine della \_ \_ dichiarazione FVF. La presenza di questo flag indica che il quinto spessore di fusione verrà considerato come un valore DWORD anziché come float. Per altre informazioni, vedere [Indexed Vertex Blending (Direct3D 9) (Blending vertici indicizzati (Direct3D 9)](indexed-vertex-blending.md)).

Gli esempi di codice seguenti illustrano la differenza tra un codice FVF che usa il flag D3DFVF \_ LASTBETA UBYTE4 e uno \_ che non lo usa. Il flag D3DFVF XYZB3 è presente quando vengono usati quattro indici di fusione perché si sottrae sempre la somma dei primi tre dal numero uno per ottenere il quarto \_ (blend₄ = 1 - (blend₁ + blend BLEND + blend₃)).


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



Il file FVF definito di seguito usa il flag D3DFVF \_ LAST \_ UBYTE4.


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione dei vertici](vertex-declaration.md)
</dt> </dl>

 

 
