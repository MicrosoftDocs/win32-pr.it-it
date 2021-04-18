---
title: Autodial RAS
description: Funzionalità denominata \ 0034; connessione predefinita \ 0034; è stato aggiunto al sistema in Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Autodial, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298809"
---
# <a name="ras-autodial"></a>Autodial RAS

Una funzionalità denominata "connessione predefinita" è stata aggiunta al sistema in Windows XP. Se si verifica un tentativo di connessione non riuscito, il sistema verifica la presenza di una corrispondenza esplicita (per nome o nome di condivisione Winsock) nel database, in caso contrario, compone la connessione predefinita se presente.

**Windows 2000:** Quando un tentativo di connessione a un indirizzo di rete non riesce perché non è possibile raggiungere l'host, la funzionalità Autodial può avviare automaticamente un'operazione di connessione remota. A tale scopo, Autodial Cerca nel database gli indirizzi di rete per trovare una voce di rubrica che può usare per stabilire la connessione.

**Windows NT 4,0:  ** RAS mantiene un database dei nomi e/o delle condivisioni Winsock che sono stati raggiunti correttamente mentre era attiva una connessione RAS/VPN. In un secondo momento, quando un tentativo di connessione Winsock o condivisione non riesce, il sistema controlla questo database e offre la connessione automatica alla connessione archiviata.

 

 




