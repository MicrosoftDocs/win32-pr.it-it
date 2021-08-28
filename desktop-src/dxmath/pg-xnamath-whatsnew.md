---
description: La libreria DirectXMath è basata sulla libreria SIMD XNA Math C++ versione 2.x. Di seguito viene descritto in che modo DirectXMath differisce da XNA Math e come differiscono le versioni di DirectXMath.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novità (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e94d4ba2433501fb5389b82dab4f5c3de4b8ed80904ed4629729537bbf264a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984711"
---
# <a name="whats-new-directxmath"></a>Novità (DirectXMath)

La libreria DirectXMath è basata sulla libreria [SIMD XNA Math C++ versione 2.04.](https://walbourn.github.io/xna-math-version-2-04/) Di seguito viene descritto in che modo DirectXMath differisce da XNA Math e come differiscono le versioni di DirectXMath.

-   [Cronologia di Rlease](#release-history)
-   [Differenze di DirectXMath rispetto a XNA Math](#directxmath-differences-from-xna-math)
-   [Argomenti correlati](#related-topics)

## <a name="release-history"></a>Cronologia delle versioni

<table>
 <tr>
  <td>Windows 10 SDK (20348), versione 2104</td><td>DirectXMath 3.16</td>
 </td>
 <tr>
  <td>Windows 10 Sdk di aggiornamento di maggio 2020</td><td>DirectXMath 3.14</td>
 </tr>
 <tr>
  <td>Aggiornamento di Windows 10 (ottobre 2018) Sdk</td><td>DirectXMath 3.13</td>
 </tr>
 <tr>
  <td>Windows 10 Sdk di aggiornamento di aprile 2018<br />Windows 10 Fall Creators Update Sdk</td><td>DirectXMath 3.11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update Sdk</td><td>DirectXMath 3.10</td>
 </tr>
 <tr>
  <td>Windows 10 SDK per l'anniversario</td><td>DirectXMath 3.09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (novembre 2015)</td><td>DirectXMath 3.08</td>
 </tr>
 <tr>
  <td>Windows SDK per Windows 8.1 (spring 2015)</td><td>DirectXMath 3.07</td>
 </tr>
 <tr>
  <td>Windows SDK per Windows 8.1</td><td>DirectXMath 3.06</td>
 </tr>
 <tr>
  <td>Windows SDK per Windows 8</td><td>DirectXMath 3.03</td>
 </tr>
</table>

Per [altre informazioni, vedere Versioni di DirectXMath.](https://github.com/Microsoft/DirectXMath/releases)

## <a name="directxmath-differences-from-xna-math"></a>Differenze di DirectXMath rispetto a XNA Math

Ecco come la libreria DirectXMath differisce principalmente dalla libreria matematica XNA:

-   DirectXMath è solo C++ (spazi dei nomi, overload, nuovi modelli e così via).
-   Richiede il supporto della libreria standard C++11, ovvero stdint.h e così via.
-   Supporto degli intrinseci ARM-NEON per la Windows RT integrata.
-   Nuova funzionalità di colore (conversioni dello spazio dei colori, costanti di colore .NET).
-   Tipi di volume di delimitazione, una versione di cui in precedenza era presente l'intestazione XNACollision nell'esempio di collisione di DirectX SDK.
-   Nessuna Xbox 360 disponibile. Il Xbox 360 XDK continua a spedire XNAMath v2.x; rimozione di Xbox 360 tipi di dati e varianti di funzione specifici.
-   Rielaborato [**XMVectorPermute per migliorare**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) l'ottimizzazione per gli intrinseci SSE e ARM-NEON.
-   Il [**tipo XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) è completamente opaco. Per accedere ai singoli elementi **di XMMATRIX,** usare altri tipi, ad esempio [**XMFLOAT4X4.**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versioni di DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
