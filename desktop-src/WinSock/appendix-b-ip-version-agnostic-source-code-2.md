---
description: Questa appendice illustra una versione riscritta delle applicazioni di esempio Simplec.c e Simples.c che gestisce correttamente il codice del server client CodeIPv6-Enabled abilitato per IPv4 o IPv6 o IPv6
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Appendice B: Codice sorgente indipendente dalla versione IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37daf34b4a7d46a2fb8fc3cbaf5aed6cf7e054a3fb0147de8d86a643a9e4f59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741608"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a>Appendice B: Codice sorgente indipendente dalla versione IP

Questa appendice illustra una versione riscritta delle applicazioni di esempio Simplec.c e Simples.c che gestisce correttamente IPv4 o IPv6.

-   [Codice client abilitato per IPv6](ipv6-enabled-client-code-2.md)
-   [Codice server abilitato per IPv6](ipv6-enabled-server-code-2.md)

Questo codice esemplifica le linee guida riportate in questa guida per IPv6 ed è incluso per fornire il codice sorgente che è stato modificato correttamente per aggiungere il supporto per IPv6. Questo esempio è intenzionalmente semplice, ma fornisce un esempio hands-on per il perusing e la revisione. Una versione solo IPv4 di questo codice sorgente è disponibile [nell'Appendice A: Codice sorgente solo IPv4.](appendix-a-ipv4-only-source-code-2.md)

Confrontando il codice sorgente nell'Appendice A (solo IPv4) e nell'Appendice B (indipendente dalla versione IP), si ottiene un'idea delle modifiche necessarie per modificare l'applicazione Windows Sockets per aggiungere il supporto per IPv6.

 

 



