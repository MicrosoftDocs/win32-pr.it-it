---
title: Verifica del kernel per i driver firmati non WHQL
description: Per i dispositivi con installazione pulita Windows 10 e in cui è installato l'avvio protetto (si noti che si tratta di uno standard per tutti i nuovi dispositivi dopo il rilascio di Windows 8.0), tutti i nuovi driver devono essere firmati da WHQL/Sysdev anziché usare solo certificati con firma incrociata.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810d0549086d36f146ca80c0b9c83a7258bb3b120202432cdab6203a081cdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852417"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Verifica del kernel per i driver firmati non WHQL

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Per i dispositivi con installazione pulita Windows 10 e in cui è installato l'avvio protetto (si noti che si tratta di uno standard per tutti i nuovi dispositivi dopo il rilascio di Windows 8.0), tutti i nuovi driver devono essere firmati da WHQL/Sysdev anziché usare solo certificati con firma incrociata. I dispositivi aggiornati e i casi in cui i driver sono stati firmati con un certificato incrociato prima dell'applicazione di questo criterio vengono esclusi da questo criterio per garantire la compatibilità con le versioni precedenti. Questo criterio è stato annunciato ad aprile 2015, ma verrà applicato con l'Windows Anniversary Edition, rilasciata ad agosto 2016.

Nei casi in cui un driver non è firmato correttamente, si manifesterà come notifica PCA che i driver vengono bloccati quando non superano i requisiti di firma. In questo modo si evita che un'esperienza utente disconnessa successiva del driver venga bloccata nel kernel in modo trasparente.

Per altre informazioni, vedere questo [post di blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/)che annuncia la modifica della firma del driver.

 

 




