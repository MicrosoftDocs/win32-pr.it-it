---
title: Prerequisiti per l'installazione di un'estensione dello schema
description: Per modificare lo schema, assicurarsi di disporre dei diritti seguenti e di disporre dei diritti sufficienti per modificare lo schema.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104336458"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>Prerequisiti per l'installazione di un'estensione dello schema

Per modificare lo schema, assicurarsi di disporre dei diritti seguenti e di conoscere le seguenti informazioni:

-   È necessario disporre di diritti sufficienti per modificare lo schema. Lo schema contiene tutte le definizioni dei dati per Active Directory Domain Services per l'intera azienda. Per aggiornare lo schema, è necessario che un utente sia membro del gruppo Schema Administrators oppure che disponga dei diritti necessari per aggiornare lo schema.
-   È possibile apportare modifiche allo schema solo nel master schema. Per ulteriori informazioni, vedere [rilevamento del master schema](detecting-the-schema-master.md).
-   Il master schema deve essere scrivibile. ovvero è necessario rimuovere l'interblocco di sicurezza nel registro di sistema. Per ulteriori informazioni, vedere [Abilitazione delle modifiche dello schema nel master schema](enabling-schema-changes-at-the-schema-master.md).
-   Per ulteriori informazioni su come verificare se il master schema può essere modificato e su come modificarne le impostazioni, vedere "XADM: Impossibile aggiornare lo schema sul proprietario dello schema" nella Knowledge base della guida e supporto tecnico all'indirizzo [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




