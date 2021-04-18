---
title: Valori di sintassi semplici SNMP (SNMP. h)
description: I valori della sintassi semplice SNMP vengono utilizzati per indicare un tipo di variabile SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120234"
---
# <a name="snmp-simple-syntax-values"></a><span data-ttu-id="8bcae-103">Valori di sintassi semplici SNMP</span><span class="sxs-lookup"><span data-stu-id="8bcae-103">SNMP Simple Syntax Values</span></span>

<span data-ttu-id="8bcae-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8bcae-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8bcae-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="8bcae-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8bcae-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="8bcae-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="8bcae-107">I valori della sintassi semplice SNMP vengono utilizzati per indicare un tipo di variabile SNMP.</span><span class="sxs-lookup"><span data-stu-id="8bcae-107">The SNMP Simple Syntax Values are used to indicate an SNMP variable type.</span></span>



| <span data-ttu-id="8bcae-108">Costante</span><span class="sxs-lookup"><span data-stu-id="8bcae-108">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="8bcae-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bcae-109">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <span data-ttu-id="8bcae-110"><dt>**\_intero ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="8bcae-110"><dt>**ASN\_INTEGER**</dt></span></span> </dl>                            | <span data-ttu-id="8bcae-111">Indica una variabile di tipo integer con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8bcae-111">Indicates a 32-bit signed integer variable.</span></span><br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <span data-ttu-id="8bcae-112"><dt>**\_bit ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="8bcae-112"><dt>**ASN\_BITS**</dt></span></span> </dl>                                     | <span data-ttu-id="8bcae-113">Indica una variabile che è un'enumerazione di bit denominati.</span><span class="sxs-lookup"><span data-stu-id="8bcae-113">Indicates a variable that is an enumeration of named bits.</span></span><br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <span data-ttu-id="8bcae-114"><dt>**\_OCTETSTRING ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="8bcae-114"><dt>**ASN\_OCTETSTRING**</dt></span></span> </dl>                | <span data-ttu-id="8bcae-115">Indica una variabile di stringa ottetto.</span><span class="sxs-lookup"><span data-stu-id="8bcae-115">Indicates an octet string variable.</span></span><br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <span data-ttu-id="8bcae-116"><dt>**ASN \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="8bcae-116"><dt>**ASN\_NULL**</dt></span></span> </dl>                                     | <span data-ttu-id="8bcae-117">Indica un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="8bcae-117">Indicates a **NULL** value.</span></span><br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <span data-ttu-id="8bcae-118"><dt>**\_OBJECTIDENTIFIER ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="8bcae-118"><dt>**ASN\_OBJECTIDENTIFIER**</dt></span></span> </dl> | <span data-ttu-id="8bcae-119">Indica una variabile dell'identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="8bcae-119">Indicates an object identifier variable.</span></span><br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <span data-ttu-id="8bcae-120"><dt>**\_INTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="8bcae-120"><dt>**ASN\_INTEGER32**</dt></span></span> </dl>                      | <span data-ttu-id="8bcae-121">Indica un valore intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8bcae-121">Indicates a 32-bit signed integer value.</span></span><br/>                   |



## <a name="requirements"></a><span data-ttu-id="8bcae-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bcae-122">Requirements</span></span>



| <span data-ttu-id="8bcae-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bcae-123">Requirement</span></span> | <span data-ttu-id="8bcae-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8bcae-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8bcae-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bcae-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8bcae-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8bcae-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="8bcae-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bcae-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8bcae-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8bcae-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8bcae-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bcae-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bcae-130"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bcae-130"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bcae-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bcae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcae-132">Panoramica del protocollo Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="8bcae-132">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="8bcae-133">Riferimento SNMP</span><span class="sxs-lookup"><span data-stu-id="8bcae-133">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="8bcae-134">Costanti SNMP</span><span class="sxs-lookup"><span data-stu-id="8bcae-134">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

