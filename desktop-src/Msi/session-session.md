---
description: La proprietà Property dell'oggetto Session è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata gestita dall'oggetto Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Proprietà Session. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333037"
---
# <a name="sessionproperty-property"></a><span data-ttu-id="6a58b-103">Proprietà Session. Property</span><span class="sxs-lookup"><span data-stu-id="6a58b-103">Session.Property property</span></span>

<span data-ttu-id="6a58b-104">La proprietà **Property** dell'oggetto [**Session**](session-object.md) è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata, gestita dall'oggetto **Session** nella tabella delle proprietà in memoria, oppure, se è preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="6a58b-104">The **Property** property of the [**Session**](session-object.md) object is a read-write property that represents the string value of a named installer property, as maintained by the **Session** object in the in-memory Property table, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="6a58b-105">È possibile specificare valori stringa o Integer.</span><span class="sxs-lookup"><span data-stu-id="6a58b-105">Either string or integer values may be supplied.</span></span> <span data-ttu-id="6a58b-106">Una proprietà o una variabile di ambiente non esistente è equivalente al valore null.</span><span class="sxs-lookup"><span data-stu-id="6a58b-106">A non-existent property or environment variable is equivalent to its value being Null.</span></span>

<span data-ttu-id="6a58b-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6a58b-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a58b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a58b-108">Syntax</span></span>


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="6a58b-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6a58b-109">Property value</span></span>

<span data-ttu-id="6a58b-110">Nome obbligatorio con distinzione tra maiuscole e minuscole di una proprietà o nome di una variabile di ambiente preceduto da un segno di percentuale (%).</span><span class="sxs-lookup"><span data-stu-id="6a58b-110">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a58b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a58b-111">Requirements</span></span>



| <span data-ttu-id="6a58b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a58b-112">Requirement</span></span> | <span data-ttu-id="6a58b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6a58b-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a58b-114">Versione</span><span class="sxs-lookup"><span data-stu-id="6a58b-114">Version</span></span><br/> | <span data-ttu-id="6a58b-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a58b-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a58b-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a58b-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a58b-117">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a58b-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6a58b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6a58b-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="6a58b-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a58b-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6a58b-120">IID</span><span class="sxs-lookup"><span data-stu-id="6a58b-120">IID</span></span><br/>     | <span data-ttu-id="6a58b-121">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6a58b-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




