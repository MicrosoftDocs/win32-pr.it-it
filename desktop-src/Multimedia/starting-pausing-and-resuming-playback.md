---
title: Avvio, sospensione e ripresa della riproduzione
description: Avvio, sospensione e ripresa della riproduzione
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay (macro)
- MCIWndPause (macro)
- MCIWndResume (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222058"
---
# <a name="starting-pausing-and-resuming-playback"></a>Avvio, sospensione e ripresa della riproduzione

[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) è la macro di riproduzione più generale. Questa macro consente di riprodurre un file o un dispositivo dalla posizione di riproduzione corrente. La riproduzione continua fino alla fine del contenuto a meno che non venga interrotta.

È possibile interrompere temporaneamente un dispositivo che sta eseguendo usando la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) . Per riprendere la riproduzione dalla posizione sospesa, usare la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) . Alcuni dispositivi non supportano i comandi Sospendi e Riprendi. Questi dispositivi in genere mappano **MCIWndPause** alla macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , che interrompe la riproduzione o la registrazione. È possibile riavviare un dispositivo che non supporta la sospensione o la ripresa usando **MCIWndPlay**, che avvia la riproduzione dalla posizione di riproduzione corrente.

 

 




