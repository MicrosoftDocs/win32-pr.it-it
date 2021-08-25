---
title: RAS AutoDial
description: Una funzionalità denominata \ 0034;connessione predefinita \ 0034; è stato aggiunto al sistema in Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- AutoDial, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7956148919505eb16d1fb2fe9bc045fa7ecbaa7e2959c430e15f8013ef372ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909871"
---
# <a name="ras-autodial"></a>RAS AutoDial

Una funzionalità denominata "connessione predefinita" è stata aggiunta al sistema in Windows XP. Se si verifica un tentativo di connessione non riuscito, il sistema verifica la presenza di una corrispondenza esplicita (per il nome Winsock o il nome di condivisione) nel database in caso contrario, viene stabilita la connessione predefinita, se presente.

**Windows 2000:** Quando un tentativo di connessione a un indirizzo di rete non riesce perché non è possibile raggiungere l'host, la funzionalità AutoDial può avviare automaticamente un'operazione di connessione remota. A tale scopo, AutoDial cerca nel database degli indirizzi di rete una voce della rubrica che può usare per stabilire la connessione.

**Windows NT 4.0: ** RAS mantiene un database dei nomi Winsock e/o dei nomi di condivisione raggiunti correttamente mentre era attiva una connessione RAS/VPN. In un secondo momento, quando un tentativo di connessione winsock o condivisione ha esito negativo, il sistema controlla questo database e offre di comporre automaticamente la connessione archiviata.

 

 




