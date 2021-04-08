---
title: Conversione di formati di nomi di account di dominio
description: Le funzioni Microsoft Win32 per l'utilizzo di gestione controllo servizi (SCM) in un server host utilizzano la 0034; dominio \\ nomeutente \ 0034; formato per gli account del servizio.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724607"
---
# <a name="converting-domain-account-name-formats"></a>Conversione di formati di nomi di account di dominio

Le funzioni Microsoft Win32 per l'utilizzo di gestione controllo servizi (SCM) in un server host utilizzano il <domain> \\ <username> formato "" per gli account del servizio. Se ad esempio si chiama la funzione [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) per recuperare l'account utente con cui viene eseguito il servizio, la funzione restituisce il nome nel formato "Fabrikam \\ SergioMelchiori". Per eseguire l'associazione all'account utente nella directory, ad esempio per modificare la password dell'account, il nome distinto dell'account è obbligatorio, il cui formato è "CN = Jeff Smith, CN = Users, DC = Fabrikam, DC = COM".

Per eseguire la conversione tra i vari formati dei nomi, usare la funzione [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) , che può convertire un nome in altri formati, ad esempio un nome dell'entità utente (UPN).

 

 