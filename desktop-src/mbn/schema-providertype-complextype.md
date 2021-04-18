---
description: Specifica le informazioni su una rete cellulare.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Tipo complesso providerType (Mobile Broadband)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307530"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="35559-103">Tipo complesso providerType</span><span class="sxs-lookup"><span data-stu-id="35559-103">providerType Complex Type</span></span>

<span data-ttu-id="35559-104">Il tipo complesso **ProviderType** specifica le informazioni su una rete cellulare.</span><span class="sxs-lookup"><span data-stu-id="35559-104">The **providerType** complex type specifies information about a cellular network.</span></span>

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="35559-105">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="35559-105">Child elements</span></span>



| <span data-ttu-id="35559-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="35559-106">Element</span></span>                                                          | <span data-ttu-id="35559-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="35559-107">Type</span></span>                                                           | <span data-ttu-id="35559-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35559-108">Description</span></span>               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="35559-109">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="35559-109">**ProviderID**</span></span>](schema-providerid-providertype-element.md)     | [<span data-ttu-id="35559-110">**providerIdType**</span><span class="sxs-lookup"><span data-stu-id="35559-110">**providerIdType**</span></span>](schema-provideridtype-simpletype.md)     | <span data-ttu-id="35559-111">ID del provider.</span><span class="sxs-lookup"><span data-stu-id="35559-111">Provider ID.</span></span><br/>   |
| [<span data-ttu-id="35559-112">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="35559-112">**ProviderName**</span></span>](schema-providername-providertype-element.md) | [<span data-ttu-id="35559-113">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="35559-113">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="35559-114">Nome del provider.</span><span class="sxs-lookup"><span data-stu-id="35559-114">Provider name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="35559-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35559-115">Requirements</span></span>



| <span data-ttu-id="35559-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="35559-116">Requirement</span></span> | <span data-ttu-id="35559-117">Valore</span><span class="sxs-lookup"><span data-stu-id="35559-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="35559-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35559-118">Minimum supported client</span></span><br/> | <span data-ttu-id="35559-119">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="35559-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="35559-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35559-120">Minimum supported server</span></span><br/> | <span data-ttu-id="35559-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="35559-121">None supported</span></span><br/>                         |



 

 




