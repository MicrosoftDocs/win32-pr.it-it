---
description: Il sistema operativo Microsoft Windows fornisce il supporto per un'ampia gamma di dispositivi hardware e protocolli di tempo di rete mediante l'architettura del provider di servizi temporali.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Provider di servizi temporali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884025"
---
# <a name="time-provider"></a>Provider di servizi temporali

Il sistema operativo Microsoft Windows fornisce il supporto per un'ampia gamma di dispositivi hardware e protocolli di tempo di rete mediante l'architettura del *provider di servizi temporali* . I provider del tempo di input recuperano timestamp accurati dall'hardware o dalla rete e i provider del tempo di output forniscono indicatori temporali ad altri client nella rete.

I provider di tempo sono gestiti da *gestione provider di servizi temporali*. È responsabile del caricamento, dell'avvio e dell'arresto dei provider di servizi temporali come indicato da Gestione controllo servizi. Questa interfaccia rende più semplice la scrittura di un provider di tempo rispetto alla scrittura di un servizio completo.

-   [Creazione di un provider Time](creating-a-time-provider.md)
-   [Registrazione di un provider Time](registering-a-time-provider.md)
-   [Provider ora di esempio](sample-time-provider.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio Ora di Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



