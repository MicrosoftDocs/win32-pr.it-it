---
description: Definisce un tipo per l'elemento SimIccID del profilo Mobile Broadband.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo semplice simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307527"
---
# <a name="simiccidtype-simple-type"></a><span data-ttu-id="f4523-103">Tipo semplice simIccIDType</span><span class="sxs-lookup"><span data-stu-id="f4523-103">simIccIDType Simple Type</span></span>

<span data-ttu-id="f4523-104">Il tipo semplice **simIccIDType** definisce un tipo per l'elemento [**SimIccID**](schema-simiccid-mbnprofile-element.md) del profilo Mobile Broadband.</span><span class="sxs-lookup"><span data-stu-id="f4523-104">The **simIccIDType** simple type defines a type for the [**SimIccID**](schema-simiccid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="f4523-105">Questo tipo è una raccolta di cifre e/o lettere maiuscole e minuscole, con una lunghezza di almeno un carattere e un massimo di 20 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f4523-105">This type is a collection of digits and/or upper- and lower-case letters, at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="f4523-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="f4523-106">Patterns</span></span>

<span data-ttu-id="f4523-107">Il tipo semplice **simIccIDType** è un token che è limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="f4523-107">The **simIccIDType** simple type is a token that is restricted by the following pattern:</span></span>

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a><span data-ttu-id="f4523-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4523-108">Requirements</span></span>



| <span data-ttu-id="f4523-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4523-109">Requirement</span></span> | <span data-ttu-id="f4523-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f4523-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f4523-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4523-111">Minimum supported client</span></span><br/> | <span data-ttu-id="f4523-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f4523-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f4523-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4523-113">Minimum supported server</span></span><br/> | <span data-ttu-id="f4523-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f4523-114">None supported</span></span><br/>                         |



 

 




