---
description: Identificatore univoco con cui il server identifica il client.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Proprietà MFNETSOURCE_CLIENTGUID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130118"
---
# <a name="mfnetsource_clientguid-property"></a><span data-ttu-id="8780c-103">\_Proprietà CLIENTGUID di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="8780c-103">MFNETSOURCE\_CLIENTGUID property</span></span>

<span data-ttu-id="8780c-104">Identificatore univoco con cui il server identifica il client.</span><span class="sxs-lookup"><span data-stu-id="8780c-104">Unique identifier by which the server identifies the client.</span></span>



<span data-ttu-id="8780c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8780c-105">Data type</span></span>

<span data-ttu-id="8780c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8780c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8780c-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8780c-107">PROPVARIANT member</span></span>

<span data-ttu-id="8780c-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8780c-108">**GUID**</span></span>

<span data-ttu-id="8780c-109">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="8780c-109">VT\_CLSID</span></span>

<span data-ttu-id="8780c-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="8780c-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="8780c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8780c-111">Remarks</span></span>

<span data-ttu-id="8780c-112">La costante **MFNETSOURCE \_ CLIENTGUID** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8780c-112">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="8780c-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="8780c-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="8780c-114">Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="8780c-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="8780c-115">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8780c-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="8780c-116">Se non è impostato o impostato come **GUID \_ NULL**, Microsoft Media Foundation genera un GUID anonimo per sessione che garantisce la privacy dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8780c-116">If not set or set as **GUID\_NULL**, Microsoft Media Foundation generates an anonymous GUID per session that ensures the user's privacy.</span></span>

## <a name="requirements"></a><span data-ttu-id="8780c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8780c-117">Requirements</span></span>



| <span data-ttu-id="8780c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8780c-118">Requirement</span></span> | <span data-ttu-id="8780c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8780c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8780c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8780c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8780c-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8780c-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8780c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8780c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8780c-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8780c-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8780c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8780c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8780c-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8780c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8780c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8780c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8780c-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8780c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8780c-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8780c-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




