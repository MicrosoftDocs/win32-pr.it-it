---
title: Operazioni di scrittura e controllo di accesso
description: Le modifiche alle proprietà hanno esito negativo se il chiamante non dispone di diritti sufficienti.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- AD Access Control e writer Operations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872238"
---
# <a name="access-control-and-write-operations"></a><span data-ttu-id="1bd6a-104">Operazioni di scrittura e controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="1bd6a-104">Access Control and Write Operations</span></span>

<span data-ttu-id="1bd6a-105">Le modifiche alle proprietà hanno esito negativo se il chiamante non dispone di diritti sufficienti.</span><span class="sxs-lookup"><span data-stu-id="1bd6a-105">Property modifications fail if the caller does not have sufficient rights.</span></span> <span data-ttu-id="1bd6a-106">Per le operazioni di scrittura che comportano la modifica in batch di più proprietà, l'intera operazione ha esito negativo se il chiamante non dispone dei diritti necessari per una sola delle proprietà modificate.</span><span class="sxs-lookup"><span data-stu-id="1bd6a-106">For write operations that batch modifications to multiple properties, the entire operation fails if the caller does not have the necessary rights to a single one of the modified properties.</span></span> <span data-ttu-id="1bd6a-107">È ad esempio possibile eseguire più chiamate [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) per impostare più proprietà in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1bd6a-107">For example, you can make multiple [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) calls to set multiple properties on an object.</span></span> <span data-ttu-id="1bd6a-108">Tuttavia, quando si chiama [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per scrivere i nuovi dati dalla cache locale alla directory, le **informazioni** non riusciranno se il chiamante non dispone dell'accesso in scrittura a tutte le proprietà modificate.</span><span class="sxs-lookup"><span data-stu-id="1bd6a-108">However, when you call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to write the new data from the local cache to the directory, **SetInfo** will fail if the caller does not have write access to all the modified properties.</span></span> <span data-ttu-id="1bd6a-109">Analogamente, il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) non è in grado di impostare alcuna proprietà se il chiamante non ha accesso a tutte le proprietà impostate.</span><span class="sxs-lookup"><span data-stu-id="1bd6a-109">Similarly, the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method fails to set any properties if the caller does not have access to all the properties being set.</span></span> <span data-ttu-id="1bd6a-110">Pertanto, è necessario raggruppare più operazioni di modifica solo se si è certi che tutte le modifiche verranno eseguite correttamente.</span><span class="sxs-lookup"><span data-stu-id="1bd6a-110">So you should batch multiple modify operations only if you know that all modifications will succeed.</span></span> <span data-ttu-id="1bd6a-111">Per determinare gli attributi di un oggetto directory che il chiamante è in grado di modificare, leggere l'attributo **allowedAttributesEffective** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1bd6a-111">To determine the attributes of a directory object that the caller has the ability to modify, read the object's **allowedAttributesEffective** attribute.</span></span>

<span data-ttu-id="1bd6a-112">Se il chiamante non dispone di diritti sufficienti per modificare una proprietà, è possibile che vengano restituiti i seguenti codici restituiti:</span><span class="sxs-lookup"><span data-stu-id="1bd6a-112">If the caller does not have sufficient rights to modify a property, the following return codes may be returned:</span></span>

<span data-ttu-id="1bd6a-113">proprietà \_ e \_ Ads \_ non \_ impostati e \_ \_ Proprietà Ads \_ non \_ modificata</span><span class="sxs-lookup"><span data-stu-id="1bd6a-113">E\_ADS\_PROPERTY\_NOT\_SET E\_ADS\_PROPERTY\_NOT\_MODIFIED</span></span>

 

 