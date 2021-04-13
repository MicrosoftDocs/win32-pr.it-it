---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104352001"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>Scopo

L'API di DirectXMath fornisce funzioni e tipi C++ intuitivi per l'algebra lineare comune e le operazioni matematiche grafiche comuni alle applicazioni DirectX. La libreria fornisce le versioni ottimizzate per Windows a 32 bit (x86), Windows 64-bit (x64) e Windows su ARM/ARM64 tramite SSE, AVX e il supporto degli intrinseci ARM-NEON nel compilatore Visual C++.

Per gli sviluppatori che non hanno familiarità con DirectXMath, è consigliabile usare il wrapper SimpleMath in *DirectX Tool Kit* per [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) come punto di partenza.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                     | Descrizione                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Guida alla programmazione di DirectXMath](ovw-xnamath-progguide.md)<br/>     | DirectXMath fornisce una soluzione matematica ottimizzata per Windows.<br/>           |
| [Guida di riferimento alla programmazione DirectXMath](ovw-xnamath-reference.md)<br/> | Questa sezione contiene materiale di riferimento per la libreria DirectXMath.<br/> |



 

## <a name="developer-audience"></a>Sviluppatori

La libreria DirectXMath è progettata per gli sviluppatori C++ che lavorano su giochi e grafica DirectX in app di Windows Store, Xbox Games e applicazioni desktop tradizionali per Windows.

## <a name="obtaining-directxmath"></a>Recupero di DirectXMath
 
Le intestazioni DirectXMath vengono fornite nella Windows SDK fornita con Visual Studio 2012 o versioni successive e come intestazione all inline non è presente alcuna DLL o libreria statica con cui eseguire il collegamento. È disponibile anche come pacchetto in [NuGet](https://www.nuget.org/packages/directxmath/).

DirectXMath è open source con la [licenza mit](https://opensource.org/licenses/MIT) ospitata su [GitHub](https://github.com/Microsoft/DirectXMath).




