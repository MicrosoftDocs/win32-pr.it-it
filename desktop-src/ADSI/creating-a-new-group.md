---
title: Creazione di un nuovo gruppo
description: Joe Worden, amministratore dell'organizzazione, deve creare un nuovo gruppo.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3f778e9eb953b60ca45665bcd92ff30efb9c111c959e78cf1824407d0a459c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962010"
---
# <a name="creating-a-new-group"></a>Creazione di un nuovo gruppo

Joe Worden, amministratore dell'organizzazione, deve creare un nuovo gruppo. Desidera proteggere alcune risorse, ad esempio file, oggetti Active Directory o altri oggetti, in base all'appartenenza di questo gruppo. Nell'esempio di codice seguente viene illustrato come creare un nuovo gruppo.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Questo gruppo, Gestione, verrà creato nell'unità organizzativa Sales. Per prima cosa, Joe deve creare un oggetto ADSI per l'unità organizzativa Sales. In secondo piano, deve impostare [**l'attributo samAccountName**](/windows/desktop/AD/group-objects) su questo oggetto, perché è un attributo obbligatorio per la compatibilità con le versioni precedenti. Per questo esempio, quando **samAccountName** è impostato, Windows NT strumenti 4.0 come User Manager vedono l'attributo **come mgmt** anziché **come Management**.

In terzo piano, Joe deve specificare il tipo di gruppo. In un Windows 2000 sono disponibili tre tipi di gruppi: Globale, Locale di dominio e Universale. Inoltre, il gruppo presenta la propria caratteristica di sicurezza. Un gruppo può essere abilitato per la sicurezza o non protetto. Essenzialmente, i gruppi abilitati per la sicurezza sono quelli a cui è possibile concedere o negare diritti di accesso alle risorse, in modo simile a un utente. Concedere a un gruppo l'accesso a una condivisione file, ad esempio, implica che tutti i membri del gruppo possono accedere alla condivisione file. Le liste di distribuzione non possono essere usate in modo simile, ad esempio non è possibile concedere a una lista di distribuzione il diritto di accedere a una condivisione file. Durante l'aggiornamento, Windows NT gruppi 4.0 vengono migrati come gruppi abilitati per la sicurezza. I gruppi non protetti in Active Directory sono simili alle liste di distribuzione in Exchange. Di conseguenza, la creazione di gruppi o liste di distribuzione è un'operazione simile Windows 2000. Nella modalità nativa Windows 2000 (la modalità nativa indica che tutti i controller di dominio in un dominio sono computer che eseguono Windows 2000 Server), i gruppi possono essere annidati a qualsiasi livello.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione di oggetti](enumerating-objects.md)
</dt> </dl>

 

 