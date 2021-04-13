---
title: Funzioni di sicurezza
description: Le funzioni di sicurezza di gestione della rete ottengono e impostano i descrittori di sicurezza per le radici autonome e basate su dominio DFS.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483845"
---
# <a name="security-functions"></a>Funzioni di sicurezza

Le funzioni di sicurezza di gestione della rete ottengono e impostano i descrittori di sicurezza per le radici autonome e basate su dominio DFS.

Le funzioni di sicurezza DFS sono elencate di seguito.

| Funzione                                                               | Descrizione                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Ottiene il descrittore di sicurezza per l'oggetto radice della radice DFS specificata.                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Individua l'oggetto radice per la radice DFS specificata e imposta il descrittore di sicurezza fornito.                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Ottiene il descrittore di sicurezza per l'oggetto contenitore della radice autonoma DFS specificata.                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Individua l'oggetto contenitore per la radice autonoma DFS specificata e imposta il descrittore di sicurezza fornito. |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Ottiene il descrittore di sicurezza per l'oggetto contenitore della radice del dominio DFS specificata.                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Individua l'oggetto contenitore per la radice del dominio DFS specificata e imposta il descrittore di sicurezza fornito.      |
