---
description: Elenco di URL a cui l'origine di rete invierà le informazioni di registrazione.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: Proprietà MFNETSOURCE_LOGURL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129782"
---
# <a name="mfnetsource_logurl-property"></a><span data-ttu-id="15ece-103">\_Proprietà LogURL di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="15ece-103">MFNETSOURCE\_LOGURL property</span></span>

<span data-ttu-id="15ece-104">Elenco di URL a cui l'origine di rete invierà le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="15ece-104">List of URLs to which the network source will send logging information.</span></span>



<span data-ttu-id="15ece-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="15ece-105">Data type</span></span>

<span data-ttu-id="15ece-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="15ece-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="15ece-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="15ece-107">PROPVARIANT member</span></span>

<span data-ttu-id="15ece-108">Matrice di stringhe di caratteri wide (**CALPWSTR**)</span><span class="sxs-lookup"><span data-stu-id="15ece-108">Array of wide-character strings (**CALPWSTR**)</span></span>

<span data-ttu-id="15ece-109">VT \_ vettore \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="15ece-109">VT\_VECTOR \| VT\_LPWSTR</span></span>

<span data-ttu-id="15ece-110">**CALPWSTR**</span><span class="sxs-lookup"><span data-stu-id="15ece-110">**calpwstr**</span></span>



## <a name="remarks"></a><span data-ttu-id="15ece-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="15ece-111">Remarks</span></span>

<span data-ttu-id="15ece-112">La costante **MFNETSOURCE \_ LogURL** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="15ece-112">The constant **MFNETSOURCE\_LOGURL** defines the GUID for this property key.</span></span> <span data-ttu-id="15ece-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="15ece-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="15ece-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="15ece-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="15ece-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="15ece-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="15ece-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="15ece-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15ece-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15ece-117">Requirements</span></span>



| <span data-ttu-id="15ece-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ece-118">Requirement</span></span> | <span data-ttu-id="15ece-119">Valore</span><span class="sxs-lookup"><span data-stu-id="15ece-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15ece-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15ece-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15ece-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15ece-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15ece-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15ece-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15ece-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15ece-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="15ece-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15ece-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ece-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15ece-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ece-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15ece-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ece-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15ece-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="15ece-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15ece-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




