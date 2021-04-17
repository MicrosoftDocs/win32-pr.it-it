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
# <a name="prerequisites-for-installing-a-schema-extension"></a><span data-ttu-id="dabeb-103">Prerequisiti per l'installazione di un'estensione dello schema</span><span class="sxs-lookup"><span data-stu-id="dabeb-103">Prerequisites for Installing a Schema Extension</span></span>

<span data-ttu-id="dabeb-104">Per modificare lo schema, assicurarsi di disporre dei diritti seguenti e di conoscere le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="dabeb-104">To modify the schema, ensure you have the following rights and are aware of the following information:</span></span>

-   <span data-ttu-id="dabeb-105">È necessario disporre di diritti sufficienti per modificare lo schema.</span><span class="sxs-lookup"><span data-stu-id="dabeb-105">You must have sufficient rights to modify the schema.</span></span> <span data-ttu-id="dabeb-106">Lo schema contiene tutte le definizioni dei dati per Active Directory Domain Services per l'intera azienda.</span><span class="sxs-lookup"><span data-stu-id="dabeb-106">The schema contains all of the data definitions for Active Directory Domain Services for the entire enterprise.</span></span> <span data-ttu-id="dabeb-107">Per aggiornare lo schema, è necessario che un utente sia membro del gruppo Schema Administrators oppure che disponga dei diritti necessari per aggiornare lo schema.</span><span class="sxs-lookup"><span data-stu-id="dabeb-107">To update the schema, a user must be a member of the Schema Administrators group, or have been delegated the rights to update the schema.</span></span>
-   <span data-ttu-id="dabeb-108">È possibile apportare modifiche allo schema solo nel master schema.</span><span class="sxs-lookup"><span data-stu-id="dabeb-108">You can only make schema changes at the schema master.</span></span> <span data-ttu-id="dabeb-109">Per ulteriori informazioni, vedere [rilevamento del master schema](detecting-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="dabeb-109">For more information, see [Detecting the Schema Master](detecting-the-schema-master.md).</span></span>
-   <span data-ttu-id="dabeb-110">Il master schema deve essere scrivibile. ovvero è necessario rimuovere l'interblocco di sicurezza nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dabeb-110">The schema master must be writable; that is, the safety interlock in the registry must be removed.</span></span> <span data-ttu-id="dabeb-111">Per ulteriori informazioni, vedere [Abilitazione delle modifiche dello schema nel master schema](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="dabeb-111">For more information, see [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
-   <span data-ttu-id="dabeb-112">Per ulteriori informazioni su come verificare se il master schema può essere modificato e su come modificarne le impostazioni, vedere "XADM: Impossibile aggiornare lo schema sul proprietario dello schema" nella Knowledge base della guida e supporto tecnico all'indirizzo [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span><span class="sxs-lookup"><span data-stu-id="dabeb-112">For more information about how to check whether the schema master can be modified, and how to change its settings, see "XADM: Unable to Update the Schema on the Schema Owner" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span></span>

 

 




