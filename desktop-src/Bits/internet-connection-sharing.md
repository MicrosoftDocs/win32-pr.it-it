---
title: Condivisione connessione Internet
description: BITS può forzare una connessione remota per le reti domestiche che usano Condivisione connessione Internet Microsoft se Condivisione connessione è configurata per la connessione remota quando i computer della rete accedono a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8736144b74d12666c4a364ac5b644ead35f8d1ec28aa03926bb7b691c8218f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588621"
---
# <a name="internet-connection-sharing"></a>Condivisione connessione Internet

BITS può forzare una connessione remota per le reti domestiche che usano Condivisione connessione Internet Microsoft se Condivisione connessione è configurata per la connessione remota quando i computer della rete accedono a Internet. Per impedire una connessione remota forzata, disabilitare l'opzione Stabilire una connessione remota ogni volta che un computer della rete tenta di accedere a **Internet** nel computer host di Condivisione connessione che condivide la connessione Internet.

I computer connessi al computer host di Condivisione connessione presuppongono di avere una connessione di rete, quindi BITS tenterà di trasferire i file. Se l'opzione di connessione remota è disabilitata nel computer host e il computer host non dispone di una connessione attiva, i trasferimenti avranno esito negativo con un errore temporaneo. BITS ripeterà periodicamente i trasferimenti.

 

 




