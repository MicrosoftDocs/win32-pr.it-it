---
description: Per rimuovere i contatori delle prestazioni delle applicazioni dal sistema, seguire questa procedura.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Eliminazione dei contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c34dfc64be4ded0ce07b466393851b235ca4b2f49c89e05f067041f236565fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144014"
---
# <a name="deleting-performance-counters"></a>Eliminazione dei contatori delle prestazioni

Per rimuovere i contatori delle prestazioni dell'applicazione dal sistema, seguire questa procedura.

1.  Usare lo **strumento unlodctr** incluso nel computer per rimuovere i dati correlati ai contatori dal Registro di sistema. Si noti che la chiave **performance dell'applicazione** deve esistere perché lo **strumento unlodctr** riesca. Per informazioni dettagliate, [vedere Rimozione di nomi e descrizioni dei contatori dal Registro di sistema.](removing-counter-names-and-descriptions-from-the-registry.md)
2.  Eliminare le **chiavi Prestazioni** **e Collegamento** sotto la chiave **Servizi** dell'applicazione. Per eliminare queste chiavi, usare l'utilità Regedt32.exe o chiamare [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
