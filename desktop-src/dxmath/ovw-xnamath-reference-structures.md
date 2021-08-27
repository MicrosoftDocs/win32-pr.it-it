---
description: Descrive i tipi e le strutture della libreria DirectXMath.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: Strutture della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce40aeb51c04f0b5ab76f20b83e2825c33e261862ab3205490aaab855ddb4ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117511"
---
# <a name="directxmath-library-structures"></a>Strutture della libreria DirectXMath

Descrive i tipi e le strutture della libreria DirectXMath.

La libreria DirectXMath fornisce una serie di strutture e tipi definiti per incapsulare i dati per supportare facilità d'uso, ottimizzazione e portabilità. L'elenco seguente include le strutture attualmente incluse nella libreria DirectXMath. Sono disponibili tramite DirectXMath.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | Vettore 2D in cui ogni componente è un intero con segno di lunghezza di 8 bit (1 byte). |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Vettore 4D in cui ogni componente è un intero con segno con lunghezza di 8 bit (1 byte).  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Vettore 2D per l'archiviazione di valori normalizzati con segno come interi con segno a 8 bit (1 byte). |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Vettore 3D per l'archiviazione di valori normalizzati con segno come interi con segno a 8 bit (1 byte).  |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Vettore di colore ARGB (Alpha Red Green Blue) a 32 bit, in cui ogni canale di colore viene specificato come intero senza segno a 8 bit. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Vettore 4D con componenti x-, y-e z- rappresentati come valori interi con segno a 10 bit e il componente w come valore intero con segno a 2 bit.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Vettore 4D per l'archiviazione di valori normalizzati con segno come componenti x-, y- e z- con segno a 10 bit e un componente w con segno a 2 bit.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | Vettore 2D costituito da due valori a virgola mobile e precisione singola. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Descrive una [**struttura XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) allineata su un limite di 16 byte. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Descrive un vettore 3D costituito da tre valori a virgola mobile e precisione singola. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Descrive una [**struttura XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) allineata su un limite di 16 byte. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Descrive un vettore 3D con componenti X e Y archiviati come numero a virgola mobile a 11 bit e componente Z archiviato come valore a virgola mobile a 10 bit.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Descrive un vettore 3D di tre componenti a virgola mobile con mantissa a 9 bit, ognuno dei quali condivide lo stesso esponente a 5 bit.  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Matrice a virgola mobile 3x3. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | Matrice principale di colonna 3x4 contenente componenti a virgola mobile a 32 bit. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | Matrice principale di colonna 3x4 contenente componenti a virgola mobile a 32 bit allineati su un limite di 16 byte. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Descrive un vettore 4D costituito da quattro valori a virgola mobile e precisione singola.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Descrive una [**struttura XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) allineata su un limite di 16 byte. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Matrice a virgola mobile 4x3. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Descrive una [**struttura XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) allineata su un limite di 16 byte. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Matrice a virgola mobile 4x4. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Descrive una [**struttura XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) allineata su un limite di 16 byte. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | Vettore 2D costituito da due valori a virgola mobile a mezza precisione (16 bit).  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Descrive un vettore 4D costituito da quattro valori a virgola mobile a mezza precisione (16 bit).  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | Vettore 2D in cui ogni componente è un intero con segno. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Vettore 3D in cui ogni componente è un intero con segno. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Vettore 4D in cui ogni componente è un intero con segno. |
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Descrive una matrice 4x4 allineata su un limite di 16 byte che esegue il mapping a quattro registri vettoriali hardware. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Descrive un vettore 2D costituito da componenti integer con segno a 16 bit e normalizzati.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Vettore 4D costituito da componenti integer con segno a 16 bit.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Vettore 2D per l'archiviazione di valori normalizzati con segno come interi con segno a 16 bit (tipo `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Vettore 4D per l'archiviazione di valori normalizzati con segno come interi con segno a 16 bit (tipo `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Vettore 4D con componenti x-, y-e z- rappresentati come valori interi senza segno a 5 bit e componente w come valore intero a 1 bit.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Vettore 3D con componenti x e z- rappresentati come valori interi senza segno a 5 bit e componente y come valore intero senza segno a 6 bit. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Descrive un vettore 2D in cui ogni componente è un intero senza segno con lunghezza di 8 bit (1 byte). |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Descrive un vettore 4D in cui ogni componente è un intero senza segno con lunghezza di 8 bit (1 byte).  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Vettore 2D per l'archiviazione di valori normalizzati senza segno come interi con segno a 8 bit (1 byte). |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Vettore 3D per l'archiviazione di valori normalizzati senza segno come interi con segno a 8 bit (1 byte).  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Vettore 4D con componenti x-, y-e z- rappresentati come valori interi senza segno a 10 bit e componente w come valore intero senza segno a 2 bit.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Vettore 4D per l'archiviazione di valori integer senza segno e normalizzati come componenti x, y e z senza segno a 10 bit e un componente w senza segno a 2 bit.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | Vettore 2D in cui ogni componente è un intero senza segno. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Vettore 3D in cui ogni componente è un intero senza segno. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Vettore 4D in cui ogni componente è un intero senza segno. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Vettore 4D con quattro componenti integer senza segno a 4 bit.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Descrive un vettore 2D costituito da componenti unsigned integer a 16 bit.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Vettore 4D costituito da componenti interi senza segno a 16 bit.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Vettore 2D per l'archiviazione di valori normalizzati senza segno come interi senza segno a 16 bit (tipo `uint16_t` ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Vettore 4D per l'archiviazione di valori normalizzati senza segno come interi a 16 bit con segno (tipo `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Vettore 4D con componenti x-, y-e z- rappresentati come valori interi con segno a 10 bit e il componente w come valore intero senza segno a 2 bit.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Vettore 4D per l'archiviazione di valori normalizzati con segno come componenti x,y e z con segno a 10 bit e un valore normalizzato senza segno come w-component senza segno a 2 bit.  |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla programmazione DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>
