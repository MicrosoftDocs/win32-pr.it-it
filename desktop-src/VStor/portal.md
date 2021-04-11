---
description: Incapsulare il disco rigido in un singolo file per l'uso da parte del sistema operativo come disco virtuale. I dischi virtuali possono fungere da dischi di avvio e possono ospitare file System nativi (NTFS, FAT, exFAT e UDF), supportando al tempo stesso le operazioni standard su disco e file.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226106"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span data-ttu-id="7c16d-104"><span id="vhd.portal"></span>Disco virtuale</span><span class="sxs-lookup"><span data-stu-id="7c16d-104"><span id="vhd.portal"></span>Virtual Disk</span></span>

## <a name="span-idpurposespanpurpose"></a><span data-ttu-id="7c16d-105"><span id="purpose"></span>Scopo</span><span class="sxs-lookup"><span data-stu-id="7c16d-105"><span id="purpose"></span>Purpose</span></span>

<span data-ttu-id="7c16d-106">Il formato del disco rigido virtuale (VHD) è una specifica del formato di immagine disponibile pubblicamente che specifica un disco rigido virtuale incapsulato in un singolo file, in grado di ospitare file System nativi, supportando al contempo operazioni standard su disco e file.</span><span class="sxs-lookup"><span data-stu-id="7c16d-106">The Virtual Hard Disk (VHD) format is a publicly-available image format specification that specifies a virtual hard disk encapsulated in a single file, capable of hosting native file systems while supporting standard disk and file operations.</span></span> <span data-ttu-id="7c16d-107">Un esempio di come vengono usati i file VHD è la funzionalità [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in windows Server 2008, Virtual Server e Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7c16d-107">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="7c16d-108">Questi prodotti usano dischi rigidi virtuali per contenere l'immagine del sistema operativo Windows usata da una macchina virtuale come disco di avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c16d-108">These products use VHDs to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span data-ttu-id="7c16d-109"><span id="developer_audience_heading"></span>Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="7c16d-109"><span id="developer_audience_heading"></span>Developer audience</span></span>

<span data-ttu-id="7c16d-110">Il Software Development Kit (SDK) di Microsoft Windows integra il supporto VHD nativo per l'utilizzo di VHD, semplificando la creazione, la gestione e la distribuzione di immagini Windows nei VHD tramite gli strumenti di supporto o di gestione delle API della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="7c16d-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with VHDs, making it easier for developers and administrators to create, manage, and deploy Windows images in VHDs using the platform API support or management tools.</span></span> <span data-ttu-id="7c16d-111">Non è necessario installare applicazioni separate o implementare un parser di formato VHD per abilitare queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="7c16d-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="7c16d-112">Queste API consentono l'uso generico di dischi rigidi virtuali indipendentemente da qualsiasi altra tecnologia di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7c16d-112">These APIs allow for generic use of VHDs independent of any other virtualization technologies.</span></span>

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span data-ttu-id="7c16d-113"><span id="run_time_requirements_heading"></span>Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="7c16d-113"><span id="run_time_requirements_heading"></span>Run-time requirements</span></span>

<span data-ttu-id="7c16d-114">VHD è supportato in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="7c16d-114">VHD is supported on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="7c16d-115"><span id="in_this_section"></span>In questa sezione</span><span class="sxs-lookup"><span data-stu-id="7c16d-115"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c16d-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="7c16d-116">Topic</span></span></th>
<th><span data-ttu-id="7c16d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c16d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c16d-118"><a href="about-vhd.md">Informazioni su VHD</a></span><span class="sxs-lookup"><span data-stu-id="7c16d-118"><a href="about-vhd.md">About VHD</a></span></span></p></td>
<td><p><span data-ttu-id="7c16d-119">Descrive il formato VHD con suggerimenti e suggerimenti sull'utilizzo dell'API.</span><span class="sxs-lookup"><span data-stu-id="7c16d-119">Describes the VHD format with API usage tips and suggestions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c16d-120"><a href="vhd-reference.md">Riferimento al disco rigido virtuale</a></span><span class="sxs-lookup"><span data-stu-id="7c16d-120"><a href="vhd-reference.md">VHD Reference</a></span></span></p></td>
<td><p><span data-ttu-id="7c16d-121">Descrive le funzioni, le strutture e le enumerazioni dell'API VHD.</span><span class="sxs-lookup"><span data-stu-id="7c16d-121">Describes the VHD API functions, structures, and enumerations.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="7c16d-122"><span id="related_topics"></span>Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c16d-122"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="7c16d-123">Servizio dischi virtuali</span><span class="sxs-lookup"><span data-stu-id="7c16d-123">Virtual Disk Service</span></span>](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
