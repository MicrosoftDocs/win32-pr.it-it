---
title: Conversione dei formati dei nomi di account di dominio
description: Le funzioni Microsoft Win32 per l'uso di Gestione controllo servizi in un server host usano \ 0034; nome \\ utente di dominio \ 0034; formato per gli account del servizio.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa1b3664cc0ad372f82b498153862e69013fb1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881598"
---
# <a name="converting-domain-account-name-formats"></a>Conversione dei formati dei nomi di account di dominio

Le funzioni Microsoft Win32 per l'uso di Gestione controllo servizi in un server host usano il formato " nome utente di dominio " per &lt; &gt; \\ &lt; gli account &gt; del servizio. Ad esempio, se si chiama la [**funzione QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) per recuperare l'account utente con cui viene eseguito il servizio, la funzione restituisce il nome nel formato "Fabrikam \\ jeffsmith". Per eseguire il binding all'account utente nella directory, ad esempio per modificare la password dell'account, è necessario il nome distinto dell'account, nel formato "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".

Per eseguire la conversione tra i vari formati di nome, usare la funzione [**TranslateName,**](/windows/desktop/api/secext/nf-secext-translatenamea) che può convertire un nome in altri formati, ad esempio un nome dell'entità utente (UPN).

 

 
