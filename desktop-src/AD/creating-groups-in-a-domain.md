---
title: Creazione di gruppi in un dominio
description: Un oggetto gruppo viene creato in Active Directory Domain Services nel contenitore del dominio in cui sarà contenuto il nuovo gruppo.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- gruppi AD, creazione di gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046534"
---
# <a name="creating-groups-in-a-domain"></a>Creazione di gruppi in un dominio

Un oggetto gruppo viene creato in Active Directory Domain Services nel contenitore del dominio in cui sarà contenuto il nuovo gruppo. I gruppi possono essere creati alla radice del dominio, all'interno di un'unità organizzativa o all'interno di un contenitore. Per creare un oggetto gruppo, usare il metodo [**IADsContainer:: create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) o [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

Gli attributi seguenti sono necessari per rendere l'oggetto gruppo un gruppo valido che verrà riconosciuto dal server Active Directory e dal sistema di sicurezza di Windows:

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**CN**
</dt> <dd>

Specifica il nome dell'oggetto gruppo nella directory. Si tratta del nome distinto relativo dell'oggetto all'interno del contenitore in cui viene creato il gruppo.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**
</dt> <dd>

Contiene un numero intero che specifica il tipo e l'ambito del gruppo. Il [**\_ tipo di gruppo Ads \_ \_ enum**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) Enumeration definisce i valori possibili per l'attributo **GroupType** .

Nell'elenco seguente vengono definiti i tipi e i valori di gruppo comuni per questo attributo.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribuzione locale di dominio
</dt> <dd>

**tipo di gruppo ADS gruppo \_ \_ \_ locale di dominio \_ \_**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Sicurezza locale di dominio
</dt> <dd>

**Annunci \_ tipo di gruppo \_ \_ dominio \_ locale \_** gruppo di \| **annunci \_ \_ \_ sicurezza \_ tipo** di gruppo abilitato

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribuzione globale
</dt> <dd>

**tipo di gruppo ADS gruppo \_ \_ \_ globale \_**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Sicurezza globale
</dt> <dd>

**Annunci \_ tipo di gruppo gruppo di annunci \_ \_ \_ gruppo globale** \| **\_ \_ \_ sicurezza \_ abilitata**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribuzione universale
</dt> <dd>

**\_gruppo Ads \_ tipo gruppo \_ universale \_**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Sicurezza universale
</dt> <dd>

**Annunci \_ \_tipo di \_ \_ gruppo** gruppi di annunci gruppo universale \| **\_ \_ \_ sicurezza \_ abilitata**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Se il gruppo è destinato a impostare il controllo di accesso per gli oggetti directory, il gruppo deve essere un gruppo di sicurezza globale o universale.

Tenere presente che i gruppi di sicurezza universali possono essere creati solo in domini Windows 2000 in esecuzione in modalità nativa. Per ulteriori informazioni sul rilevamento della modalità mista e nativa, vedere [rilevamento della modalità operativa di un dominio](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**
</dt> <dd>

Contiene una stringa che rappresenta il nome utilizzato per supportare client e server di una versione precedente. Il valore di **sAMAccountName** deve essere composto da meno di 20 caratteri per supportare i client di una versione precedente di Windows.

**SAMAccountName** deve essere univoco tra tutti gli oggetti entità di sicurezza all'interno del dominio. È necessario eseguire una query sul dominio per verificare che **sAMAccountName** sia univoco all'interno del dominio.

</dd> </dl>

I membri del gruppo possono essere aggiunti in fase di creazione usando il metodo [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . Facoltativamente, i membri possono essere aggiunti al gruppo dopo la creazione usando il metodo [**IADsGroup:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Per ulteriori informazioni sull'aggiunta di membri a un gruppo, vedere [aggiunta di membri a gruppi in un dominio](adding-members-to-groups-in-a-domain.md).

 

 