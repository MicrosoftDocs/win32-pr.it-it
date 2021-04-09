---
description: In questa appendice viene illustrata una versione riscritta delle applicazioni di esempio SIMPLEC. c e simples. c che gestiscono normalmente il codice server CodeIPv6-Enabled client abilitato per IPv4 o IPv6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Appendice B: codice sorgente indipendente dalla versione IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879237"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a>Appendice B: codice sorgente indipendente dalla versione IP

In questa appendice viene illustrata una versione riscritta delle applicazioni di esempio SIMPLEC. c e simples. c che gestiscono normalmente IPv4 o IPv6.

-   [Codice client abilitato per IPv6](ipv6-enabled-client-code-2.md)
-   [Codice server abilitato per IPv6](ipv6-enabled-server-code-2.md)

Questo codice esemplifica le linee guida definite in questa guida IPv6 ed è incluso per fornire codice sorgente che è stato modificato correttamente per aggiungere il supporto per IPv6. Questo esempio è intenzionalmente semplice, ma offre un esempio pratico per la lettura e la revisione. Una versione solo IPv4 di questo codice sorgente è disponibile nell' [appendice a: codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md).

Confrontando il codice sorgente in Appendice A (solo IPv4) e Appendice B (IP-version Agnostic), si ottiene un'idea delle modifiche necessarie per modificare l'applicazione Windows Sockets per aggiungere il supporto per IPv6.

 

 



