---
description: Specifica la password utilizzata per autenticare un utente.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (UserLogonCred)-elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306778"
---
# <a name="password-userlogoncred-element"></a><span data-ttu-id="5f3db-103">Password (UserLogonCred)-elemento</span><span class="sxs-lookup"><span data-stu-id="5f3db-103">Password (UserLogonCred) Element</span></span>

<span data-ttu-id="5f3db-104">L'elemento [**password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) specifica la password usata per autenticare un utente.</span><span class="sxs-lookup"><span data-stu-id="5f3db-104">The [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) element specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="5f3db-105">L'elemento è una stringa composta da un massimo di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5f3db-105">The element is a string of up to 255 characters.</span></span>

<span data-ttu-id="5f3db-106">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f3db-106">This element is optional.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="5f3db-107">L'elemento **password** è definito dall'elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5f3db-107">The **Password** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f3db-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f3db-108">Requirements</span></span>



| <span data-ttu-id="5f3db-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f3db-109">Requirement</span></span> | <span data-ttu-id="5f3db-110">Valore</span><span class="sxs-lookup"><span data-stu-id="5f3db-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="5f3db-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f3db-111">Minimum supported client</span></span><br/> | <span data-ttu-id="5f3db-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5f3db-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5f3db-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f3db-113">Minimum supported server</span></span><br/> | <span data-ttu-id="5f3db-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f3db-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="5f3db-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f3db-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f3db-116">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="5f3db-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5f3db-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="5f3db-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="5f3db-118">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="5f3db-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5f3db-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="5f3db-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




