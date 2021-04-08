---
title: BITS e ripristino del sistema
description: Non tutte le versioni di BITS utilizzano lo stesso formato per archiviare i processi.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044254"
---
# <a name="bits-and-system-restore"></a>BITS e ripristino del sistema

Non tutte le versioni di BITS utilizzano lo stesso formato per archiviare i processi. Se il computer viene restituito a un punto di ripristino prima di un aggiornamento BITS, la versione precedente di BITS potrebbe non essere in grado di leggere le informazioni sul processo corrente. In tal caso, BITS eliminerà l'elenco dei processi e creerà un nuovo elenco di processi vuoti. Di conseguenza, i file temporanei associati all'elenco dei processi precedenti non vengono eliminati; per recuperare lo spazio su disco, è necessario eliminare i file manualmente.

Gli utenti che hanno familiarità con la riga di comando di Windows possono evitare questo problema usando lo [strumento Bitsadmin](bitsadmin-tool.md) per cancellare l'elenco dei processi BITS prima di eseguire Ripristino configurazione di sistema. Per cancellare l'elenco dei processi BITS, eseguire il comando seguente:

**Bitsadmin/reset/allusers**

Si noti che per eseguire questo comando è necessario disporre dei privilegi di amministratore.

 

 




