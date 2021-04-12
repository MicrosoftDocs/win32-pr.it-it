---
description: Descrive i tipi e le strutture della libreria DirectXMath.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: Strutture della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ac040ee932e9da84c186124514d9f763e20e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344496"
---
# <a name="directxmath-library-structures"></a>Strutture della libreria DirectXMath

Descrive i tipi e le strutture della libreria DirectXMath.

La libreria DirectXMath fornisce una serie di strutture e tipi definiti per incapsulare i dati per supportare semplicità di utilizzo, ottimizzazione e portabilità. Nell'elenco seguente sono incluse le strutture che fanno attualmente parte della libreria DirectXMath. Sono disponibili tramite DirectXMath. h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | Vettore 2D in cui ogni componente è un intero con segno, a 8 bit (1 byte) di lunghezza. |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Vettore 4D in cui ogni componente è un intero con segno, a 8 bit (1 byte) di lunghezza.  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Vettore 2D per l'archiviazione di valori normalizzati firmati come interi con segno a 8 bit (1 byte). |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Vettore 3D per l'archiviazione di valori normalizzati firmati come interi con segno a 8 bit (1 byte).  |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Vettore di colore alfa rosso verde (ARGB) a 32 bit, dove ogni canale di colore viene specificato come intero senza segno a 8 bit. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Vettore 4D con i componenti x, y e z rappresentati come valori interi con segno a 10 bit e il componente w come valore intero con segno a 2 bit.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Vettore 4D per l'archiviazione di valori con firma e normalizzati come componenti x-, y-e z-con segno a 10 bit e un w-Component con segno a 2 bit.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | Vettore 2D costituito da due valori a virgola mobile a precisione singola. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Descrive una struttura [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) allineata a un limite di 16 byte. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Descrive un vettore 3D costituito da tre valori a virgola mobile a precisione singola. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Descrive una struttura [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) allineata a un limite di 16 byte. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Descrive un vettore 3D con componenti X e Y archiviati come numero a virgola mobile a 11 bit e componente Z archiviato come valore a virgola mobile a 10 bit.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Descrive un vettore 3D di tre componenti a virgola mobile con mantisse a 9 bit, ognuno dei quali condivide lo stesso esponente a 5 bit.  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Matrice A virgola mobile 3x3. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | Matrice 3x4 colonna-Major contenente i componenti a virgola mobile a 32 bit. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | Matrice 3x4 colonna-Major contenente componenti a virgola mobile a 32 bit allineati su un limite di 16 byte. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Descrive un vettore 4D costituito da quattro valori a virgola mobile a precisione singola.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Descrive una struttura [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) allineata a un limite di 16 byte. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Matrice A virgola mobile 4x3. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Descrive una struttura [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) allineata a un limite di 16 byte. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Matrice A virgola mobile 4x4. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Descrive una struttura [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) allineata a un limite di 16 byte. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | Vettore 2D costituito da due valori a virgola mobile a metà precisione (16 bit).  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Descrive un vettore 4D costituito da quattro valori a virgola mobile a metà precisione (a 16 bit).  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | Vettore 2D in cui ogni componente è un intero con segno. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Vettore 3D in cui ogni componente è un intero con segno. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Vettore 4D in cui ogni componente è un intero con segno. |
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Descrive una matrice 4x4 allineata a un limite di 16 byte che esegue il mapping a quattro registri vettoriali hardware. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Descrive un vettore 2D costituito da componenti interi con segno a 16 bit e normalizzati.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Vettore 4D costituito da componenti interi con segno a 16 bit.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Vettore 2D per l'archiviazione di valori normalizzati firmati come interi con segno a 16 bit (tipo `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Vettore 4D per l'archiviazione di valori normalizzati firmati come interi con segno a 16 bit, (tipo `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Vettore 4D con i componenti x-, y-e z rappresentati come valori Unsigned Integer a 5 bit e il componente w come valore intero a 1 bit.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Vettore 3D con componenti x e z rappresentati come valori Unsigned Integer a 5 bit e il componente y come valore Unsigned Integer a 6 bit. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Descrive un vettore 2D in cui ogni componente è un Unsigned Integer, a 8 bit (1 byte) di lunghezza. |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Descrive un vettore 4D in cui ogni componente è una Unsigned Integer, a 8 bit (1 byte) di lunghezza.  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Vettore 2D per l'archiviazione di valori normalizzati senza segno come interi con segno a 8 bit (1 byte). |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Vettore 3D per l'archiviazione di valori normalizzati senza segno come interi con segno a 8 bit (1 byte).  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Vettore 4D con i componenti x-, y-e z rappresentati come valori di Unsigned Integer a 10 bit e il componente w come valore di Unsigned Integer a 2 bit.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Vettore 4D per l'archiviazione di valori interi non firmati e normalizzati come componenti x, y e z senza segno a 10 bit e un w-Component senza segno a 2 bit.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | Vettore 2D in cui ogni componente è un Unsigned Integer. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Vettore 3D in cui ogni componente è un Unsigned Integer. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Vettore 4D in cui ogni componente è un Unsigned Integer. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Vettore 4D con quattro componenti interi senza segno a 4 bit.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Descrive un vettore 2D costituito da componenti Unsigned Integer a 16 bit.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Vettore 4D costituito da componenti Unsigned Integer a 16 bit.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Vettore 2D per l'archiviazione di valori normalizzati senza segno come interi senza segno a 16 bit, (tipo `uint16_t` ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Vettore 4D per l'archiviazione di valori normalizzati senza segno come interi con segno a 16 bit (tipo `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Vettore 4D con i componenti x, y e z rappresentati come valori interi con segno a 10 bit e il componente w come valore di Unsigned Integer a 2 bit.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Vettore 4D per l'archiviazione di valori con firma e normalizzati come componenti x-, y-e z-signed a 10 bit e un valore non firmato e normalizzato come un componente w senza segno a 2 bit.  |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>
