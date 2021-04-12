---
title: Verifica del kernel per i driver non WHQL firmati
description: Per i dispositivi che puliscono l'installazione di Windows 10 e l'avvio protetto (si noti che questo è lo standard per tutti i nuovi dispositivi rispetto alla versione di Windows 8,0), tutti i nuovi driver devono essere firmati da WHQL/sysdev anziché usare semplicemente certificati con firma incrociata.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396550"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Verifica del kernel per i driver non WHQL firmati

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Per i dispositivi che puliscono l'installazione di Windows 10 e l'avvio protetto (si noti che questo è lo standard per tutti i nuovi dispositivi rispetto alla versione di Windows 8,0), tutti i nuovi driver devono essere firmati da WHQL/sysdev anziché usare semplicemente certificati con firma incrociata. I dispositivi aggiornati e i casi in cui i driver sono stati firmati con un certificato incrociato prima che questo criterio venisse applicato vengono esclusi da questi criteri per garantire la compatibilità con le versioni precedenti. Questo criterio è stato annunciato il 2015 aprile, ma verrà applicato con l'edizione dell'anniversario di Windows, rilasciato il 2016 agosto.

Nei casi in cui un driver non è firmato correttamente, si manifesterà come una notifica PCA che i driver vengono bloccati quando non vengono superati i requisiti di firma. In questo modo si impedisce che un'esperienza utente disconnessa in un secondo momento del driver venga bloccata nel kernel in modo trasparente.

Per altre informazioni, fare riferimento a [questo post di Blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), che annuncia la modifica della firma del driver.

 

 




