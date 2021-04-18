---
description: Direct3D è un'API di basso livello per il disegno di primitive con la pipeline di rendering o l'esecuzione di operazioni parallele con compute shader.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Introduzione a Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2b5a579b589a747c4e7640b3c868d488a7e58f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313061"
---
# <a name="getting-started-with-direct3d"></a>Introduzione a Direct3D

Direct3D è un'API di basso livello per il disegno di primitive con la pipeline di rendering o per l'esecuzione di operazioni parallele con compute shader.

## <a name="what-is-direct3d"></a>Che cos'è Direct3D?

Direct3D è un'API di basso livello che è possibile usare per creare triangoli, linee o punti per fotogramma oppure per avviare operazioni altamente parallele sulla GPU.

Direct3D

-   Nasconde diverse implementazioni GPU dietro un'astrazione coerente. Ma è comunque necessario saper creare grafica 3D.
-   È progettato per gestire un processore separato specifico per la grafica. Le GPU più recenti hanno centinaia o migliaia di processori paralleli.
-   Enfatizza l'elaborazione parallela. Si configura una serie di rendering o di calcolo e quindi si avvia un'operazione. Non attendi commenti e suggerimenti immediati dall'operazione. Non si combinano operazioni CPU e GPU.

## <a name="which-direct3d-apis-can-you-use"></a>Quali API Direct3D è possibile usare?

Le API Direct3D scelte dipendono dallo stile dell'app che si vuole scrivere.

-   Se si vuole scrivere un'app UWP, usare un subset di API Direct3D 11, DXGI e HLSL. Per un elenco di queste API, vedere [API Win32 e com per le app UWP](/uwp/win32-and-com/win32-and-com-for-uwp-apps). Per informazioni su come scrivere un'app di Windows Store Direct3D 11, vedere [creare grafica 3D con DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).
-   Se si scrive un'applicazione desktop, è possibile usare il set completo di API Direct3D 11, DXGI e HLSL.
-   A partire da Windows 8, Microsoft non supporta più attivamente il framework XNA per le applicazioni desktop. Tuttavia, le app di Windows Store, le app UWP e le app desktop possono usare il set completo di API [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) e [DirectXMath](/windows/desktop/dxmath/directxmath-portal) . Le app desktop possono usare il set completo di API [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) , mentre le app di Windows Store e le app UWP possono usare la maggior parte delle API XInput. per altre informazioni, vedere [versioni di XInput](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>Quale versione di Direct3D?

La versione dell'API Direct3D scelta dipende dal sistema operativo e dal livello hardware di destinazione.

-   Per fare riferimento a Windows 8 e versioni successive, usare le API Direct3D 11.
-   Usare le API Direct3D 9 con Windows XP e versioni successive. Tutti i componenti hardware supportano le API Direct3D 9, anche l'hardware più recente a livello di Direct3D 11.
-   Usare le API Direct3D 10 con Windows Vista e versioni successive. Solo i componenti hardware Direct3D 10 e versioni successive supportano le API Direct3D 10.
-   Usare le API Direct3D 10,1 e Direct3D 11 con Windows 7 e versioni successive. È inoltre possibile utilizzare le API Direct3D 10,1 e Direct3D 11 con Windows Vista con Service Pack 2 (SP2) scaricando [KB 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Pipeline di rendering Direct3D

Nella pipeline di [rendering](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)Direct3D i dati passano da diverse origini, ad esempio gli affluenti di un fiume.

-   Alcune parti del flusso sono programmabili.
-   Alcune parti includono manopole e quadrate.
-   Le origini dei dati sono flussi seriali di pacchetti (vertici) o matrici indicizzabili (risorse dello shader).
-   I vertici e le risorse dello shader scorrono in primitive, che è possibile amplificare.
-   Le primitive e le risorse dello shader scorrono in operazioni pixel.

## <a name="direct3d-compute-shader"></a>Compute Shader Direct3D

Con Direct3D [compute shader](./direct3d11/direct3d-11-advanced-stages-compute-shader.md), tutti i processori della GPU vengono eseguiti in parallelo. Quindi, compute shader si comporta in modo più simile a uno stagno rispetto a un fiume.
