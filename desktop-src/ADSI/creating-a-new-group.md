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
# <a name="creating-a-new-group"></a><span data-ttu-id="2d5cf-103">Creazione di un nuovo gruppo</span><span class="sxs-lookup"><span data-stu-id="2d5cf-103">Creating a New Group</span></span>

<span data-ttu-id="2d5cf-104">Joe worden, l'amministratore dell'organizzazione, deve creare un nuovo gruppo.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-104">Joe Worden, the enterprise administrator, must create a new group.</span></span> <span data-ttu-id="2d5cf-105">Desidera proteggere alcune risorse, ad esempio file, Active Directory oggetti o altri oggetti, in base all'appartenenza di questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-105">He would like to secure some resources, such as file, Active Directory objects, or other objects, based on the membership of this group.</span></span> <span data-ttu-id="2d5cf-106">Nell'esempio di codice seguente viene illustrato come creare un nuovo gruppo.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-106">The following code example shows how to create a new group.</span></span>


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



<span data-ttu-id="2d5cf-107">Questo gruppo di gestione verrà creato nell'unità organizzativa Sales.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-107">This group, Management, will be created in the Sales organizational unit.</span></span> <span data-ttu-id="2d5cf-108">In primo luogo, Joe deve creare un oggetto ADSI per l'unità organizzativa Sales.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-108">First, Joe must create an ADSI object for the Sales organizational unit.</span></span> <span data-ttu-id="2d5cf-109">In secondo luogo, deve impostare l'attributo [**sAMAccountName**](/windows/desktop/AD/group-objects) per questo oggetto, perché è un attributo obbligatorio per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-109">Second, he must set the [**samAccountName**](/windows/desktop/AD/group-objects) attribute on this object, because it is a mandatory attribute for backward compatibility.</span></span> <span data-ttu-id="2d5cf-110">Per questo esempio, quando si imposta **sAMAccountName** , gli strumenti di Windows NT 4,0, ad esempio gestione utenti, visualizzano l'attributo come **Mgmt** anziché **gestione**.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-110">For this example, when **samAccountName** is set, Windows NT 4.0 tools such as User Manager see the attribute as **mgmt** instead of **Management**.</span></span>

<span data-ttu-id="2d5cf-111">In terzo luogo, Joe deve specificare il tipo di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-111">Third, Joe must specify the type of group.</span></span> <span data-ttu-id="2d5cf-112">In un dominio Windows 2000 sono disponibili tre tipi di gruppi: globale, locale di dominio e universale.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-112">In a Windows 2000 domain, there are three types of groups: Global, Domain Local, and Universal.</span></span> <span data-ttu-id="2d5cf-113">Inoltre, il gruppo trasporta le sue caratteristiche di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-113">In addition, the group carries its security characteristic.</span></span> <span data-ttu-id="2d5cf-114">Un gruppo può essere un gruppo abilitato per la sicurezza o non protetto.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-114">A group can be either a security-enabled or a non-secured group.</span></span> <span data-ttu-id="2d5cf-115">In sostanza, i gruppi abilitati per la sicurezza sono quelli a cui è possibile concedere o negare i diritti di accesso alle risorse, in modo analogo a un utente.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-115">Essentially, security-enabled groups are those that can be granted or denied access rights to resources, similar to a user.</span></span> <span data-ttu-id="2d5cf-116">Se si concede a un gruppo l'accesso a una condivisione file, ad esempio, si presuppone che tutti i membri del gruppo possano accedere alla condivisione file.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-116">Granting a group access to a file share, for example, implies that all members of the group can access the file share.</span></span> <span data-ttu-id="2d5cf-117">Le liste di distribuzione non possono essere usate in modo analogo, non è possibile, ad esempio, concedere a un elenco di distribuzione il diritto di accedere a una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-117">Distribution lists cannot be used in a similar manner—you cannot, for example, grant a distribution list the right to access a file share.</span></span> <span data-ttu-id="2d5cf-118">Durante l'aggiornamento, viene eseguita la migrazione dei gruppi di Windows NT 4,0 come gruppi abilitati per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-118">During the upgrade, Windows NT 4.0 groups are migrated as security-enabled groups.</span></span> <span data-ttu-id="2d5cf-119">I gruppi non protetti in Active Directory sono simili alle liste di distribuzione in Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-119">Non-secured groups in Active Directory are similar to distribution lists in Exchange.</span></span> <span data-ttu-id="2d5cf-120">Di conseguenza, la creazione di gruppi o liste di distribuzione è operazioni simili in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-120">Hence, creating groups or distribution lists are similar operations in Windows 2000.</span></span> <span data-ttu-id="2d5cf-121">In modalità nativa di Windows 2000 (modalità nativa significa che tutti i controller di dominio in un dominio sono computer che eseguono Windows 2000 Server), i gruppi possono essere annidati a qualsiasi livello.</span><span class="sxs-lookup"><span data-stu-id="2d5cf-121">In the Windows 2000 native mode (native mode means that all domain controllers in a domain are computers running Windows 2000 Server), the groups can be nested to any level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d5cf-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d5cf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d5cf-123">Enumerazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="2d5cf-123">Enumerating Objects</span></span>](enumerating-objects.md)
</dt> </dl>

 

 