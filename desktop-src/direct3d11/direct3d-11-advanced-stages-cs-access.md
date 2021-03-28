---
title: Accesso alle risorse
description: Sono disponibili diversi modi per accedere alle risorse.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993496"
---
# <a name="accessing-resources"></a>Accesso alle risorse

Sono disponibili diversi modi per accedere alle [risorse](overviews-direct3d-11-resources-types.md). Indipendentemente da Direct3D, Direct3D garantisce che restituisca zero per tutte le risorse a cui si accede fuori limite.

-   [Accesso per offset di byte](#access-by-byte-offset)
-   [Accesso in base all'indice](#access-by-index)
-   [Accesso per metodo MIPS](#access-by-mips-method)
-   [Argomenti correlati](#related-topics)

## <a name="access-by-byte-offset"></a>Accesso per offset di byte

È possibile accedere a due nuovi tipi di buffer usando un offset di byte:

-   [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) è un buffer di sola lettura.
-   [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) è un buffer di lettura o scrittura.

## <a name="access-by-index"></a>Accesso in base all'indice

I tipi di risorse possono usare un indice per fare riferimento a una posizione specifica nella risorsa. Prendere in considerazione questo esempio:


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



Questo esempio Mostra come assegnare i 4 valori float archiviati in Texel che si trova nella posizione *pos* nella risorsa trama *2D texture alla variabile* *myvar* .

> [!Note]  
> Il valore predefinito per l'accesso a una trama in questo modo è mipmap livello zero (il livello più dettagliato).

 

> [!Note]  
> La riga "float4 myVar = texture \[ POS \] ;" è equivalente a "float4 myvar = texture. Load (uint3 (POS, 0));". L'accesso in base all'indice è un nuovo miglioramento della sintassi di HLSL.

 

> [!Note]  
> Il compilatore nella versione di giugno 2010 di DirectX SDK e versioni successive consente di indicizzare tutti i tipi di risorse ad eccezione dei [buffer degli indirizzi byte](direct3d-11-advanced-stages-cs-resources.md).

 

> [!Note]  
> Il compilatore di giugno 2010 e versioni successive consente di dichiarare le variabili di risorse locali. È possibile assegnare le risorse definite a livello globale (ad esempio, la *trama*) a queste variabili e usarle allo stesso modo delle rispettive controparti globali.

 

## <a name="access-by-mips-method"></a>Accesso per metodo MIPS

Gli oggetti texture hanno un metodo **MIPS** , ad esempio [**Texture2D. MIPS**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85)), che è possibile usare per specificare il livello mipmap. Questo esempio legge il colore archiviato in (7, 16) in mipmap livello 2 in una trama 2D:


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Si tratta di un miglioramento del compilatore di giugno 2010 e versioni successive. L'espressione "texture. MIPS \[ 2 \] \[ uint2 (x, y) \] " equivale a "texture. Load (uint3 (x, y, 2))".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica di Compute Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 