---
description: Il programma di installazione imposta la proprietà VersionNT64 sul numero di versione del sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64 - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262073"
---
# <a name="versionnt64-property"></a><span data-ttu-id="774a1-103">VersionNT64 - proprietà</span><span class="sxs-lookup"><span data-stu-id="774a1-103">VersionNT64 property</span></span>

<span data-ttu-id="774a1-104">Il programma di installazione **imposta la proprietà VersionNT64** sul numero di versione del sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="774a1-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="774a1-105">La proprietà non è definita se il sistema operativo non è a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="774a1-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="774a1-106">Il valore è un numero intero: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="774a1-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="774a1-107">Per motivi di compatibilità, la [](template-summary.md) proprietà non è definita anche se la proprietà Riepilogo modello indica che il pacchetto è per sistemi Intel (x86) a 32 bit e il sistema operativo non può eseguire codice Intel (x64) a 64 bit, ad esempio Windows 10 on ARM (ARM64).</span><span class="sxs-lookup"><span data-stu-id="774a1-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel (x86) systems and the operating system cannot run 64-bit Intel (x64) code, such as Windows 10 on ARM (ARM64).</span></span>

> [!NOTE]
> <span data-ttu-id="774a1-108">A Windows 10 build 21277, le build ARM64 nel canale Dev del programma Windows Insider Preview supportano le applicazioni x64.</span><span class="sxs-lookup"><span data-stu-id="774a1-108">As of Windows 10 Build 21277, ARM64 builds in the Dev channel of the Windows Insider Preview program have support for x64 applications.</span></span> <span data-ttu-id="774a1-109">In queste build ARM64 la proprietà VersionNT64 è definita per i pacchetti x86.</span><span class="sxs-lookup"><span data-stu-id="774a1-109">On these ARM64 builds, the VersionNT64 property is defined for x86 packages.</span></span>

## <a name="remarks"></a><span data-ttu-id="774a1-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="774a1-110">Remarks</span></span>

<span data-ttu-id="774a1-111">Le espressioni condizionali eseguono il test per Windows a 64 bit semplicemente usando il nome della proprietà o verificando la versione usando un operatore di confronto.</span><span class="sxs-lookup"><span data-stu-id="774a1-111">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="774a1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="774a1-112">Requirements</span></span>



| <span data-ttu-id="774a1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="774a1-113">Requirement</span></span> | <span data-ttu-id="774a1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="774a1-114">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="774a1-115">Versione</span><span class="sxs-lookup"><span data-stu-id="774a1-115">Version</span></span><br/> | <span data-ttu-id="774a1-116">Windows Installer 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="774a1-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="774a1-117">Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="774a1-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="774a1-118">Windows Installer in Windows Server 2003 o Windows XP Vedere i requisiti [di Windows Installer Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una Windows Installer versione.</span><span class="sxs-lookup"><span data-stu-id="774a1-118">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="774a1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="774a1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774a1-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="774a1-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




