---
title: Modifica del registro di sistema di Windows 95
description: È possibile utilizzare REGEDIT per modificare il registro di sistema di Windows 95 per designare un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856773"
---
# <a name="editing-the-windows-95-registry"></a>Modifica del registro di sistema di Windows 95

È possibile utilizzare REGEDIT per modificare il registro di sistema di Windows 95 per designare un NSP.

**Per designare un provider di servizi di nome localizzatore Microsoft per Windows 95**

1.  Select

    **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **RPC**

2.  Crea una nuova chiave denominata

    **NameService**

3.  Con la chiave **NameService** selezionata, creare i nuovi nomi **StringValue** e modificarli in modo che contengano i dati, come illustrato nella tabella seguente.

    

    | Nome                     | Data                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                                |
    | **Protocollo**             | \_NP ncacn<br/>                                                        |
    | **Endpoint**             | \\\\localizzatore pipe<br/>                                                  |
    | **NetworkAddress**       | MyServer (dove MyServer è il nome del computer Windows NT)<br/> |
    | **ServerNetworkAddress** | MyServer<br/>                                                         |

    

     

È possibile utilizzare REGEDIT per modificare il registro di sistema di Windows 95 per designare un NSP DCE CDS.

**Per designare un provider di servizi di nomi di CDS DCE per Windows 95**

1.  Select

    **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **RPC**

2.  Crea una nuova chiave denominata

    **NameService**

3.  Con la chiave **NameService** selezionata, creare i nuovi nomi **StringValue** e modificarli in modo che contengano i dati, come illustrato nella tabella seguente.

    

    | Nome                     | Data                                                             |
    |--------------------------|------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                     |
    | **Protocollo**             | \_TCP IP \_ ncacn<br/>                                        |
    | **Endpoint**             | "" (stringa vuota)<br/>                                  |
    | **NetworkAddress**       | MyServer (il nome del computer host che esegue NSID)<br/> |
    | **ServerNetworkAddress** | MyServer (il nome del computer host che esegue NSID)<br/> |

    

     

    > [!Note]  
    > Per configurare i CD DCE come provider di servizi di nome, è necessario disporre del prodotto del servizio directory celle DCE Digital Equipment Corporation. Per informazioni sui CD DCE, vedere la documentazione fornita da Digital Equipment Corporation.

     

 

 





