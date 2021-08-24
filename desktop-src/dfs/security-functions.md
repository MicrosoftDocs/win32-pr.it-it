---
title: Funzioni di sicurezza
description: Le funzioni di sicurezza di gestione della rete ottengono e impostano descrittori di sicurezza per radici DFS basate su dominio e autonome.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31611aa650bb55ecdc29af468e0ef784b670555b247d536d27b397de356f4ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677801"
---
# <a name="security-functions"></a>Funzioni di sicurezza

Le funzioni di sicurezza di gestione della rete ottengono e impostano descrittori di sicurezza per radici DFS basate su dominio e autonome.

Le funzioni di sicurezza DFS sono elencate di seguito.

| Funzione                                                               | Descrizione                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Ottiene il descrittore di sicurezza per l'oggetto radice della radice DFS specificata.                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Individua l'oggetto radice per la radice DFS specificata e imposta il descrittore di sicurezza fornito su di esso.                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Ottiene il descrittore di sicurezza per l'oggetto contenitore della radice autonoma DFS specificata.                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Individua l'oggetto contenitore per la radice autonoma DFS specificata e imposta il descrittore di sicurezza fornito su di esso. |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Ottiene il descrittore di sicurezza per l'oggetto contenitore della radice del dominio DFS specificata.                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Individua l'oggetto contenitore per la radice del dominio DFS specificata e imposta il descrittore di sicurezza fornito su di esso.      |
