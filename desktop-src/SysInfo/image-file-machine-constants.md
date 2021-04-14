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
# <a name="image-file-machine-constants"></a>Costanti computer del file di immagine

Descrive le possibili architetture di computer. Utilizzato in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) e [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**\_computer file di immagine \_ \_ sconosciuto**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Sconosciuto


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_host di \_ \_ destinazione computer del file \_ di immagine**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Interagisce con l'host e non con un Guest WOW64

> [!Note]  
> Questa costante è disponibile a partire da Windows 10, versione 1607 e Windows Server 2016.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**FILE di immagine \_ \_ i386 del computer \_**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**FILE di immagine \_ \_ R3000 del computer \_**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



MIPS little-endian, 0X160 big-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**FILE di immagine \_ \_ R4000 del computer \_**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



Little-endian MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**FILE di immagine \_ \_ R10000 del computer \_**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



Little-endian MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**FILE di immagine \_ \_ WCEMIPSV2 del computer \_**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



MIPS little-endian WCE V2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**immagine del computer del file di immagine \_ \_ \_ Alpha**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



\_AXP alfa


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**FILE di immagine \_ \_ SH3 del computer \_**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**FILE di immagine \_ \_ SH3DSP del computer \_**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**FILE di immagine \_ \_ SH3E del computer \_**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**FILE di immagine \_ \_ SH4 del computer \_**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**FILE di immagine \_ \_ SH5 del computer \_**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**FILE di immagine del \_ \_ computer \_ ARM**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



Little-Endian ARM


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_Thumb del \_ computer del file di immagine \_**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



Little-Endian ARM Thumb/Thumb-2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**FILE di immagine \_ \_ ARMNT del computer \_**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



Pollice Little-Endian ARM-2

> [!Note]  
> Questa costante è disponibile a partire da Windows 7 e Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**FILE di immagine \_ \_ AM33 del computer \_**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**computer con file di immagine \_ \_ \_ PowerPC**
</dt> <dd> <dl> <dt>

0x01F0
</dt> <dt>



Little-Endian PowerPC IBM


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**FILE di immagine \_ \_ POWERPCFP del computer \_**
</dt> <dd> <dl> <dt>

0x01f1
</dt> <dt>



POWERPCFP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Computer del file di immagine \_ \_ \_ ia64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**FILE di immagine \_ \_ MIPS16 del computer \_**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**FILE di immagine \_ \_ ALPHA64 del computer \_**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**FILE di immagine \_ \_ MIPSFPU del computer \_**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**FILE di immagine \_ \_ MIPSFPU16 del computer \_**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**FILE di immagine \_ \_ AXP64 del computer \_**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**\_Tricore computer del file di immagine \_ \_**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



Infineon


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**\_computer file di immagine \_ \_ CEF**
</dt> <dd> <dl> <dt>

0x0CEF
</dt> <dt>



CEF


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**FILE di immagine del \_ \_ computer \_ EBC**
</dt> <dd> <dl> <dt>

0x0EBC
</dt> <dt>



Codice byte EFI


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**FILE di immagine \_ \_ amd64 del computer \_**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



AMD64 (K8)


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**FILE di immagine \_ \_ M32R del computer \_**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**FILE di immagine \_ \_ arm64 del computer \_**
</dt> <dd> <dl> <dt>

0xAA64
</dt> <dt>



Little-Endian ARM64

> [!Note]  
> Questa costante è disponibile a partire da Windows 8.1 e Windows Server 2012 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**computer del file di immagine \_ \_ \_ CEE**
</dt> <dd> <dl> <dt>

0xC0EE
</dt> <dt>



CEE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




