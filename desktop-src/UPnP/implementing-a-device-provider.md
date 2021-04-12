---
title: Implementazione di un provider di dispositivi
description: Per implementare un provider di dispositivi, creare un oggetto che espone l'interfaccia IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471726"
---
# <a name="implementing-a-device-provider"></a>Implementazione di un provider di dispositivi

Per implementare un provider di dispositivi, creare un oggetto che espone l'interfaccia [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) . Questo oggetto deve essere registrato con l'host del dispositivo usando il metodo [**IUPnPRegistrar:: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) . Questo metodo accetta i parametri seguenti:

-   Nome del provider, che deve essere univoco nel computer.
-   ProgID della classe che implementa il provider del dispositivo.
-   Stringa di inizializzazione che viene passata al provider di dispositivi quando viene avviata.
-   ID del contenitore. Un ID contenitore è una stringa che identifica il gruppo a cui appartiene il dispositivo. Tutti i dispositivi con lo stesso identificatore del contenitore sono ospitati nello stesso processo.

 

 




