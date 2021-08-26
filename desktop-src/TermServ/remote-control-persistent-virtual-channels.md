---
title: Canali virtuali permanenti di controllo remoto
description: Un canale virtuale permanente di controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client. I dati continueranno a essere trasmessi e ricevuti tramite questo canale.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71206b8272fb516da9a3c39bed7f7d54edbc5227958d975bf11b114db9c13869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988781"
---
# <a name="remote-control-persistent-virtual-channels"></a>Canali virtuali permanenti di controllo remoto

In Windows XP, una DLL può specificare uno o più canali virtuali come *persistenti di controllo remoto.* Un canale virtuale permanente di controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client. I dati continueranno a essere trasmessi e ricevuti tramite questo canale. I canali virtuali che la DLL non specifica come persistenti per il controllo remoto verranno chiuso in questo scenario.

I canali virtuali permanenti di controllo remoto vengono specificati durante la chiamata **a VirtualChannelInit.** Per informazioni specifiche su questo argomento, vedere la pagina di riferimento per [**VirtualChannelInit.**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)

 

 




