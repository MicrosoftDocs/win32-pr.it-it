---
title: Valori di sintassi del costruttore SNMP (SNMP. h)
description: I valori di sintassi del costruttore SNMP descrivono i tipi conformi allo standard di codifica ASN. 1 (Abstract Syntax Notation One).
ms.assetid: 8e3b6e00-51cf-4e39-a68e-dcf8fbe8ab3b
topic_type:
- apiref
api_name:
- ASN_SEQUENCE
- ASN_SEQUENCEOF
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484e58d7a92a3c75408db3160362d84e7891b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119527"
---
# <a name="snmp-constructor-syntax-values"></a><span data-ttu-id="2c6ca-103">Valori di sintassi del costruttore SNMP</span><span class="sxs-lookup"><span data-stu-id="2c6ca-103">SNMP Constructor Syntax Values</span></span>

<span data-ttu-id="2c6ca-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2c6ca-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2c6ca-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="2c6ca-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2c6ca-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="2c6ca-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="2c6ca-107">I valori di sintassi del costruttore SNMP descrivono i tipi conformi allo standard di codifica ASN. 1 (Abstract Syntax Notation One).</span><span class="sxs-lookup"><span data-stu-id="2c6ca-107">The SNMP Constructor Syntax Values describe types that are compliant with the Abstract Syntax Notation One (ASN.1) encoding standard.</span></span>



| <span data-ttu-id="2c6ca-108">Costante</span><span class="sxs-lookup"><span data-stu-id="2c6ca-108">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="2c6ca-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c6ca-109">Description</span></span>                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="ASN_SEQUENCE"></span><span id="asn_sequence"></span><dl> <span data-ttu-id="2c6ca-110"><dt>**\_sequenza ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2c6ca-110"><dt>**ASN\_SEQUENCE**</dt></span></span> </dl>       | <span data-ttu-id="2c6ca-111">Indica che il messaggio è una sequenza ASN.</span><span class="sxs-lookup"><span data-stu-id="2c6ca-111">Indicates that the message is an ASN sequence.</span></span><br/> |
| <span id="ASN_SEQUENCEOF"></span><span id="asn_sequenceof"></span><dl> <span data-ttu-id="2c6ca-112"><dt>**\_SEQUENCEOF ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2c6ca-112"><dt>**ASN\_SEQUENCEOF**</dt></span></span> </dl> | <span data-ttu-id="2c6ca-113">Vedere \_ sequenza ASN.</span><span class="sxs-lookup"><span data-stu-id="2c6ca-113">See ASN\_SEQUENCE.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="2c6ca-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c6ca-114">Requirements</span></span>



| <span data-ttu-id="2c6ca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c6ca-115">Requirement</span></span> | <span data-ttu-id="2c6ca-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2c6ca-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2c6ca-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c6ca-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6ca-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2c6ca-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="2c6ca-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c6ca-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6ca-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2c6ca-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c6ca-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c6ca-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c6ca-122"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c6ca-122"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c6ca-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c6ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c6ca-124">Panoramica del protocollo Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="2c6ca-124">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="2c6ca-125">Riferimento SNMP</span><span class="sxs-lookup"><span data-stu-id="2c6ca-125">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="2c6ca-126">Costanti SNMP</span><span class="sxs-lookup"><span data-stu-id="2c6ca-126">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

