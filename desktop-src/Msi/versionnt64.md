---
description: Il programma di installazione imposta la proprietà VersionNT64 sul numero di versione per il sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Proprietà VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326898"
---
# <a name="versionnt64-property"></a><span data-ttu-id="b6ab9-103">Proprietà VersionNT64</span><span class="sxs-lookup"><span data-stu-id="b6ab9-103">VersionNT64 property</span></span>

<span data-ttu-id="b6ab9-104">Il programma di installazione imposta la proprietà **VersionNT64** sul numero di versione per il sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="b6ab9-105">La proprietà non è definita se il sistema operativo non è a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="b6ab9-106">Il valore è un numero intero: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="b6ab9-107">Per motivi di compatibilità, anche la proprietà non è definita se la proprietà di [**Riepilogo del modello**](template-summary.md) indica che il pacchetto è per i sistemi Intel a 32 bit e il sistema operativo è un'architettura a 64 bit che non è Intel64 o x64, ad esempio arm64.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel systems and the operating system is a 64-bit architecture that is not Intel64 or x64 (such as ARM64).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6ab9-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6ab9-108">Remarks</span></span>

<span data-ttu-id="b6ab9-109">Le espressioni condizionali testano le finestre a 64 bit semplicemente utilizzando il nome della proprietà o verificando la versione utilizzando un operatore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-109">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ab9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6ab9-110">Requirements</span></span>



| <span data-ttu-id="b6ab9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ab9-111">Requirement</span></span> | <span data-ttu-id="b6ab9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b6ab9-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ab9-113">Versione</span><span class="sxs-lookup"><span data-stu-id="b6ab9-113">Version</span></span><br/> | <span data-ttu-id="b6ab9-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b6ab9-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b6ab9-116">Windows Installer in Windows Server 2003 o Windows XP, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack di Windows minimo richiesto da una versione di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b6ab9-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6ab9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6ab9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ab9-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6ab9-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




