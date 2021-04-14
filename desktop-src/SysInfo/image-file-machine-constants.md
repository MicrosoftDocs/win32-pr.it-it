---
description: Descrive le possibili architetture di computer.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Costanti del computer del file di immagine (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526983"
---
# <a name="image-file-machine-constants"></a><span data-ttu-id="89140-103">Costanti computer del file di immagine</span><span class="sxs-lookup"><span data-stu-id="89140-103">Image File Machine Constants</span></span>

<span data-ttu-id="89140-104">Descrive le possibili architetture di computer.</span><span class="sxs-lookup"><span data-stu-id="89140-104">Describes possible machine architectures.</span></span> <span data-ttu-id="89140-105">Utilizzato in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) e [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span><span class="sxs-lookup"><span data-stu-id="89140-105">Used in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) and [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span></span>

<dl> <dt>

<span data-ttu-id="89140-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**\_computer file di immagine \_ \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="89140-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**IMAGE\_FILE\_MACHINE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-107">0</span><span class="sxs-lookup"><span data-stu-id="89140-107">0</span></span>
</dt> <dt>



<span data-ttu-id="89140-108">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="89140-108">Unknown</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_host di \_ \_ destinazione computer del file \_ di immagine**</span><span class="sxs-lookup"><span data-stu-id="89140-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE\_FILE\_MACHINE\_TARGET\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="89140-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="89140-111">Interagisce con l'host e non con un Guest WOW64</span><span class="sxs-lookup"><span data-stu-id="89140-111">Interacts with the host and not a WOW64 guest</span></span>

> [!Note]  
> <span data-ttu-id="89140-112">Questa costante è disponibile a partire da Windows 10, versione 1607 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="89140-112">This constant is available starting with Windows 10, version 1607 and Windows Server 2016.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**FILE di immagine \_ \_ i386 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**IMAGE\_FILE\_MACHINE\_I386**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-114">0x014c</span><span class="sxs-lookup"><span data-stu-id="89140-114">0x014c</span></span>
</dt> <dt>



<span data-ttu-id="89140-115">Intel 386</span><span class="sxs-lookup"><span data-stu-id="89140-115">Intel 386</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**FILE di immagine \_ \_ R3000 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**IMAGE\_FILE\_MACHINE\_R3000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-117">0x0162</span><span class="sxs-lookup"><span data-stu-id="89140-117">0x0162</span></span>
</dt> <dt>



<span data-ttu-id="89140-118">MIPS little-endian, 0X160 big-endian</span><span class="sxs-lookup"><span data-stu-id="89140-118">MIPS little-endian, 0x160 big-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**FILE di immagine \_ \_ R4000 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**IMAGE\_FILE\_MACHINE\_R4000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-120">0x0166</span><span class="sxs-lookup"><span data-stu-id="89140-120">0x0166</span></span>
</dt> <dt>



<span data-ttu-id="89140-121">Little-endian MIPS</span><span class="sxs-lookup"><span data-stu-id="89140-121">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**FILE di immagine \_ \_ R10000 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**IMAGE\_FILE\_MACHINE\_R10000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-123">0x0168</span><span class="sxs-lookup"><span data-stu-id="89140-123">0x0168</span></span>
</dt> <dt>



<span data-ttu-id="89140-124">Little-endian MIPS</span><span class="sxs-lookup"><span data-stu-id="89140-124">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**FILE di immagine \_ \_ WCEMIPSV2 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**IMAGE\_FILE\_MACHINE\_WCEMIPSV2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-126">0x0169</span><span class="sxs-lookup"><span data-stu-id="89140-126">0x0169</span></span>
</dt> <dt>



<span data-ttu-id="89140-127">MIPS little-endian WCE V2</span><span class="sxs-lookup"><span data-stu-id="89140-127">MIPS little-endian WCE v2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**immagine del computer del file di immagine \_ \_ \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="89140-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**IMAGE\_FILE\_MACHINE\_ALPHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-129">0x0184</span><span class="sxs-lookup"><span data-stu-id="89140-129">0x0184</span></span>
</dt> <dt>



<span data-ttu-id="89140-130">\_AXP alfa</span><span class="sxs-lookup"><span data-stu-id="89140-130">Alpha\_AXP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**FILE di immagine \_ \_ SH3 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**IMAGE\_FILE\_MACHINE\_SH3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-132">0x01a2</span><span class="sxs-lookup"><span data-stu-id="89140-132">0x01a2</span></span>
</dt> <dt>



<span data-ttu-id="89140-133">SH3 little-endian</span><span class="sxs-lookup"><span data-stu-id="89140-133">SH3 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**FILE di immagine \_ \_ SH3DSP del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**IMAGE\_FILE\_MACHINE\_SH3DSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-135">0x01a3</span><span class="sxs-lookup"><span data-stu-id="89140-135">0x01a3</span></span>
</dt> <dt>



<span data-ttu-id="89140-136">SH3DSP</span><span class="sxs-lookup"><span data-stu-id="89140-136">SH3DSP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**FILE di immagine \_ \_ SH3E del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**IMAGE\_FILE\_MACHINE\_SH3E**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-138">0x01a4</span><span class="sxs-lookup"><span data-stu-id="89140-138">0x01a4</span></span>
</dt> <dt>



<span data-ttu-id="89140-139">SH3E little-endian</span><span class="sxs-lookup"><span data-stu-id="89140-139">SH3E little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**FILE di immagine \_ \_ SH4 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**IMAGE\_FILE\_MACHINE\_SH4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-141">0x01a6</span><span class="sxs-lookup"><span data-stu-id="89140-141">0x01a6</span></span>
</dt> <dt>



<span data-ttu-id="89140-142">SH4 little-endian</span><span class="sxs-lookup"><span data-stu-id="89140-142">SH4 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**FILE di immagine \_ \_ SH5 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**IMAGE\_FILE\_MACHINE\_SH5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-144">0x01a8</span><span class="sxs-lookup"><span data-stu-id="89140-144">0x01a8</span></span>
</dt> <dt>



<span data-ttu-id="89140-145">SH5</span><span class="sxs-lookup"><span data-stu-id="89140-145">SH5</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**FILE di immagine del \_ \_ computer \_ ARM**</span><span class="sxs-lookup"><span data-stu-id="89140-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**IMAGE\_FILE\_MACHINE\_ARM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-147">0x01c0</span><span class="sxs-lookup"><span data-stu-id="89140-147">0x01c0</span></span>
</dt> <dt>



<span data-ttu-id="89140-148">Little-Endian ARM</span><span class="sxs-lookup"><span data-stu-id="89140-148">ARM Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_Thumb del \_ computer del file di immagine \_**</span><span class="sxs-lookup"><span data-stu-id="89140-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**IMAGE\_FILE\_MACHINE\_THUMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-150">0x01c2</span><span class="sxs-lookup"><span data-stu-id="89140-150">0x01c2</span></span>
</dt> <dt>



<span data-ttu-id="89140-151">Little-Endian ARM Thumb/Thumb-2</span><span class="sxs-lookup"><span data-stu-id="89140-151">ARM Thumb/Thumb-2 Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**FILE di immagine \_ \_ ARMNT del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**IMAGE\_FILE\_MACHINE\_ARMNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-153">0x01c4</span><span class="sxs-lookup"><span data-stu-id="89140-153">0x01c4</span></span>
</dt> <dt>



<span data-ttu-id="89140-154">Pollice Little-Endian ARM-2</span><span class="sxs-lookup"><span data-stu-id="89140-154">ARM Thumb-2 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="89140-155">Questa costante è disponibile a partire da Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="89140-155">This constant is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**FILE di immagine \_ \_ AM33 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**IMAGE\_FILE\_MACHINE\_AM33**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-157">0x01d3</span><span class="sxs-lookup"><span data-stu-id="89140-157">0x01d3</span></span>
</dt> <dt>



<span data-ttu-id="89140-158">TAM33BD</span><span class="sxs-lookup"><span data-stu-id="89140-158">TAM33BD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**computer con file di immagine \_ \_ \_ PowerPC**</span><span class="sxs-lookup"><span data-stu-id="89140-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**IMAGE\_FILE\_MACHINE\_POWERPC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-160">0x01F0</span><span class="sxs-lookup"><span data-stu-id="89140-160">0x01F0</span></span>
</dt> <dt>



<span data-ttu-id="89140-161">Little-Endian PowerPC IBM</span><span class="sxs-lookup"><span data-stu-id="89140-161">IBM PowerPC Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**FILE di immagine \_ \_ POWERPCFP del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**IMAGE\_FILE\_MACHINE\_POWERPCFP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-163">0x01f1</span><span class="sxs-lookup"><span data-stu-id="89140-163">0x01f1</span></span>
</dt> <dt>



<span data-ttu-id="89140-164">POWERPCFP</span><span class="sxs-lookup"><span data-stu-id="89140-164">POWERPCFP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Computer del file di immagine \_ \_ \_ ia64**</span><span class="sxs-lookup"><span data-stu-id="89140-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**IMAGE\_FILE\_MACHINE\_IA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-166">0x0200</span><span class="sxs-lookup"><span data-stu-id="89140-166">0x0200</span></span>
</dt> <dt>



<span data-ttu-id="89140-167">Intel 64</span><span class="sxs-lookup"><span data-stu-id="89140-167">Intel 64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**FILE di immagine \_ \_ MIPS16 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**IMAGE\_FILE\_MACHINE\_MIPS16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-169">0x0266</span><span class="sxs-lookup"><span data-stu-id="89140-169">0x0266</span></span>
</dt> <dt>



<span data-ttu-id="89140-170">MIPS</span><span class="sxs-lookup"><span data-stu-id="89140-170">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**FILE di immagine \_ \_ ALPHA64 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**IMAGE\_FILE\_MACHINE\_ALPHA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-172">0x0284</span><span class="sxs-lookup"><span data-stu-id="89140-172">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="89140-173">ALPHA64</span><span class="sxs-lookup"><span data-stu-id="89140-173">ALPHA64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**FILE di immagine \_ \_ MIPSFPU del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-175">0x0366</span><span class="sxs-lookup"><span data-stu-id="89140-175">0x0366</span></span>
</dt> <dt>



<span data-ttu-id="89140-176">MIPS</span><span class="sxs-lookup"><span data-stu-id="89140-176">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**FILE di immagine \_ \_ MIPSFPU16 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-178">0x0466</span><span class="sxs-lookup"><span data-stu-id="89140-178">0x0466</span></span>
</dt> <dt>



<span data-ttu-id="89140-179">MIPS</span><span class="sxs-lookup"><span data-stu-id="89140-179">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**FILE di immagine \_ \_ AXP64 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**IMAGE\_FILE\_MACHINE\_AXP64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-181">0x0284</span><span class="sxs-lookup"><span data-stu-id="89140-181">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="89140-182">AXP64</span><span class="sxs-lookup"><span data-stu-id="89140-182">AXP64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**\_Tricore computer del file di immagine \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89140-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**IMAGE\_FILE\_MACHINE\_TRICORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-184">0x0520</span><span class="sxs-lookup"><span data-stu-id="89140-184">0x0520</span></span>
</dt> <dt>



<span data-ttu-id="89140-185">Infineon</span><span class="sxs-lookup"><span data-stu-id="89140-185">Infineon</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**\_computer file di immagine \_ \_ CEF**</span><span class="sxs-lookup"><span data-stu-id="89140-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**IMAGE\_FILE\_MACHINE\_CEF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-187">0x0CEF</span><span class="sxs-lookup"><span data-stu-id="89140-187">0x0CEF</span></span>
</dt> <dt>



<span data-ttu-id="89140-188">CEF</span><span class="sxs-lookup"><span data-stu-id="89140-188">CEF</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**FILE di immagine del \_ \_ computer \_ EBC**</span><span class="sxs-lookup"><span data-stu-id="89140-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**IMAGE\_FILE\_MACHINE\_EBC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-190">0x0EBC</span><span class="sxs-lookup"><span data-stu-id="89140-190">0x0EBC</span></span>
</dt> <dt>



<span data-ttu-id="89140-191">Codice byte EFI</span><span class="sxs-lookup"><span data-stu-id="89140-191">EFI Byte Code</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**FILE di immagine \_ \_ amd64 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**IMAGE\_FILE\_MACHINE\_AMD64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-193">0x8664</span><span class="sxs-lookup"><span data-stu-id="89140-193">0x8664</span></span>
</dt> <dt>



<span data-ttu-id="89140-194">AMD64 (K8)</span><span class="sxs-lookup"><span data-stu-id="89140-194">AMD64 (K8)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**FILE di immagine \_ \_ M32R del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**IMAGE\_FILE\_MACHINE\_M32R**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-196">0x9041</span><span class="sxs-lookup"><span data-stu-id="89140-196">0x9041</span></span>
</dt> <dt>



<span data-ttu-id="89140-197">M32R little-endian</span><span class="sxs-lookup"><span data-stu-id="89140-197">M32R little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**FILE di immagine \_ \_ arm64 del computer \_**</span><span class="sxs-lookup"><span data-stu-id="89140-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**IMAGE\_FILE\_MACHINE\_ARM64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-199">0xAA64</span><span class="sxs-lookup"><span data-stu-id="89140-199">0xAA64</span></span>
</dt> <dt>



<span data-ttu-id="89140-200">Little-Endian ARM64</span><span class="sxs-lookup"><span data-stu-id="89140-200">ARM64 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="89140-201">Questa costante è disponibile a partire da Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="89140-201">This constant is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="89140-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**computer del file di immagine \_ \_ \_ CEE**</span><span class="sxs-lookup"><span data-stu-id="89140-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**IMAGE\_FILE\_MACHINE\_CEE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89140-203">0xC0EE</span><span class="sxs-lookup"><span data-stu-id="89140-203">0xC0EE</span></span>
</dt> <dt>



<span data-ttu-id="89140-204">CEE</span><span class="sxs-lookup"><span data-stu-id="89140-204">CEE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89140-205">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89140-205">Requirements</span></span>



| <span data-ttu-id="89140-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="89140-206">Requirement</span></span> | <span data-ttu-id="89140-207">Valore</span><span class="sxs-lookup"><span data-stu-id="89140-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89140-208">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89140-208">Minimum supported client</span></span><br/> | <span data-ttu-id="89140-209">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="89140-209">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89140-210">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89140-210">Minimum supported server</span></span><br/> | <span data-ttu-id="89140-211">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89140-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89140-212">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89140-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="89140-213"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="89140-213"><dt>Winnt.h</dt></span></span> </dl> |



 

 




