---
description: La libreria DirectXMath è basata sulla libreria SIMD XNA Math C++ versione 2.x. Di seguito viene descritto come DirectXMath differisce da XNA Math e come differiscono le versioni di DirectXMath.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novità (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827627"
---
# <a name="whats-new-directxmath"></a>Novità (DirectXMath)

La libreria DirectXMath è basata sulla libreria [SIMD XNA Math C++ versione 2.04.](https://walbourn.github.io/xna-math-version-2-04/) Di seguito viene descritto come DirectXMath differisce da XNA Math e come differiscono le versioni di DirectXMath.

-   [Cronologia di Rlease](#release-history)
-   [Differenze di DirectXMath rispetto a XNA Math](#directxmath-differences-from-xna-math)
-   [Argomenti correlati](#related-topics)

## <a name="release-history"></a>Cronologia delle versioni

<table>
 <tr>
  <td>Windows 10 SDK (20348), versione 2104</td><td>DirectXMath 3.16</td>
 </td>
 <tr>
  <td>Windows 10 sdk di aggiornamento di maggio 2020</td><td>DirectXMath 3.14</td>
 </tr>
 <tr>
  <td>Aggiornamento di Windows 10 (ottobre 2018) SDK</td><td>DirectXMath 3.13</td>
 </tr>
 <tr>
  <td>Aggiornamento di Windows 10 (aprile 2018) SDK<br />Windows 10 Fall Creators Update SDK</td><td>DirectXMath 3.11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update SDK</td><td>DirectXMath 3.10</td>
 </tr>
 <tr>
  <td>Windows 10 Anniversary SDK</td><td>DirectXMath 3.09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (novembre 2015)</td><td>DirectXMath 3.08</td>
 </tr>
 <tr>
  <td>Windows SDK for Windows 8.1 (Spring 2015)</td><td>DirectXMath 3.07</td>
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
-   Supporto degli intrinseci ARM-NEON per la Windows RT di lavoro.
-   Nuova funzionalità di colore (conversioni dello spazio dei colori, costanti di colore .NET).
-   Tipi di volume di delimitazione, una versione di cui in precedenza era presente l'intestazione XNACollision nell'esempio di collisione di DirectX SDK.
-   Nessuna Xbox 360 disponibile. Il Xbox 360 XDK continua a spedire XNAMath v2.x; rimozione di Xbox 360 tipi di dati e varianti di funzione specifici.
-   Rielaborato [**XMVectorPermute per**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) migliorare l'ottimizzazione per gli intrinseci SSE e ARM-NEON.
-   Il [**tipo XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) è completamente opaco. Per accedere ai singoli elementi **di XMMATRIX,** usare altri tipi, ad esempio [**XMFLOAT4X4.**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versioni di DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
