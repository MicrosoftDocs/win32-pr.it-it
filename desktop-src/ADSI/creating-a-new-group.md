---
title: Creazione di un nuovo gruppo
description: Joe worden, l'amministratore dell'organizzazione, deve creare un nuovo gruppo.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963463"
---
# <a name="creating-a-new-group"></a>Creazione di un nuovo gruppo

Joe worden, l'amministratore dell'organizzazione, deve creare un nuovo gruppo. Desidera proteggere alcune risorse, ad esempio file, Active Directory oggetti o altri oggetti, in base all'appartenenza di questo gruppo. Nell'esempio di codice seguente viene illustrato come creare un nuovo gruppo.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Questo gruppo di gestione verrà creato nell'unità organizzativa Sales. In primo luogo, Joe deve creare un oggetto ADSI per l'unità organizzativa Sales. In secondo luogo, deve impostare l'attributo [**sAMAccountName**](/windows/desktop/AD/group-objects) per questo oggetto, perché è un attributo obbligatorio per la compatibilità con le versioni precedenti. Per questo esempio, quando si imposta **sAMAccountName** , gli strumenti di Windows NT 4,0, ad esempio gestione utenti, visualizzano l'attributo come **Mgmt** anziché **gestione**.

In terzo luogo, Joe deve specificare il tipo di gruppo. In un dominio Windows 2000 sono disponibili tre tipi di gruppi: globale, locale di dominio e universale. Inoltre, il gruppo trasporta le sue caratteristiche di sicurezza. Un gruppo può essere un gruppo abilitato per la sicurezza o non protetto. In sostanza, i gruppi abilitati per la sicurezza sono quelli a cui è possibile concedere o negare i diritti di accesso alle risorse, in modo analogo a un utente. Se si concede a un gruppo l'accesso a una condivisione file, ad esempio, si presuppone che tutti i membri del gruppo possano accedere alla condivisione file. Le liste di distribuzione non possono essere usate in modo analogo, non è possibile, ad esempio, concedere a un elenco di distribuzione il diritto di accedere a una condivisione file. Durante l'aggiornamento, viene eseguita la migrazione dei gruppi di Windows NT 4,0 come gruppi abilitati per la sicurezza. I gruppi non protetti in Active Directory sono simili alle liste di distribuzione in Exchange. Di conseguenza, la creazione di gruppi o liste di distribuzione è operazioni simili in Windows 2000. In modalità nativa di Windows 2000 (modalità nativa significa che tutti i controller di dominio in un dominio sono computer che eseguono Windows 2000 Server), i gruppi possono essere annidati a qualsiasi livello.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione di oggetti](enumerating-objects.md)
</dt> </dl>

 

 