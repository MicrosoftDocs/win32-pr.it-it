---
description: La nozione di blocco in un ambiente Windows è stata storicamente molto importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operazioni di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307039"
---
# <a name="blocking-operations"></a>Operazioni di blocco

La nozione di blocco in un ambiente Windows è stata storicamente molto importante. Negli ambienti Windows Sockets 1,1, le chiamate di blocco erano sconsigliate poiché tendevano a disabilitare l'interazione continuativa con il sistema. Inoltre, utilizzano una tecnica pseudoblocking che, per diversi motivi, non sempre funziona come previsto. Tuttavia, negli ambienti Windows preventivamente pianificati, le chiamate di blocco sono molto più sensate, possono essere implementate dai servizi del sistema operativo nativo e sono in realtà un meccanismo preferenziale. L'API Winsock 2 non supporta più psuedoblocking, ma poiché gli shim di compatibilità di Windows Sockets 1,1 devono continuare a emulare questo comportamento, i provider di servizi devono supportare questo comportamento come descritto di seguito.

 

 



