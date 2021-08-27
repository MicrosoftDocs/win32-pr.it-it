---
description: Direct3D è un'API di basso livello per disegnare primitive con la pipeline di rendering o eseguire operazioni parallele con lo shader di calcolo.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Introduzione a Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea01f24659bfbb5eb0667a0ae1cbfa3529a206b7b7ce7e3d3a4388e71fabd571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092551"
---
# <a name="getting-started-with-direct3d"></a>Introduzione a Direct3D

Direct3D è un'API di basso livello per il disegno di primitive con la pipeline di rendering o per l'esecuzione di operazioni parallele con lo shader di calcolo.

## <a name="what-is-direct3d"></a>Che cos'è Direct3D?

Direct3D è un'API di basso livello che è possibile usare per disegnare triangoli, linee o punti per fotogramma o per avviare operazioni altamente parallele nella GPU.

Direct3d:

-   Nasconde diverse implementazioni della GPU dietro un'astrazione coerente. È comunque necessario sapere come disegnare grafica 3D.
-   È progettato per guidare un processore specifico della grafica separato. Le GPU più nuove hanno centinaia o migliaia di processori paralleli.
-   Enfatizza l'elaborazione parallela. Si configura un gruppo di stato di rendering o calcolo e quindi si avvia un'operazione. Non si attende un feedback immediato dall'operazione. Le operazioni cpu e GPU non vengono combinate.

## <a name="which-direct3d-apis-can-you-use"></a>Quali API Direct3D è possibile usare?

Le API Direct3D che si sceglie dipendono dal tipo di app che si vuole scrivere.

-   Se si vuole scrivere un'app UWP, usare un subset di API Direct3D 11, DXGI e HLSL. Per un elenco di queste API, vedere [API Win32 e COM per le app UWP.](/uwp/win32-and-com/win32-and-com-for-uwp-apps) Per informazioni su come scrivere un'app Direct3D 11 Windows Store, vedere Creare grafica [3D con DirectX.](/previous-versions/windows/apps/hh465137(v=win.10))
-   Se si scrive un'app desktop, è possibile usare il set completo di API Direct3D 11, DXGI e HLSL.
-   A partire Windows 8, il framework XNA per le app desktop non è più attivo. Ma Windows app dello Store, app UWP e app desktop possono usare il set completo delle API [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) e [DirectXMath.](/windows/desktop/dxmath/directxmath-portal) Le app desktop possono usare il set completo delle API [XInput,](/windows/desktop/xinput/xinput-game-controller-apis-portal) mentre le app di Windows Store e le app UWP possono usare la maggior parte delle API XInput. Per altre informazioni, vedere [Versioni di XInput.](/windows/desktop/xinput/xinput-versions)

## <a name="which-direct3d-version"></a>Quale versione di Direct3D?

La versione dell'API Direct3D scelta dipende dal sistema operativo e dal livello hardware di destinazione.

-   Se si vuole usare come destinazione Windows 8 e versioni successive, usare le API Direct3D 11.
-   Usare le API Direct3D 9 con Windows XP e versioni successive. Tutto l'hardware supporta le API Direct3D 9, anche l'hardware di livello 11 Direct3D più recente.
-   Usare le API Direct3D 10 con Windows Vista e versioni successive. Solo l'hardware Direct3D 10 e versioni successive supportano le API Direct3D 10.
-   Usare le API Direct3D 10.1 e Direct3D 11 con Windows 7 e versioni successive. È anche possibile usare le API Direct3D 10.1 e Direct3D 11 con Windows Vista con Service Pack 2 (SP2) scaricando [kb 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Direct3D Rendering Pipeline

Nella pipeline di [rendering](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)Direct3D i dati vengono flussi da diverse origini, ad esempio gli affluenti di un river.

-   Alcune parti del flusso sono programmabili.
-   Alcune parti hanno manopole e quadranti.
-   Le origini dati sono flussi seriali di pacchetti (vertici) o matrici indicizzabili (risorse shader).
-   I vertici e le risorse shader fluire in primitive, che è possibile amplificare.
-   Le primitive e le risorse shader scorrono in operazioni pixel.

## <a name="direct3d-compute-shader"></a>Shader di calcolo Direct3D

Con lo shader di [calcolo](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)Direct3D, tutti i processori della GPU vengono eseguiti in parallelo. Quindi, lo shader di calcolo si comporta più come un acquaio rispetto a un river.
