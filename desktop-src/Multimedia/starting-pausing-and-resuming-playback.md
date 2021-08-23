---
title: Avvio, sospensione e ripresa della riproduzione
description: Avvio, sospensione e ripresa della riproduzione
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- Macro MCIWndPlay
- Macro MCIWndPause
- Macro MCIWndResume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49977b9bc741c6b32ce0da0c0ae9f63bd875a24268a00bb4782cd71531a4ef31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688671"
---
# <a name="starting-pausing-and-resuming-playback"></a>Avvio, sospensione e ripresa della riproduzione

[**MCIWndPlay è**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) la macro di riproduzione più generale. Questa macro consente di riprodurre un file o un dispositivo dalla posizione di riproduzione corrente. La riproduzione continua fino alla fine del contenuto, a meno che non venga interrotta.

È possibile interrompere temporaneamente un dispositivo in riproduzione usando la macro [**MCIWndPause.**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) Per riprendere la riproduzione dalla posizione sospesa, usare la macro [**MCIWndResume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) Alcuni dispositivi non supportano i comandi sospendi e riprendi. Questi dispositivi in genere e **mappano MCIWndPause** alla macro [**MCIWndStop,**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) che interrompe la riproduzione o la registrazione. Puoi riavviare un dispositivo che non supporta la sospensione o la ripresa usando **MCIWndPlay,** che avvia la riproduzione dalla posizione di riproduzione corrente.

 

 




