---
title: Tipo complesso attachmentsType
description: Definisce gli elementi utilizzati per specificare un allegato inviato con un messaggio di posta elettronica.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- Utilità di pianificazione di tipo complesso attachmentsType
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302172"
---
# <a name="attachmentstype-complex-type"></a><span data-ttu-id="420ea-104">Tipo complesso attachmentsType</span><span class="sxs-lookup"><span data-stu-id="420ea-104">attachmentsType Complex Type</span></span>

<span data-ttu-id="420ea-105">Definisce gli elementi utilizzati per specificare un allegato inviato con un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="420ea-105">Defines the elements used to specify an attachment sent with an email message.</span></span>

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="420ea-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="420ea-106">Child elements</span></span>



| <span data-ttu-id="420ea-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="420ea-107">Element</span></span>                                                          | <span data-ttu-id="420ea-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="420ea-108">Type</span></span>                                                                    | <span data-ttu-id="420ea-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="420ea-109">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="420ea-110">**File**</span><span class="sxs-lookup"><span data-stu-id="420ea-110">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="420ea-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="420ea-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="420ea-112">Specifica il percorso di un file inviato come allegato in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="420ea-112">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="420ea-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="420ea-113">Requirements</span></span>



| <span data-ttu-id="420ea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="420ea-114">Requirement</span></span> | <span data-ttu-id="420ea-115">Valore</span><span class="sxs-lookup"><span data-stu-id="420ea-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="420ea-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="420ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="420ea-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="420ea-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="420ea-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="420ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="420ea-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="420ea-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





