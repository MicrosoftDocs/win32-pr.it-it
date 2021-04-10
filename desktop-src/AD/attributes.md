---
title: Attributi (AD DS)
description: Ogni oggetto in Active Directory Domain Services contiene un set di attributi che definiscono le caratteristiche dell'oggetto.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- attributi AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046558"
---
# <a name="attributes-ad-ds"></a>Attributi (AD DS)

Ogni oggetto in Active Directory Domain Services contiene un set di attributi che definiscono le caratteristiche dell'oggetto. Ogni attributo è descritto da un oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) nel contenitore dello schema che definisce l'attributo. La definizione dell'attributo include una varietà di dati, ad esempio i tipi di oggetto a cui si applica l'attributo e il tipo di sintassi dell'attributo. Per ulteriori informazioni sulle definizioni dello schema degli attributi, vedere [caratteristiche degli attributi](characteristics-of-attributes.md).

Nell'elenco seguente sono elencati i tipi di attributi archiviati in Active Directory Domain Services.

<dl> <dt>

<span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Attributi archiviati con replica di dominio
</dt> <dd>

Alcuni attributi vengono archiviati nella directory, ad esempio [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), e replicati in tutti i controller di dominio di un dominio. Un subset di questi attributi viene inoltre replicato nel catalogo globale. Se si enumerano gli attributi di un oggetto dal catalogo globale, vengono restituiti solo gli attributi replicati nel catalogo globale. Alcuni attributi vengono indicizzati anche perché l'inclusione di una proprietà indicizzata in una query migliora le prestazioni di esecuzione delle query.

</dd> <dt>

<span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Attributi archiviati localmente non replicati
</dt> <dd>

Gli attributi non replicati, ad esempio [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon)e [**Last-disconnessione**](/windows/desktop/ADSchema/a-lastlogoff) , vengono archiviati in ogni controller di dominio, ma non vengono replicati. Gli attributi non replicati sono attributi che riguardano un particolare controller di dominio. Ad esempio, l'attributo **Last-Logon** è l'ultima data e ora in cui l'accesso alla rete dell'utente è stato convalidato da quel particolare controller di dominio che ha restituito la proprietà. Questi attributi possono essere recuperati nello stesso modo degli attributi a livello di dominio descritti in precedenza. Tuttavia, per questi attributi, ogni controller di dominio archivia solo i valori che riguardano quel particolare controller di dominio. Ad esempio, per ottenere l'ultima volta in cui un utente ha effettuato l'accesso al dominio, recuperare l'attributo **Last-Logon** per l'utente da ogni controller di dominio nel dominio e individuare la data e l'ora più recenti.

</dd> <dt>

<span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Attributi non archiviati e costruiti
</dt> <dd>

Un oggetto utente dispone inoltre di attributi costruiti che non sono archiviati nella directory, ma vengono calcolati dal controller di dominio, ad esempio [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname) e [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).

</dd> </dl>

 

 