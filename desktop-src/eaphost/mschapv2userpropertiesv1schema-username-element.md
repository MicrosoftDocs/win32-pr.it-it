---
title: Elemento UserName (CHAP)
description: Informazioni sull'elemento username, che identifica l'utente che sta eseguendo l'autenticazione. Vedere un esempio di sintassi e visualizzare altre risorse disponibili.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Elemento Username EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963457"
---
# <a name="username-element-chap"></a><span data-ttu-id="8a38c-105">Elemento UserName (CHAP)</span><span class="sxs-lookup"><span data-stu-id="8a38c-105">Username element (CHAP)</span></span>

<span data-ttu-id="8a38c-106">L'elemento **username** identifica l'utente autenticato.</span><span class="sxs-lookup"><span data-stu-id="8a38c-106">The **Username** element identifies the user being authenticated.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a><span data-ttu-id="8a38c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a38c-107">Remarks</span></span>

<span data-ttu-id="8a38c-108">Se l'elemento **username** non è presente, il nome utente viene ottenuto da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="8a38c-108">If the **Username** element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="8a38c-109">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a38c-109">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a38c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a38c-110">Requirements</span></span>



| <span data-ttu-id="8a38c-111">Ruolo</span><span class="sxs-lookup"><span data-stu-id="8a38c-111">Role</span></span> | <span data-ttu-id="8a38c-112">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="8a38c-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="8a38c-113">Client</span><span class="sxs-lookup"><span data-stu-id="8a38c-113">Client</span></span><br/> | <span data-ttu-id="8a38c-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a38c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a38c-115">Server</span><span class="sxs-lookup"><span data-stu-id="8a38c-115">Server</span></span><br/> | <span data-ttu-id="8a38c-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a38c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a38c-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a38c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a38c-118">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="8a38c-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8a38c-119">Schema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="8a38c-119">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





