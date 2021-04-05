---
title: Ottenere un ID di collegamento
description: A partire da Windows Server 2003, non è più necessario richiedere un linkID da Microsoft; è disponibile un processo per la generazione automatica di un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Ottenere un ID di collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117550"
---
# <a name="obtaining-a-link-id"></a><span data-ttu-id="7ed4b-104">Ottenere un ID di collegamento</span><span class="sxs-lookup"><span data-stu-id="7ed4b-104">Obtaining a Link ID</span></span>

<span data-ttu-id="7ed4b-105">A partire da Windows Server 2003, non è più necessario richiedere un [**LinkId**](/windows/desktop/ADSchema/a-linkid) da Microsoft; è disponibile un processo per la generazione automatica di un **LinkId**.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-105">Starting with Windows Server 2003, it is no longer necessary to request a [**linkID**](/windows/desktop/ADSchema/a-linkid) from Microsoft; there is a process for automatically generating a **linkID**.</span></span> <span data-ttu-id="7ed4b-106">Il sistema genererà automaticamente un ID collegamento per un nuovo attributo collegato quando l'attributo **LinkId** dell'attributo viene impostato su 1.2.840.113556.1.2.50.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-106">The system will automatically generate a link ID for a new linked attribute when the attribute's **linkID** attribute is set to 1.2.840.113556.1.2.50.</span></span> <span data-ttu-id="7ed4b-107">Viene creato un collegamento indietro per questo collegamento in diretta impostando **LinkId** su [**attributeId**](/windows/desktop/ADSchema/a-attributeid) o [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) del collegamento in diretta.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-107">A back link for this forward link is created by setting the **linkID** to the [**attributeID**](/windows/desktop/ADSchema/a-attributeid) or [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) of the forward link.</span></span> <span data-ttu-id="7ed4b-108">La cache dello schema deve essere ricaricata dopo aver creato il collegamento in diretta e prima di creare il collegamento indietro.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-108">The schema cache must be reloaded after creating the forward link and before creating the back link.</span></span> <span data-ttu-id="7ed4b-109">In caso contrario, l'elemento **attributeId** o **ldapDisplayName** del collegamento diretto non verrà trovato quando viene creato il collegamento indietro.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-109">Otherwise, the forward link's **attributeId** or **ldapDisplayName** will not be found when the back link is created.</span></span> <span data-ttu-id="7ed4b-110">La cache dello schema viene ricaricata su richiesta, pochi minuti dopo che è stata apportata una modifica dello schema o quando il controller di dominio viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-110">The schema cache is reloaded on demand, a few minutes after a schema change is made, or when the DC is restarted.</span></span> <span data-ttu-id="7ed4b-111">Creare tutti i collegamenti in secondo piano, ricaricare la cache dello schema e quindi creare tutti i collegamenti indietro.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-111">Create all forward links, reload the schema cache and then create all back links.</span></span>

<span data-ttu-id="7ed4b-112">Ad esempio, quando sono stati creati i nuovi attributi **myForwardLinkAttr** e **myBackLinkAttr** e si desidera collegarli:</span><span class="sxs-lookup"><span data-stu-id="7ed4b-112">For example, when you have created the new attributes **myForwardLinkAttr** and **myBackLinkAttr**, and wish to link them:</span></span>

> [!Note]  
> <span data-ttu-id="7ed4b-113">Il OID in questo esempio è escogitato.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-113">The OIDs in this example are contrived.</span></span> <span data-ttu-id="7ed4b-114">Per istruzioni su come ottenere OID per i nuovi attributi, vedere [ottenere un identificatore di oggetto da Microsoft](obtaining-an-object-identifier-from-microsoft.md) .</span><span class="sxs-lookup"><span data-stu-id="7ed4b-114">See [Obtaining an Object Identifier from Microsoft](obtaining-an-object-identifier-from-microsoft.md) for instructions on obtaining OIDs for new attributes.</span></span>

 

1.  <span data-ttu-id="7ed4b-115">Impostare questi attributi sull'attributo che deve essere il collegamento in avanti:</span><span class="sxs-lookup"><span data-stu-id="7ed4b-115">Set these attributes on the attribute that is to be the forward link:</span></span>
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  <span data-ttu-id="7ed4b-116">Ricaricare lo schema.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-116">Reload the Schema.</span></span>
3.  <span data-ttu-id="7ed4b-117">Impostare questi attributi sull'attributo che deve essere il collegamento indietro:</span><span class="sxs-lookup"><span data-stu-id="7ed4b-117">Set these attributes on the attribute that is to be the back link:</span></span>
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a><span data-ttu-id="7ed4b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ed4b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed4b-119">Attributi collegati</span><span class="sxs-lookup"><span data-stu-id="7ed4b-119">Linked Attributes</span></span>](linked-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ed4b-120">Come estendere lo schema</span><span class="sxs-lookup"><span data-stu-id="7ed4b-120">How to Extend the Schema</span></span>](how-to-extend-the-schema.md)
</dt> </dl>

 

 