---
description: Poiché il protocollo Kerberos è stato originariamente progettato, una chiave master per un utente è stata derivata da una password fornita dall'utente.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Ticket Ticket-Granting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dff161ba2d905f676fe6b6b5e7e7d5289ee550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129314"
---
# <a name="ticket-granting-tickets"></a>Ticket Ticket-Granting

Poiché il [*protocollo Kerberos*](../secgloss/k-gly.md) è stato originariamente progettato, una chiave master per un utente è stata derivata da una password fornita dall'utente. Quando un utente ha effettuato l'accesso, il client Kerberos nella workstation dell'utente ha accettato la password dall'utente e la ha convertita in una chiave di crittografia passando il testo tramite una funzione [*hash*](../secgloss/h-gly.md) unidirezionale. L'hash risultante è la [*chiave master*](../secgloss/m-gly.md)dell'utente. Il client ha utilizzato questa *chiave master* per decrittografare le [*chiavi di sessione*](../secgloss/s-gly.md) ricevute dal KDC.

Il problema con la progettazione originale di Kerberos è che il client richiede la chiave master dell'utente ogni volta che viene decrittografata una chiave di sessione dal KDC. Ciò significa che il client deve chiedere all'utente la password all'inizio di ogni scambio client/server oppure il client deve archiviare la chiave dell'utente nella workstation. Interruzioni frequenti dell'utente sono troppo intrusive. L'archiviazione della chiave nella workstation rischia di compromettere una chiave derivata dalla password utente che è una chiave a lungo termine.

La soluzione del protocollo Kerberos a questo problema è che il client ottenga una chiave temporanea dal KDC. Questa chiave temporanea è efficace solo per questa [*sessione di accesso*](../secgloss/l-gly.md). Quando un utente esegue l'accesso, il client richiede un ticket per il KDC così come richiederebbe un ticket per qualsiasi altro servizio. Il KDC risponde creando una chiave della sessione di accesso e un ticket per un server speciale, il servizio di concessione ticket completo del KDC. Una copia della chiave della sessione di accesso è incorporata nel ticket e il ticket viene crittografato con la chiave master del KDC. Un'altra copia della chiave della sessione di accesso viene crittografata con la chiave master dell'utente derivata dalla password di accesso dell'utente. Sia il ticket che la chiave della sessione crittografata vengono inviati al client.

Quando il client riceve la risposta del KDC, decrittografa la chiave della sessione di accesso con la chiave master dell'utente derivata dalla password dell'utente. Il client non richiede più la chiave derivata dalla password dell'utente perché il client userà ora la chiave della sessione di accesso per decrittografare la propria copia di qualsiasi chiave di sessione del server ottenuta dal KDC. Il client archivia la chiave della sessione di accesso nella cache dei ticket insieme al relativo ticket per il servizio di concessione ticket completo del KDC.

Il ticket per il servizio di concessione ticket completo è denominato ticket di concessione ticket (TGT). Quando il client richiede al KDC un ticket a un server, presenta le [*credenziali*](../secgloss/c-gly.md) sotto forma di un messaggio di autenticatore e di un ticket, in questo caso un TGT, proprio come se presentasse le credenziali a qualsiasi altro servizio. Il servizio di concessione ticket apre il TGT con la chiave master, estrae la chiave della sessione di accesso per il client e usa la chiave della sessione di accesso per crittografare la copia del client di una chiave di sessione per il server.

 

 
