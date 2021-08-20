---
description: Il concetto di blocco in un ambiente Windows è stato storicamente molto importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operazioni di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d130de2322e10de15bc73e9901b7d55764b34cfbb609e2e25942fb55a3cf445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322436"
---
# <a name="blocking-operations"></a>Operazioni di blocco

Il concetto di blocco in un ambiente Windows è stato storicamente molto importante. Negli Windows Sockets 1.1, le chiamate di blocco erano sconsigliate perché tendevano a disabilitare l'interazione continua con il sistema. Inoltre, utilizzano una tecnica di pseudoblocco che, per diversi motivi, non sempre funziona come previsto. Tuttavia, negli ambienti Windows pianificati preventivamente, le chiamate di blocco hanno molto più senso, possono essere implementate dai servizi del sistema operativo nativo e sono in realtà un meccanismo generalmente preferito. L'API Winsock 2 non supporta più il blocco psuedoblocking, ma poiché gli schemi di compatibilità di Windows Sockets 1.1 devono continuare a emulare questo comportamento, i provider di servizi devono supportare questo comportamento come descritto di seguito.

 

 



