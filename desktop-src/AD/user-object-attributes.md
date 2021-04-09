---
title: Attributi dell'oggetto utente
description: Un oggetto utente dispone di più attributi. Questa sezione illustra gli attributi chiave usati da Windows, strumenti di amministrazione e la Rubrica di Windows (WAB). Non descrive tutti gli attributi. molti attributi non vengono usati per l'oggetto utente.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- AD degli attributi degli oggetti utente
- Utenti AD, attributi degli oggetti utente
- Oggetti AD, utente, attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956295"
---
# <a name="user-object-attributes"></a>Attributi dell'oggetto utente

Un oggetto utente dispone di più attributi. Questa sezione illustra gli attributi chiave usati da Windows, strumenti di amministrazione e la Rubrica di Windows (WAB). Non descrive tutti gli attributi. molti attributi non vengono usati per l'oggetto utente.

Alcuni attributi vengono archiviati nella directory, ad esempio [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)e così via, e replicati in tutti i controller di dominio all'interno di un dominio. Un subset di questi attributi viene inoltre replicato nel catalogo globale.

Gli attributi non replicati vengono archiviati in ogni controller di dominio, ma non vengono replicati altrove, ad esempio [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**LastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**LastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)e così via. Gli attributi non replicati sono attributi che riguardano un particolare controller di dominio. Ad esempio, **LastLogon** è l'ultima data e ora in cui l'accesso alla rete utente è stato convalidato dal particolare controller di dominio che restituisce la proprietà.

Un oggetto utente dispone inoltre di attributi costruiti che non sono archiviati nella directory, ma vengono calcolati dal controller di dominio, ad esempio [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**Distinguishname**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes)e così via.

Gli attributi per gli oggetti utente sono classificati come:

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Attributi dell'oggetto di base
</dt> <dd>

Questa categoria include gli attributi necessari per tutti gli oggetti directory, ad esempio [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e così via.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Attributi di denominazione
</dt> <dd>

Questa categoria include attributi usati per fare riferimento a o identificare l'oggetto, ad esempio [**Distinguishname**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid)e così via. Per ulteriori informazioni sulla denominazione degli attributi degli oggetti utente, vedere [attributi di denominazione degli utenti](naming-properties.md).

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Attributi di sicurezza
</dt> <dd>

Questa categoria include gli attributi per il controllo di accesso e accesso. Per ulteriori informazioni sugli attributi di sicurezza per gli oggetti utente, vedere [attributi di sicurezza utente](security-properties.md).

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Attributi Rubrica
</dt> <dd>

Questa categoria include gli attributi per la posta elettronica e i dati utente. Per ulteriori informazioni sugli attributi degli indirizzi Rubrica per gli oggetti utente, vedere attributi della rubrica [utente](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Attributi specifici dell'applicazione
</dt> <dd>

Questa categoria include i dati di configurazione specifici dell'utente per applicazioni specifiche.

</dd> </dl>

Per ulteriori informazioni sulla lettura e la modifica degli attributi per un oggetto utente, vedere [lettura e scrittura degli attributi degli oggetti in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Per ulteriori informazioni sulla classe utente, incluso un elenco completo degli attributi [**mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) della classe, vedere [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Impostazione delle password

Non è possibile modificare direttamente la password di un utente perché questa operazione comporterebbe l'invio di una password non crittografata sulla rete. Per impostare la password per un utente, è necessario usare il metodo [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) o [**IADsUser. sepassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Il metodo **IADsUser. ChangePassword** viene utilizzato quando l'applicazione consente all'utente di modificare la propria password. Il metodo **IADsUser. sepassword** viene utilizzato quando l'applicazione consente a un amministratore di reimpostare una password.

 

 