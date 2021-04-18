---
description: Il programma di installazione imposta la proprietà VersionNT sul numero di versione del sistema operativo, non definito se il sistema operativo non è Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 o Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Proprietà VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328755"
---
# <a name="versionnt-property"></a><span data-ttu-id="70769-103">Proprietà VersionNT</span><span class="sxs-lookup"><span data-stu-id="70769-103">VersionNT property</span></span>

<span data-ttu-id="70769-104">Il programma di installazione imposta la proprietà **VersionNT** sul numero di versione del sistema operativo, non definito se il sistema operativo non è Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70769-104">The installer sets the **VersionNT** property to the version number for the operating system, undefined if the operating system is not Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="70769-105">Il valore è un numero intero: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="70769-105">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="70769-106">Questa proprietà può essere utilizzata dalle istruzioni condizionali che dipendono dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="70769-106">Conditional statements that depend upon the operating system can use this property.</span></span>

<span data-ttu-id="70769-107">Vedere anche [valori delle proprietà del sistema operativo](operating-system-property-values.md).</span><span class="sxs-lookup"><span data-stu-id="70769-107">See also [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70769-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="70769-108">Remarks</span></span>

<span data-ttu-id="70769-109">Le espressioni di condizione possono eseguire il test per Windows NT, Windows 2000 o Windows XP utilizzando il nome della proprietà oppure possono verificare la versione utilizzando un operatore di confronto.</span><span class="sxs-lookup"><span data-stu-id="70769-109">Condition expressions can test for Windows NT, Windows 2000, or Windows XP by using the property name, or may verify the version by using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="70769-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70769-110">Requirements</span></span>



| <span data-ttu-id="70769-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="70769-111">Requirement</span></span> | <span data-ttu-id="70769-112">Valore</span><span class="sxs-lookup"><span data-stu-id="70769-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70769-113">Versione</span><span class="sxs-lookup"><span data-stu-id="70769-113">Version</span></span><br/> | <span data-ttu-id="70769-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70769-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="70769-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="70769-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="70769-116">Windows Installer in Windows Server 2003 o Windows XP, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack di Windows minimo richiesto da una versione di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="70769-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70769-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70769-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70769-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70769-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




