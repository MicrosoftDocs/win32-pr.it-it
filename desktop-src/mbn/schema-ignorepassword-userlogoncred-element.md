---
description: Specifica la modalità di gestione delle password durante l'aggiornamento dei profili.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Elemento IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307535"
---
# <a name="ignorepassword-userlogoncred-element"></a><span data-ttu-id="7c386-103">Elemento IgnorePassword (UserLogonCred)</span><span class="sxs-lookup"><span data-stu-id="7c386-103">IgnorePassword (UserLogonCred) Element</span></span>

<span data-ttu-id="7c386-104">L'elemento **IgnorePassword (UserLogonCred)** specifica come gestire le password quando si aggiornano i profili.</span><span class="sxs-lookup"><span data-stu-id="7c386-104">The **IgnorePassword (UserLogonCred)** element specifies how to handle passwords when upgrading profiles.</span></span>

<span data-ttu-id="7c386-105">Se è impostato su **true** e un profilo con lo stesso nome esiste al momento dell'operazione di aggiornamento, la password del profilo verrà acquisita e archiviata nel nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="7c386-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in new profile.</span></span>

<span data-ttu-id="7c386-106">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7c386-106">This element is optional.</span></span>

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

<span data-ttu-id="7c386-107">L'elemento **IgnorePassword** è definito dall'elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7c386-107">The **IgnorePassword** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c386-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c386-108">Requirements</span></span>



| <span data-ttu-id="7c386-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c386-109">Requirement</span></span> | <span data-ttu-id="7c386-110">Valore</span><span class="sxs-lookup"><span data-stu-id="7c386-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="7c386-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c386-111">Minimum supported client</span></span><br/> | <span data-ttu-id="7c386-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7c386-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7c386-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c386-113">Minimum supported server</span></span><br/> | <span data-ttu-id="7c386-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7c386-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="7c386-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c386-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c386-116">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="7c386-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7c386-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="7c386-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="7c386-118">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="7c386-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7c386-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="7c386-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




