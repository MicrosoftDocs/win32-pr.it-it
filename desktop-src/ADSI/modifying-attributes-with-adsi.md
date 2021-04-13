---
title: Modifica degli attributi con ADSI
description: Per modificare i valori degli attributi, ADSI fornisce i metodi IADs. Put e IADs. PutEx. Questi metodi modificano i dati nella cache sul lato client. È necessario chiamare il metodo IADs. SetInfo per eseguire il commit delle modifiche nella directory.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modifica degli attributi con ADSI
- Attributi ADSI, modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399721"
---
# <a name="modifying-attributes-with-adsi"></a><span data-ttu-id="228d0-107">Modifica degli attributi con ADSI</span><span class="sxs-lookup"><span data-stu-id="228d0-107">Modifying Attributes with ADSI</span></span>

<span data-ttu-id="228d0-108">Per modificare i valori degli attributi, ADSI fornisce i metodi [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="228d0-108">To modify attribute values, ADSI provides the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) methods.</span></span> <span data-ttu-id="228d0-109">Questi metodi modificano i dati nella cache sul lato client.</span><span class="sxs-lookup"><span data-stu-id="228d0-109">These methods modify the data on the client-side cache.</span></span> <span data-ttu-id="228d0-110">È necessario chiamare il metodo [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) per eseguire il commit delle modifiche nella directory.</span><span class="sxs-lookup"><span data-stu-id="228d0-110">The [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method must be called to commit the changes to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="228d0-111">Quando si esegue il commit di più modifiche di attributo in una singola chiamata a [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), se non è possibile modificare un singolo attributo, nessuno degli attributi verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="228d0-111">When multiple attribute changes are committed in a single call to [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), if any single attribute cannot be modified, none of the attributes will be modified.</span></span> <span data-ttu-id="228d0-112">Se, ad esempio, si modificano gli attributi [**sn**](/windows/desktop/ADSchema/a-sn) e [**given**](/windows/desktop/ADSchema/a-givenname) e si cancella l'attributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) di un oggetto utente senza alcuna chiamata successiva al metodo **seinfo** , le modifiche vengono immesse quando si chiama **seinfo**.</span><span class="sxs-lookup"><span data-stu-id="228d0-112">For example, if you modify the [**sn**](/windows/desktop/ADSchema/a-sn) and [**givenName**](/windows/desktop/ADSchema/a-givenname) attributes and clear the [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) attribute of a user object without any subsequent calls to the **SetInfo** method, the changes are entered when you call **SetInfo**.</span></span> <span data-ttu-id="228d0-113">Se una o più delle modifiche non sono consentite e pertanto non possono essere eseguite, nessuna delle modifiche collettive apportate agli attributi viene immessa durante la chiamata a **seinfo**.</span><span class="sxs-lookup"><span data-stu-id="228d0-113">If one or more of the modifications are not allowed and therefore cannot be performed, then none of the collective modifications made to the attributes are entered during the call to **SetInfo**.</span></span>

 

<span data-ttu-id="228d0-114">Il metodo [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) accetta un nome di attributo e un parametro Variant.</span><span class="sxs-lookup"><span data-stu-id="228d0-114">The [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method takes an attribute name and a variant parameter.</span></span> <span data-ttu-id="228d0-115">Utilizzare questo metodo per impostare attributi che contengono valori singoli e multipli.</span><span class="sxs-lookup"><span data-stu-id="228d0-115">Use this method to set attributes that contain both single and multiple values.</span></span>

<span data-ttu-id="228d0-116">Il metodo [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) fornisce il controllo sulle operazioni sugli attributi multivalore.</span><span class="sxs-lookup"><span data-stu-id="228d0-116">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method provides control over operations on multi-valued attributes.</span></span> <span data-ttu-id="228d0-117">È possibile accodare, eliminare, aggiornare e cancellare i valori esistenti.</span><span class="sxs-lookup"><span data-stu-id="228d0-117">You can append, delete, update, and clear existing values.</span></span> <span data-ttu-id="228d0-118">Il metodo **IADs. PutEx** prevede sempre una matrice Variant di valori di attributo.</span><span class="sxs-lookup"><span data-stu-id="228d0-118">The **IADs.PutEx** method always expects a variant array of attribute values.</span></span> <span data-ttu-id="228d0-119">Tuttavia, è possibile usare questo metodo per impostare anche un attributo con un valore singolo.</span><span class="sxs-lookup"><span data-stu-id="228d0-119">However, you can use this method to set an attribute with a single value as well.</span></span>

<span data-ttu-id="228d0-120">Il metodo [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa le operazioni specificate dall'enumerazione [**\_ enum dell' \_ operazione \_ della proprietà ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="228d0-120">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the operations specified by the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

 

 