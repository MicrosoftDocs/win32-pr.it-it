---
title: Tipo complesso sendEmailType
description: Definisce il tipo di azione utilizzato per specificare che un messaggio di posta elettronica verrà inviato quando viene eseguita un'attività. Questo tipo definisce tutti gli elementi utilizzati per modellare il messaggio di posta elettronica.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- Utilità di pianificazione di tipo complesso sendEmailType
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302681"
---
# <a name="sendemailtype-complex-type"></a><span data-ttu-id="aaa44-105">Tipo complesso sendEmailType</span><span class="sxs-lookup"><span data-stu-id="aaa44-105">sendEmailType Complex Type</span></span>

<span data-ttu-id="aaa44-106">Definisce il tipo di azione utilizzato per specificare che un messaggio di posta elettronica verrà inviato quando viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="aaa44-106">Defines the action type used to specify that an email will be sent when a task executes.</span></span> <span data-ttu-id="aaa44-107">Questo tipo definisce tutti gli elementi utilizzati per modellare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-107">This type defines all the elements used to model the email message.</span></span>

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="aaa44-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="aaa44-108">Child elements</span></span>



| <span data-ttu-id="aaa44-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="aaa44-109">Element</span></span>                                                                        | <span data-ttu-id="aaa44-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="aaa44-110">Type</span></span>                                                                         | <span data-ttu-id="aaa44-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaa44-111">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aaa44-112">**Allegati**</span><span class="sxs-lookup"><span data-stu-id="aaa44-112">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="aaa44-113">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="aaa44-113">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="aaa44-114">Specifica un elenco di allegati nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-114">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="aaa44-115">**Bcc**</span><span class="sxs-lookup"><span data-stu-id="aaa44-115">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="aaa44-116">**string**</span><span class="sxs-lookup"><span data-stu-id="aaa44-116">**string**</span></span>                                                                   | <span data-ttu-id="aaa44-117">Specifica gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-117">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="aaa44-118">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="aaa44-118">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="aaa44-119">**string**</span><span class="sxs-lookup"><span data-stu-id="aaa44-119">**string**</span></span>                                                                   | <span data-ttu-id="aaa44-120">Specifica il testo nel corpo del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-120">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="aaa44-121">**CC**</span><span class="sxs-lookup"><span data-stu-id="aaa44-121">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="aaa44-122">**string**</span><span class="sxs-lookup"><span data-stu-id="aaa44-122">**string**</span></span>                                                                   | <span data-ttu-id="aaa44-123">Specifica gli indirizzi di posta elettronica usati nella riga CC di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-123">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="aaa44-124">**Da**</span><span class="sxs-lookup"><span data-stu-id="aaa44-124">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="aaa44-125">**string**</span><span class="sxs-lookup"><span data-stu-id="aaa44-125">**string**</span></span>                                                                   | <span data-ttu-id="aaa44-126">Specifica l'indirizzo di posta elettronica del mittente.</span><span class="sxs-lookup"><span data-stu-id="aaa44-126">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="aaa44-127">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="aaa44-127">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="aaa44-128">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="aaa44-128">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="aaa44-129">Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-129">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="aaa44-130">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="aaa44-130">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="aaa44-131">**string**</span><span class="sxs-lookup"><span data-stu-id="aaa44-131">**string**</span></span>                                                                   | <span data-ttu-id="aaa44-132">Specifica gli indirizzi di posta elettronica a cui risponde nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-132">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="aaa44-133">**Server**</span><span class="sxs-lookup"><span data-stu-id="aaa44-133">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="aaa44-134">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="aaa44-134">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="aaa44-135">Specifica il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-135">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="aaa44-136">**Oggetto**</span><span class="sxs-lookup"><span data-stu-id="aaa44-136">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="aaa44-137">**string**</span><span class="sxs-lookup"><span data-stu-id="aaa44-137">**string**</span></span>                                                                   | <span data-ttu-id="aaa44-138">Specifica l'oggetto del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-138">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="aaa44-139">**A**</span><span class="sxs-lookup"><span data-stu-id="aaa44-139">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="aaa44-140">**string**</span><span class="sxs-lookup"><span data-stu-id="aaa44-140">**string**</span></span>                                                                   | <span data-ttu-id="aaa44-141">Specifica gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aaa44-141">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="aaa44-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaa44-142">Requirements</span></span>



| <span data-ttu-id="aaa44-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaa44-143">Requirement</span></span> | <span data-ttu-id="aaa44-144">Valore</span><span class="sxs-lookup"><span data-stu-id="aaa44-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aaa44-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaa44-145">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa44-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aaa44-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aaa44-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaa44-147">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa44-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aaa44-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





