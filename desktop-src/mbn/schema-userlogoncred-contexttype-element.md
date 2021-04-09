---
description: Contiene le credenziali di accesso per una connessione.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Elemento UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129563"
---
# <a name="userlogoncred-contexttype-element"></a><span data-ttu-id="d275c-103">Elemento UserLogonCred (contextType)</span><span class="sxs-lookup"><span data-stu-id="d275c-103">UserLogonCred (contextType) Element</span></span>

<span data-ttu-id="d275c-104">L'elemento **UserLogonCred (ContextType)** contiene le credenziali di accesso per una connessione.</span><span class="sxs-lookup"><span data-stu-id="d275c-104">The **UserLogonCred (contextType)** element contains logon credentials for a connection.</span></span>

<span data-ttu-id="d275c-105">Questo elemento può avere gli elementi figlio seguenti.</span><span class="sxs-lookup"><span data-stu-id="d275c-105">This element can have the following child elements.</span></span>

-   [<span data-ttu-id="d275c-106">**Nome utente**</span><span class="sxs-lookup"><span data-stu-id="d275c-106">**UserName**</span></span>](schema-username-userlogoncred-element.md)
-   [<span data-ttu-id="d275c-107">**Password**</span><span class="sxs-lookup"><span data-stu-id="d275c-107">**Password**</span></span>](schema-password-userlogoncred-element.md)
-   [<span data-ttu-id="d275c-108">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="d275c-108">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md)

<span data-ttu-id="d275c-109">Questo elemento può avere un massimo di un'occorrenza.</span><span class="sxs-lookup"><span data-stu-id="d275c-109">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="d275c-110">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d275c-110">This element is optional.</span></span>

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d275c-111">L'elemento **UserLogonCred** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d275c-111">The **UserLogonCred** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d275c-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d275c-112">Child elements</span></span>



| <span data-ttu-id="d275c-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="d275c-113">Element</span></span>                                                               | <span data-ttu-id="d275c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d275c-114">Type</span></span>                                           | <span data-ttu-id="d275c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d275c-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="d275c-116">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="d275c-116">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="d275c-117">boolean</span><span class="sxs-lookup"><span data-stu-id="d275c-117">boolean</span></span>                                        | <span data-ttu-id="d275c-118">Come gestire le password durante l'aggiornamento dei profili.</span><span class="sxs-lookup"><span data-stu-id="d275c-118">How to handle passwords when upgrading profiles.</span></span><br/> |
| [<span data-ttu-id="d275c-119">**Password**</span><span class="sxs-lookup"><span data-stu-id="d275c-119">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="d275c-120">string</span><span class="sxs-lookup"><span data-stu-id="d275c-120">string</span></span>                                         | <span data-ttu-id="d275c-121">Password utente.</span><span class="sxs-lookup"><span data-stu-id="d275c-121">User password.</span></span><br/>                                   |
| [<span data-ttu-id="d275c-122">**Nome utente**</span><span class="sxs-lookup"><span data-stu-id="d275c-122">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="d275c-123">**nameType**</span><span class="sxs-lookup"><span data-stu-id="d275c-123">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="d275c-124">Nome utente.</span><span class="sxs-lookup"><span data-stu-id="d275c-124">User name.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="d275c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d275c-125">Requirements</span></span>



| <span data-ttu-id="d275c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d275c-126">Requirement</span></span> | <span data-ttu-id="d275c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d275c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d275c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d275c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d275c-129">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d275c-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d275c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d275c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d275c-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d275c-131">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d275c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d275c-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="d275c-133">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d275c-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d275c-134">**contextType**</span><span class="sxs-lookup"><span data-stu-id="d275c-134">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="d275c-135">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="d275c-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d275c-136">**Contesto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="d275c-136">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




