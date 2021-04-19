---
description: La libreria DirectXMath si basa sulla libreria XNA Math C++ SIMD versione 2. x. Qui viene descritto come DirectXMath differisce da XNA Math e come le versioni di DirectXMath sono diverse.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novità (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309244"
---
# <a name="whats-new-directxmath"></a>Novità (DirectXMath)

La libreria DirectXMath si basa sulla [libreria XNA Math C++ SIMD della versione 2,04](https://walbourn.github.io/). Qui viene descritto come DirectXMath differisce da XNA Math e come le versioni di DirectXMath sono diverse.

-   [Cronologia Rlease](#release-history)
-   [Differenze DirectXMath da XNA Math](#directxmath-differences-from-xna-math)
-   [Argomenti correlati](#related-topics)

## <a name="release-history"></a>Cronologia delle versioni

<table>
 <tr>
  <td>SDK di aggiornamento di Windows 10 maggio 2020</td><td>DirectXMath 3,14</td>
 </tr>
 <tr>
  <td>SDK di aggiornamento di Windows 10 ottobre 2018</td><td>DirectXMath 3,13</td>
 </tr>
 <tr>
  <td>SDK di aggiornamento di Windows 10 aprile 2018<br />Windows 10 Fall Creators Update SDK</td><td>DirectXMath 3,11</td>
 </tr>
 <tr>
  <td>SDK di Windows 10 Creators Update</td><td>DirectXMath 3,10</td>
 </tr>
 <tr>
  <td>Windows 10 Anniversary SDK</td><td>DirectXMath 3,09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (2015 novembre)</td><td>DirectXMath 3,08</td>
 </tr>
 <tr>
  <td>Windows SDK per Windows 8.1 (Spring 2015)</td><td>DirectXMath 3,07</td>
 </tr>
 <tr>
  <td>Windows SDK per Windows 8.1</td><td>DirectXMath 3,06</td>
 </tr>
 <tr>
  <td>Windows SDK per Windows 8</td><td>DirectXMath 3,03</td>
 </tr>
</table>

Per ulteriori informazioni, vedere [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) .

## <a name="directxmath-differences-from-xna-math"></a>Differenze DirectXMath da XNA Math

Ecco come la libreria DirectXMath differisce principalmente dalla libreria matematica XNA:

-   DirectXMath è solo C++ (spazi dei nomi, overload, nuovi modelli e così via).
-   Richiede il supporto della libreria standard C++ 11, ovvero stdint. h e così via.
-   ARM-NEON intrinseci supporto per la piattaforma Windows RT.
-   Nuova funzionalità per i colori (conversioni dello spazio dei colori, costanti di colore .NET).
-   Tipi di volumi di delimitazione (una versione di che in precedenza era presente nell'intestazione XNACollision nell'esempio di conflitto di DirectX SDK).
-   Nessuna versione di Xbox 360 disponibile. Il XDK di Xbox 360 continua a spedire XNAMath V2. x; rimozione dei tipi di dati e delle varianti di funzione specifici di Xbox 360.
-   [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) rilavorato per ottimizzare l'ottimizzazione per le funzioni intrinseche SSE e ARM-Neon.
-   Il tipo [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) è completamente opaco. Per accedere ai singoli elementi di **XMMATRIX**, usare altri tipi, ad esempio [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versioni di DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
