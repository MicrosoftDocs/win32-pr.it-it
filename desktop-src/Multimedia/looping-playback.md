---
title: Riproduzione a ciclo continuo per MCIWnd
description: Riproduzione a ciclo continuo (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9144cd17886ff9d6f59bc38311481335a9ae581e5464d7feda0e7fd1a4ec2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139292"
---
# <a name="looping-playback-for-mciwnd"></a>Riproduzione a ciclo continuo per MCIWnd

MCIWnd supporta la riproduzione come ciclo continuo. È possibile riprodurre ripetutamente il contenuto di un file o di un dispositivo come ciclo usando  la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) in combinazione con il pulsante Riproduci sulla barra degli strumenti. Il dispositivo di riproduzione video, MCIAVI, supporta i cicli di riproduzione. Per determinare se la riproduzione continua è stata attivata, usare la macro [**MCIWndGetRepeat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)

 

 




