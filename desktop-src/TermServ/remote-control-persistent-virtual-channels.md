---
title: Canale virtuale persistente del controllo remoto
description: Un canale virtuale persistente del controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client. I dati continueranno a essere trasmessi e ricevuti tramite questo canale.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396754"
---
# <a name="remote-control-persistent-virtual-channels"></a>Canale virtuale persistente del controllo remoto

In Windows XP, una DLL può specificare uno o più canali virtuali come *controllo remoto persistente*. Un canale virtuale persistente del controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client. I dati continueranno a essere trasmessi e ricevuti tramite questo canale. In questo scenario, i canali virtuali che la DLL non specifica come controllo remoto persistente si chiuderà.

I canali virtuali permanenti di controllo remoto vengono specificati durante la chiamata a **VirtualChannelInit**. Per informazioni specifiche su questa pagina, vedere la pagina di riferimento per [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .

 

 




