---
description: La \_ Proprietà pkey Audioengine \_ OEMFormat specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione di un flusso. I valori vengono popolati dall'OEM in un file con estensione inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127427"
---
# <a name="pkey_audioengine_oemformat"></a><span data-ttu-id="a8b0e-104">PKEY \_ Audioengine \_ OEMFormat</span><span class="sxs-lookup"><span data-stu-id="a8b0e-104">PKEY\_AudioEngine\_OEMFormat</span></span>

<span data-ttu-id="a8b0e-105">La \_ Proprietà pkey Audioengine \_ OEMFormat specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-105">The PKEY\_AudioEngine\_OEMFormat property specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="a8b0e-106">I valori vengono popolati dall'OEM in un file con estensione inf.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-106">The values are populated by the OEM in an .inf file.</span></span>

<span data-ttu-id="a8b0e-107">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ BLOB.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="a8b0e-108">Il membro **BLOB** della struttura **PROPVARIANT** è una struttura di tipo **BLOB** che contiene due membri.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-108">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="a8b0e-109">Member **BLOB. cbSize** è un **valore DWORD** che specifica il numero di byte nella descrizione del formato.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-109">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="a8b0e-110">Il membro **BLOB. pBlobData** punta a una struttura **WAVEFORMATEX** che contiene la descrizione del formato.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-110">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="a8b0e-111">Per ulteriori informazioni su BLOB, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-111">For more information about BLOB, see the Windows SDK documentation.</span></span> <span data-ttu-id="a8b0e-112">Per ulteriori informazioni su **WAVEFORMATEX**, vedere la documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-112">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b0e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8b0e-113">Requirements</span></span>



| <span data-ttu-id="a8b0e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b0e-114">Requirement</span></span> | <span data-ttu-id="a8b0e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a8b0e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b0e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b0e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b0e-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a8b0e-117">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a8b0e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b0e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b0e-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b0e-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8b0e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8b0e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b0e-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b0e-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b0e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8b0e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b0e-123">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="a8b0e-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="a8b0e-124">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="a8b0e-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




