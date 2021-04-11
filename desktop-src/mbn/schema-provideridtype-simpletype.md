---
description: Definisce un tipo per l'elemento ProviderID del profilo Mobile Broadband.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Tipo semplice providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129007"
---
# <a name="provideridtype-simple-type"></a><span data-ttu-id="de2c7-103">Tipo semplice providerIdType</span><span class="sxs-lookup"><span data-stu-id="de2c7-103">providerIdType Simple Type</span></span>

<span data-ttu-id="de2c7-104">Il tipo semplice **providerIdType** definisce un tipo per l'elemento [**ProviderID**](schema-providerid-providertype-element.md) del profilo Mobile Broadband.</span><span class="sxs-lookup"><span data-stu-id="de2c7-104">The **providerIdType** simple type defines a type for the [**ProviderID**](schema-providerid-providertype-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="de2c7-105">Questo tipo è una raccolta di cifre con una lunghezza di almeno una cifra e un massimo di 6 cifre.</span><span class="sxs-lookup"><span data-stu-id="de2c7-105">This type is a collection of digits at least one digit long and at most 6 digits long.</span></span>

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="de2c7-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="de2c7-106">Patterns</span></span>

<span data-ttu-id="de2c7-107">Il tipo semplice **providerIdType** è un token che è limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="de2c7-107">The **providerIdType** simple type is a token that is restricted by the following pattern:</span></span>

-   `\d{1,6}`

## <a name="requirements"></a><span data-ttu-id="de2c7-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de2c7-108">Requirements</span></span>



| <span data-ttu-id="de2c7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="de2c7-109">Requirement</span></span> | <span data-ttu-id="de2c7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="de2c7-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="de2c7-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de2c7-111">Minimum supported client</span></span><br/> | <span data-ttu-id="de2c7-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="de2c7-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="de2c7-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de2c7-113">Minimum supported server</span></span><br/> | <span data-ttu-id="de2c7-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="de2c7-114">None supported</span></span><br/>                         |



 

 




