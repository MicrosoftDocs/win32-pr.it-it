---
title: Disabilitazione delle funzionalità di Servizi Desktop remoto
description: Per una maggiore sicurezza, è possibile scegliere di disabilitare Servizi Desktop remoto funzionalità.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "103963639"
---
# <a name="disabling-remote-desktop-services-features"></a>Disabilitazione delle funzionalità di Servizi Desktop remoto

Per una maggiore sicurezza, è possibile scegliere di disabilitare Servizi Desktop remoto funzionalità come il reindirizzamento degli Appunti e il reindirizzamento della stampante per i client che si connettono ai server di host sessione Desktop remoto (host sessione Desktop remoto) utilizzando il Desktop remoto controllo ActiveX.

**Per disabilitare le funzionalità di Servizi Desktop remoto**

1.  Modificare il registro di sistema del computer client e aggiungere le chiavi seguenti:

    -   **\_Computer locale \_ HKEY \\ software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**
    -   **\_Computer locale \_ HKEY \\ software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**
    -   **\_Computer locale \_ HKEY \\ software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**

2.  Impostare il valore di entrambe le chiavi su **reg \_ DWORD** 1.

 

 




