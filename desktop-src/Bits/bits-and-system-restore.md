---
title: BITS e Ripristino configurazione di sistema
description: Non tutte le versioni di BITS usano lo stesso formato per archiviare i processi.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0fbf96cf4d1e3372a9e65cad27c1e1f34ebdb07b6edd976e8b1f36add8a50eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702101"
---
# <a name="bits-and-system-restore"></a>BITS e Ripristino configurazione di sistema

Non tutte le versioni di BITS usano lo stesso formato per archiviare i processi. Se si restituisce il computer a un punto di ripristino prima di un aggiornamento BITS, la versione precedente di BITS potrebbe non essere in grado di leggere le informazioni sul processo corrente. In questo caso, BITS eliminerà l'elenco dei processi e creerà un nuovo elenco di processi vuoto. Di conseguenza, i file temporanei associati all'elenco dei processi precedenti non vengono puliti. Per recuperare lo spazio su disco, è necessario eliminare i file manualmente.

Gli utenti che hanno familiarità Windows riga di comando possono evitare questo problema usando lo strumento [BITSAdmin](bitsadmin-tool.md) per cancellare l'elenco dei processi BITS prima di eseguire Ripristino configurazione di sistema. Per cancellare l'elenco dei processi BITS, eseguire il comando seguente:

**bitsadmin /reset /allusers**

Per eseguire questo comando, è necessario disporre dei privilegi di amministratore.

 

 




