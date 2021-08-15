---
title: Attributi dell'oggetto utente
description: Un oggetto utente ha più attributi. Questa sezione documenta gli attributi chiave usati da Windows, strumenti di amministrazione e Windows Rubrica (WAB). Non descrive tutti gli attributi. molti attributi non vengono usati per l'oggetto utente.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Attributi dell'oggetto utente AD
- Utenti AD , Attributi dell'oggetto utente
- Oggetti AD, utente, attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1bb6b347bd55daceb07dfe1fad4adc3e1352afc91ec14018aab6b24615c2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182630"
---
# <a name="user-object-attributes"></a>Attributi dell'oggetto utente

Un oggetto utente ha più attributi. Questa sezione documenta gli attributi chiave usati da Windows, strumenti di amministrazione e Windows Rubrica (WAB). Non descrive tutti gli attributi. molti attributi non vengono usati per l'oggetto utente.

Alcuni attributi vengono archiviati nella directory, ad esempio [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)e così via, e replicati in tutti i controller di dominio all'interno di un dominio. Un subset di questi attributi viene replicato anche nel catalogo globale.

Gli attributi non replicati vengono archiviati in ogni controller di dominio, ma non vengono replicati altrove, ad esempio [**badPwdCount,**](/windows/desktop/ADSchema/a-badpwdcount) [**lastLogon,**](/windows/desktop/ADSchema/a-lastlogon) [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)e così via. Gli attributi non replicati sono attributi che riguardano un controller di dominio specifico. Ad esempio, **lastLogon** è l'ultima data e ora in cui l'accesso alla rete dell'utente è stato convalidato dal controller di dominio specifico che restituisce la proprietà .

Un oggetto utente ha anche attributi costruiti che non sono archiviati nella directory, ma vengono calcolati dal controller di dominio, ad esempio [**canonicalName,**](/windows/desktop/ADSchema/a-canonicalname) [**distinguishedName,**](/windows/desktop/ADSchema/a-distinguishedname) [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes)e così via.

Gli attributi per gli oggetti utente sono classificati come:

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Attributi dell'oggetto di base
</dt> <dd>

Questa categoria include gli attributi necessari per tutti gli oggetti directory, ad esempio [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e così via.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Attributi di denominazione
</dt> <dd>

Questa categoria include gli attributi usati per fare riferimento o identificare l'oggetto, ad esempio [**distinguishedName,**](/windows/desktop/ADSchema/a-distinguishedname) [**objectGUID,**](/windows/desktop/ADSchema/a-objectguid) [**objectSID**](/windows/desktop/ADSchema/a-objectsid)e così via. Per altre informazioni sulla denominazione degli attributi per gli oggetti utente, vedere [Attributi di denominazione utente](naming-properties.md).

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Attributi di sicurezza
</dt> <dd>

Questa categoria include gli attributi per l'accesso e il controllo di accesso. Per altre informazioni sugli attributi di sicurezza per gli oggetti utente, vedere [Attributi di sicurezza utente](security-properties.md).

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Rubrica attributi
</dt> <dd>

Questa categoria include gli attributi per la posta elettronica e i dati utente. Per altre informazioni sugli attributi della rubrica per gli oggetti utente, vedere Attributi Rubrica [utente](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Attributi specifici dell'applicazione
</dt> <dd>

Questa categoria include i dati di configurazione specifici dell'utente per applicazioni specifiche.

</dd> </dl>

Per altre informazioni sulla lettura e la modifica degli attributi per un oggetto utente, vedere Lettura e scrittura di attributi di [oggetti in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Per altre informazioni sulla classe User, incluso un elenco completo degli attributi [**mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) della classe, vedere [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Impostazione delle password

La password per un utente non può essere modificata direttamente perché ciò comporterebbe l'invio di una password non crittografata in rete. Per impostare la password per un utente, è necessario usare il metodo [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) o [**IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) Il **metodo IADsUser.ChangePassword** viene usato quando l'applicazione consente all'utente di modificare la propria password. Il **metodo IADsUser.SetPassword** viene usato quando l'applicazione consente a un amministratore di reimpostare una password.

 

 