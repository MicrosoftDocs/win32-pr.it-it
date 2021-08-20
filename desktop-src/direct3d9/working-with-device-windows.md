---
description: Questa sezione elenca un problema che potrebbe verificarsi quando si lavora con le finestre dei dispositivi nelle applicazioni Direct3D.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Uso di Device Windows (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98bfc53abb77fbc657bab49e8d0135996eba9bfcd4b00d77c50b200d33a924
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518831"
---
# <a name="working-with-device-windows-direct3d-9"></a>Uso di Device Windows (Direct3D 9)

Questa sezione elenca un problema che potrebbe verificarsi quando si lavora con le finestre dei dispositivi nelle applicazioni Direct3D.

-   Direct3D collega solo le finestre dello stato attivo anziché la finestra del dispositivo con la funzione di elaborazione dei messaggi Direct3D ed elabora solo i messaggi della finestra di stato attivo. Pertanto, la finestra dello stato attivo deve essere l'elemento padre di qualsiasi finestra del dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 



