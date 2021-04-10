---
title: Tipo complesso showMessageType
description: Definisce gli elementi che rappresentano un'azione che visualizza una finestra di messaggio.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- Utilità di pianificazione di tipo complesso showMessageType
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964512"
---
# <a name="showmessagetype-complex-type"></a><span data-ttu-id="fd2ba-104">Tipo complesso showMessageType</span><span class="sxs-lookup"><span data-stu-id="fd2ba-104">showMessageType Complex Type</span></span>

<span data-ttu-id="fd2ba-105">Definisce gli elementi che rappresentano un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="fd2ba-105">Defines the elements that represent an action that shows a message box.</span></span>

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fd2ba-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fd2ba-106">Child elements</span></span>



| <span data-ttu-id="fd2ba-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd2ba-107">Element</span></span>                                                            | <span data-ttu-id="fd2ba-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd2ba-108">Type</span></span>           | <span data-ttu-id="fd2ba-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd2ba-109">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="fd2ba-110">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="fd2ba-110">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="fd2ba-111">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="fd2ba-111">nonEmptyString</span></span> | <span data-ttu-id="fd2ba-112">Specifica il testo da visualizzare nel corpo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="fd2ba-112">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="fd2ba-113">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="fd2ba-113">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="fd2ba-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="fd2ba-114">nonEmptyString</span></span> | <span data-ttu-id="fd2ba-115">Specifica il titolo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="fd2ba-115">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="requirements"></a><span data-ttu-id="fd2ba-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd2ba-116">Requirements</span></span>



| <span data-ttu-id="fd2ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd2ba-117">Requirement</span></span> | <span data-ttu-id="fd2ba-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fd2ba-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd2ba-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd2ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd2ba-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd2ba-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd2ba-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd2ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd2ba-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd2ba-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





