---
description: La proprietà Environment dell'oggetto Installer è una proprietà di lettura/scrittura che corrisponde al valore stringa per una variabile di ambiente del processo corrente.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Proprietà Installer. Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324643"
---
# <a name="installerenvironment-property"></a><span data-ttu-id="82e34-103">Proprietà Installer. Environment</span><span class="sxs-lookup"><span data-stu-id="82e34-103">Installer.Environment property</span></span>

<span data-ttu-id="82e34-104">La proprietà **Environment** dell'oggetto [**Installer**](installer-object.md) è una proprietà di lettura/scrittura che corrisponde al valore stringa per una variabile di ambiente del processo corrente.</span><span class="sxs-lookup"><span data-stu-id="82e34-104">The **Environment** property of the [**Installer**](installer-object.md) object is a read-write property that is the string value for an environment variable of the current process.</span></span>

<span data-ttu-id="82e34-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="82e34-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e34-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82e34-106">Syntax</span></span>


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a><span data-ttu-id="82e34-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="82e34-107">Property value</span></span>

<span data-ttu-id="82e34-108">Nome della variabile di ambiente da leggere o scrivere.</span><span class="sxs-lookup"><span data-stu-id="82e34-108">The name of the environment variable to be read or written.</span></span> <span data-ttu-id="82e34-109">Questa operazione non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="82e34-109">This is case-insensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="82e34-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="82e34-110">Remarks</span></span>

<span data-ttu-id="82e34-111">L'impostazione di una variabile di ambiente con la proprietà **Environment** ha effetto solo sulla sessione attiva.</span><span class="sxs-lookup"><span data-stu-id="82e34-111">Setting an environment variable with the **Environment** property only affects the active session.</span></span> <span data-ttu-id="82e34-112">Per apportare modifiche permanenti a una variabile di ambiente, usare la [tabella Environment](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="82e34-112">To make persistent changes to an environment variable, use the [Environment table](environment-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82e34-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82e34-113">Requirements</span></span>



| <span data-ttu-id="82e34-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e34-114">Requirement</span></span> | <span data-ttu-id="82e34-115">Valore</span><span class="sxs-lookup"><span data-stu-id="82e34-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e34-116">Versione</span><span class="sxs-lookup"><span data-stu-id="82e34-116">Version</span></span><br/> | <span data-ttu-id="82e34-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82e34-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="82e34-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82e34-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="82e34-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="82e34-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="82e34-120">DLL</span><span class="sxs-lookup"><span data-stu-id="82e34-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="82e34-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82e34-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="82e34-122">IID</span><span class="sxs-lookup"><span data-stu-id="82e34-122">IID</span></span><br/>     | <span data-ttu-id="82e34-123">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="82e34-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




