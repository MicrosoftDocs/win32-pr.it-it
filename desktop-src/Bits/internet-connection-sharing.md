---
title: Condivisione connessione Internet
description: BITS può forzare una connessione remota per le reti domestiche che usano Microsoft Internet sharing se la condivisione della connessione è configurata per la connessione quando i computer nella rete accedono a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707840"
---
# <a name="internet-connection-sharing"></a>Condivisione connessione Internet

BITS può forzare una connessione remota per le reti domestiche che usano Microsoft Internet sharing se la condivisione della connessione è configurata per la connessione quando i computer nella rete accedono a Internet. Per evitare una connessione remota forzata, disabilitare la **connessione remota ogni volta che un computer della rete tenta di accedere all'opzione Internet** nel computer host di condivisione della connessione che condivide la connessione Internet.

I computer connessi al computer host che condivide la connessione presuppongono che dispongano di una connessione di rete, quindi BITS tenterà di trasferire i file. Se l'opzione di connessione remota è disabilitata nel computer host e il computer host non dispone di una connessione attiva, i trasferimenti avranno esito negativo con un errore temporaneo. BITS tenterà periodicamente di eseguire i trasferimenti.

 

 




