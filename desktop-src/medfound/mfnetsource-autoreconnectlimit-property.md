---
description: Il numero di volte in cui l'origine di rete tenta di riconnettersi al server e riprendere lo streaming in caso di perdita della connessione.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: Proprietà MFNETSOURCE_AUTORECONNECTLIMIT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753135"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a><span data-ttu-id="9e79f-103">\_Proprietà AUTORECONNECTLIMIT di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="9e79f-103">MFNETSOURCE\_AUTORECONNECTLIMIT property</span></span>

<span data-ttu-id="9e79f-104">Il numero di volte in cui l'origine di rete tenta di riconnettersi al server e riprendere lo streaming in caso di perdita della connessione.</span><span class="sxs-lookup"><span data-stu-id="9e79f-104">The number of times the network source tries to reconnect to the server and resume streaming if the connection is lost.</span></span>



<span data-ttu-id="9e79f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9e79f-105">Data type</span></span>

<span data-ttu-id="9e79f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9e79f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9e79f-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9e79f-107">PROPVARIANT member</span></span>

<span data-ttu-id="9e79f-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="9e79f-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="9e79f-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9e79f-109">VT\_I4</span></span>

<span data-ttu-id="9e79f-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="9e79f-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9e79f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e79f-111">Remarks</span></span>

<span data-ttu-id="9e79f-112">La costante **MFNETSOURCE \_ AUTORECONNECTLIMIT** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e79f-112">The constant **MFNETSOURCE\_AUTORECONNECTLIMIT** defines the GUID for this property key.</span></span> <span data-ttu-id="9e79f-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="9e79f-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="9e79f-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="9e79f-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="9e79f-115">Per impostare la proprietà, passare un oggetto **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="9e79f-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="9e79f-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="9e79f-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e79f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e79f-117">Requirements</span></span>



| <span data-ttu-id="9e79f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e79f-118">Requirement</span></span> | <span data-ttu-id="9e79f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9e79f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e79f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e79f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e79f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e79f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9e79f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e79f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e79f-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e79f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9e79f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e79f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e79f-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e79f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e79f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e79f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e79f-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e79f-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9e79f-128">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="9e79f-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="9e79f-129">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e79f-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




