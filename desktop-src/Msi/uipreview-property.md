---
description: La proprietà Property dell'oggetto UIPreview è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata oppure, se è preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Proprietà UIPreview. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327915"
---
# <a name="uipreviewproperty-property"></a><span data-ttu-id="1c378-103">Proprietà UIPreview. Property</span><span class="sxs-lookup"><span data-stu-id="1c378-103">UIPreview.Property property</span></span>

<span data-ttu-id="1c378-104">La proprietà **Property** dell'oggetto [**UIPreview**](uipreview-object.md) è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata oppure, se è preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="1c378-104">The **Property** property of the [**UIPreview**](uipreview-object.md) object is a read-write property that represents the string value of a named installer property, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="1c378-105">Questa operazione viene esposta per consentire la visualizzazione corretta delle finestre di dialogo che dipendono dai valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c378-105">This is exposed to allow proper display of dialog boxes that are dependent upon property values.</span></span> <span data-ttu-id="1c378-106">È possibile specificare valori stringa o Integer.</span><span class="sxs-lookup"><span data-stu-id="1c378-106">Either string or integer values may be supplied.</span></span> <span data-ttu-id="1c378-107">Una proprietà o una variabile di ambiente inesistente è equivalente al valore null.</span><span class="sxs-lookup"><span data-stu-id="1c378-107">A nonexistent property or environment variable is equivalent to its value being null.</span></span>

<span data-ttu-id="1c378-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1c378-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c378-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c378-109">Syntax</span></span>


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="1c378-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1c378-110">Property value</span></span>

<span data-ttu-id="1c378-111">Nome obbligatorio con distinzione tra maiuscole e minuscole di una proprietà o nome di una variabile di ambiente preceduto da un segno di percentuale (%).</span><span class="sxs-lookup"><span data-stu-id="1c378-111">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c378-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c378-112">Requirements</span></span>



| <span data-ttu-id="1c378-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c378-113">Requirement</span></span> | <span data-ttu-id="1c378-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1c378-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c378-115">Versione</span><span class="sxs-lookup"><span data-stu-id="1c378-115">Version</span></span><br/> | <span data-ttu-id="1c378-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c378-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1c378-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1c378-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1c378-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c378-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1c378-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1c378-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c378-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c378-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1c378-121">IID</span><span class="sxs-lookup"><span data-stu-id="1c378-121">IID</span></span><br/>     | <span data-ttu-id="1c378-122">IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1c378-122">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




