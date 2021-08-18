---
title: Prerequisiti per l'installazione di un'estensione dello schema
description: Per modificare lo schema, assicurarsi di disporre dei diritti seguenti e di essere a conoscenza delle informazioni seguenti. È necessario disporre di diritti sufficienti per modificare lo schema.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af50626d452c8e26cbf1e7d33addfcea4f854cd2b40b0860bb98c783044748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185303"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>Prerequisiti per l'installazione di un'estensione dello schema

Per modificare lo schema, assicurarsi di disporre dei diritti seguenti e di essere a conoscenza delle informazioni seguenti:

-   È necessario disporre di diritti sufficienti per modificare lo schema. Lo schema contiene tutte le definizioni di dati per Active Directory Domain Services per l'intera organizzazione. Per aggiornare lo schema, è necessario che un utente sia membro del gruppo Amministratori schema o che siano stati delegati i diritti per aggiornare lo schema.
-   È possibile apportare modifiche allo schema solo nel master schema. Per altre informazioni, vedere [Rilevamento del master schema](detecting-the-schema-master.md).
-   Il master dello schema deve essere scrivibile. ciò significa che l'interlock di sicurezza nel Registro di sistema deve essere rimosso. Per altre informazioni, vedere [Abilitazione delle modifiche dello schema nel master schema](enabling-schema-changes-at-the-schema-master.md).
-   Per altre informazioni su come verificare se il master dello schema può essere modificato e su come modificarne le impostazioni, vedere "XADM: Unable to Update the Schema on the Schema Owner" (XADM: Impossibile aggiornare lo schema nel proprietario dello schema) nella guida e supporto tecnico Knowledge Base all'indirizzo [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




