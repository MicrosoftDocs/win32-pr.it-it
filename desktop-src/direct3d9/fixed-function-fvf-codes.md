---
description: Un codice FVF descrive il contenuto dei vertici archiviati con interfoliazione in un singolo flusso di dati.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Codici FVF della funzione fissa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303678"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Codici FVF della funzione fissa (Direct3D 9)

Un codice FVF descrive il contenuto dei vertici archiviati con interfoliazione in un singolo flusso di dati. In genere specifica i dati che devono essere elaborati dalla pipeline di elaborazione del vertice della funzione fissa. Si tratta di una dichiarazione di vertice di tipo precedente; per visualizzare lo stile di dichiarazione del vertice corrente, vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Le applicazioni Direct3D possono definire i vertici del modello in diversi modi. Il supporto per le definizioni dei vertici flessibili, noti anche come formati di vertici flessibili o codici di formato vertice flessibili, consente all'applicazione di usare solo i componenti Vertex necessari, eliminando i componenti che non vengono usati. Utilizzando solo i componenti Vertex necessari, l'applicazione può conservare la memoria e ridurre al minimo la larghezza di banda di elaborazione necessaria per il rendering dei modelli. Viene descritto il modo in cui i vertici vengono formattati utilizzando una combinazione di codici [D3DFVF](d3dfvf.md) .

La specifica FVF include i formati per le dimensioni dei punti, specificati da D3DFVF \_ PSIZE. Questa dimensione è espressa in unità di spazio della fotocamera per i vertici non trasformati e illuminati (TL) e in unità di spazio del dispositivo per i vertici TL.

I metodi di rendering dell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) forniscono applicazioni C++ con metodi che accettano una combinazione di questi flag e li usano per determinare come eseguire il rendering delle primitive. Fondamentalmente, questi flag indicano al sistema i componenti dei vertici, ovvero la posizione, i pesi di fusione dei vertici, le normali, i colori e il numero e il formato delle coordinate di trama. l'applicazione usa e, indirettamente, le parti della pipeline di rendering a cui si vuole applicare Direct3D. Inoltre, la presenza o l'assenza di un particolare flag di formato vertice comunica al sistema quali campi del componente Vertex sono presenti in memoria e che sono stati omessi.

Per determinare le limitazioni dei dispositivi, è possibile eseguire una query su un dispositivo per i valori di D3DFVFCAPS \_ DONOTSTRIPELEMENTS e D3DFVFCAPS \_ TEXCOORDCOUNTMASK nel membro FVFCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

Le coordinate di trama possono essere dichiarate in formati diversi, consentendo la ricerca di trame usando il numero di coordinate di una coordinata o di quattro coordinate di trama (per le coordinate di trama proiettate 2D). Per altre informazioni, vedere [formati di coordinate di trama (Direct3D 9)](texture-coordinate-formats.md). Usare il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) per creare modelli di bit che identifichino i formati di coordinate di trama usati dal formato del vertice.

Nessuna applicazione userà tutti i componenti. I campi uniformi W (RHW) e i normali vertici si escludono a vicenda. E la maggior parte delle applicazioni tentano di usare tutti e otto i set di coordinate di trama, ma Direct3D ha questa capacità. Esistono diverse restrizioni sui flag che è possibile usare con altri flag. Ad esempio, non è possibile usare \_ insieme i flag D3DFVF XYZ e D3DFVF \_ XYZRHW, in quanto ciò indicherebbe che l'applicazione sta descrivendo la posizione di un vertice con i vertici non trasformati e trasformati.

Per usare la combinazione di vertici indicizzati, \_ il \_ flag D3DFVF LASTBETA UBYTE4 dovrebbe essere visualizzato alla fine della dichiarazione FVF. La presenza di questo flag indica che il quinto peso di fusione verrà considerato come DWORD anziché come float. Per ulteriori informazioni, vedere la pagina relativa alla [fusione dei vertici indicizzati (Direct3D 9)](indexed-vertex-blending.md).

Gli esempi di codice seguenti illustrano la differenza tra un codice FVF che usa \_ il \_ flag D3DFVF LASTBETA UBYTE4 e uno che non lo è. Il flag D3DFVF \_ XYZB3 è presente quando vengono usati quattro indici di fusione perché si sottrae sempre la somma dei primi tre dal numero uno per ottenere il quarto (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).


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



Il FVF definito di seguito usa il \_ flag D3DFVF Last \_ UBYTE4.


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

[Dichiarazione vertici](vertex-declaration.md)
</dt> </dl>

 

 
