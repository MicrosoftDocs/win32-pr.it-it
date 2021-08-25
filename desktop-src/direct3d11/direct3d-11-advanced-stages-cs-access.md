---
title: Accesso alle risorse
description: Esistono diversi modi per accedere alle risorse.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b66ae5ad0f3a49f51281d12ba5e3c2c52cd822aadd5097485b571533ae1a04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677171"
---
# <a name="accessing-resources"></a>Accesso alle risorse

Esistono diversi modi per accedere alle [risorse](overviews-direct3d-11-resources-types.md). Indipendentemente dal fatto che Direct3D restituirà zero per qualsiasi risorsa a cui si accede fuori dai limiti.

-   [Accesso in base all'offset dei byte](#access-by-byte-offset)
-   [Accesso in base all'indice](#access-by-index)
-   [Metodo Access By Mips](#access-by-mips-method)
-   [Argomenti correlati](#related-topics)

## <a name="access-by-byte-offset"></a>Accesso in base all'offset dei byte

È possibile accedere a due nuovi tipi di buffer usando un offset di byte:

-   [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) è un buffer di sola lettura.
-   [**RWByteAddressBuffer è**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) un buffer di lettura o scrittura.

## <a name="access-by-index"></a>Accesso in base all'indice

I tipi di risorse possono usare un indice per fare riferimento a una posizione specifica nella risorsa. Prendere in considerazione questo esempio:


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



Questo esempio assegna i 4 valori float archiviati in corrispondenza del texel situato nella posizione *pos* nella risorsa *trama 2D myTexture* alla *variabile myVar.*

> [!Note]  
> L'impostazione predefinita per l'accesso a una trama in questo modo è il livello mipmap zero (il livello più dettagliato).

 

> [!Note]  
> La riga "float4 myVar = myTexture pos ;" equivale a \[ \] "float4 myVar = myTexture.Load(uint3(pos,0));". L'accesso in base all'indice è un nuovo miglioramento della sintassi HLSL.

 

> [!Note]  
> Il compilatore nella versione di giugno 2010 di DirectX SDK e versioni successive consente di indicizzare tutti i tipi di risorse ad eccezione dei [buffer di indirizzi byte.](direct3d-11-advanced-stages-cs-resources.md)

 

> [!Note]  
> Il compilatore di giugno 2010 e versioni successive consente di dichiarare variabili di risorse locali. È possibile assegnare a queste variabili risorse definite a livello globale (ad esempio *myTexture)* e usarle allo stesso modo delle controparti globali.

 

## <a name="access-by-mips-method"></a>Metodo Access By Mips

Gli oggetti texture hanno un metodo **mips** (ad [**esempio, Texture2D.mips),**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))che è possibile usare per specificare il livello mipmap. Questo esempio legge il colore archiviato in (7,16) nel livello mipmap 2 in una trama 2D:


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Si tratta di un miglioramento del compilatore di giugno 2010 e versioni successive. L'espressione "myTexture.mips \[ 2 \] \[ uint2(x,y) " equivale a \] "myTexture.Load(uint3(x,y,2))".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sul compute shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 