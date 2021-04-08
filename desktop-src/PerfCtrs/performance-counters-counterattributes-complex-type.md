---
description: Definisce un elenco contenente fino a cinque attributi del contatore.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Tipo complesso counterAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967508"
---
# <a name="counterattributes-complex-type"></a><span data-ttu-id="5e736-103">Tipo complesso counterAttributes</span><span class="sxs-lookup"><span data-stu-id="5e736-103">counterAttributes Complex Type</span></span>

<span data-ttu-id="5e736-104">Definisce un elenco contenente fino a cinque attributi del contatore.</span><span class="sxs-lookup"><span data-stu-id="5e736-104">Defines a list that contains up to five counter attributes.</span></span>

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5e736-105">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5e736-105">Child elements</span></span>



| <span data-ttu-id="5e736-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e736-106">Element</span></span>              | <span data-ttu-id="5e736-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e736-107">Type</span></span>                                                                               | <span data-ttu-id="5e736-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e736-108">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e736-109">**counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="5e736-109">**counterAttribute**</span></span> | [<span data-ttu-id="5e736-110">**uomo: counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="5e736-110">**man:counterAttribute**</span></span>](performance-counters-counterattribute-complex-type.md) | <span data-ttu-id="5e736-111">Un attributo del contatore che specifica la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.</span><span class="sxs-lookup"><span data-stu-id="5e736-111">A counter attribute that specifies how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5e736-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e736-112">Requirements</span></span>



| <span data-ttu-id="5e736-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e736-113">Requirement</span></span> | <span data-ttu-id="5e736-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5e736-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e736-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e736-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5e736-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e736-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e736-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e736-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5e736-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e736-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




