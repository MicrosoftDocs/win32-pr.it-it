---
description: Archivia una matrice di byte che rappresenta la licenza DRM associata al flusso di byte.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Proprietà MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753127"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a><span data-ttu-id="58ba4-103">\_Proprietà di \_ rappresentazione della licenza MFNETSOURCE DRMNET \_</span><span class="sxs-lookup"><span data-stu-id="58ba4-103">MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION property</span></span>

<span data-ttu-id="58ba4-104">Archivia una matrice di byte che rappresenta la licenza DRM associata al flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="58ba4-104">Stores an array of bytes that represents the DRM license associated with the byte stream.</span></span>



<span data-ttu-id="58ba4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="58ba4-105">Data type</span></span>

<span data-ttu-id="58ba4-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="58ba4-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="58ba4-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="58ba4-107">PROPVARIANT member</span></span>

<span data-ttu-id="58ba4-108">Matrice di byte (**BLOB**)</span><span class="sxs-lookup"><span data-stu-id="58ba4-108">Byte array (**BLOB**)</span></span>

<span data-ttu-id="58ba4-109">\_BLOB VT</span><span class="sxs-lookup"><span data-stu-id="58ba4-109">VT\_BLOB</span></span>

<span data-ttu-id="58ba4-110">**blob**</span><span class="sxs-lookup"><span data-stu-id="58ba4-110">**blob**</span></span>



## <a name="remarks"></a><span data-ttu-id="58ba4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="58ba4-111">Remarks</span></span>

<span data-ttu-id="58ba4-112">La **rappresentazione di \_ \_ licenza \_ Constant MFNETSOURCE DRMNET** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="58ba4-112">The constant **MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION** defines the GUID for this property key.</span></span> <span data-ttu-id="58ba4-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="58ba4-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="58ba4-114">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="58ba4-114">This property is read-only.</span></span> <span data-ttu-id="58ba4-115">Per ottenere il valore della proprietà dal flusso di byte di rete, chiamare **IPropertyStore:: GetValue** e passare la struttura **PropertyKey** nel parametro *Key* .</span><span class="sxs-lookup"><span data-stu-id="58ba4-115">To get the property value from the network byte stream, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="58ba4-116">Il membro **fmtid** di **PropertyKey** deve essere impostato sul GUID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="58ba4-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ba4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ba4-117">Requirements</span></span>



| <span data-ttu-id="58ba4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ba4-118">Requirement</span></span> | <span data-ttu-id="58ba4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="58ba4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58ba4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ba4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58ba4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="58ba4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ba4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58ba4-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="58ba4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58ba4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="58ba4-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ba4-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ba4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58ba4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ba4-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58ba4-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="58ba4-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58ba4-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




