---
description: Il metodo FileVersion dell'oggetto Installer restituisce la stringa di versione o la stringa della lingua del percorso specificato nel percorso utilizzando il formato in cui il programma di installazione prevede di trovarle nel database.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324622"
---
# <a name="installerfileversion-method"></a><span data-ttu-id="0915e-103">Installer. FileVersion (metodo)</span><span class="sxs-lookup"><span data-stu-id="0915e-103">Installer.FileVersion method</span></span>

<span data-ttu-id="0915e-104">Il metodo **fileversion** dell'oggetto [**Installer**](installer-object.md) restituisce la stringa di versione o la stringa della lingua del percorso specificato nel *percorso* utilizzando il formato in cui il programma di installazione prevede di trovarle nel database.</span><span class="sxs-lookup"><span data-stu-id="0915e-104">The **FileVersion** method of the [**Installer**](installer-object.md) object returns the version string or language string of the path specified in *Path* using the format in which the installer expects to find them in the database.</span></span> <span data-ttu-id="0915e-105">Per le versioni, si tratta di una stringa \# nel \# formato ".. \# . \# ".</span><span class="sxs-lookup"><span data-stu-id="0915e-105">For versions, this is a string in "\#.\#.\#.\#" format.</span></span> <span data-ttu-id="0915e-106">Per la lingua, si tratta dell'ID della lingua decimale.</span><span class="sxs-lookup"><span data-stu-id="0915e-106">For language, this is the decimal language ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="0915e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0915e-107">Syntax</span></span>


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="0915e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0915e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0915e-109">*Percorso*</span><span class="sxs-lookup"><span data-stu-id="0915e-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="0915e-110">Stringa obbligatoria contenente il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="0915e-110">Required string containing the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="0915e-111">*Lingua*</span><span class="sxs-lookup"><span data-stu-id="0915e-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="0915e-112">Flag che indica se il valore restituito è un ID lingua o una stringa di versione.</span><span class="sxs-lookup"><span data-stu-id="0915e-112">Flag for designating whether the returned value is a language ID or version string.</span></span> <span data-ttu-id="0915e-113">TRUE restituisce il linguaggio, FALSE restituisce la versione.</span><span class="sxs-lookup"><span data-stu-id="0915e-113">TRUE returns the language, FALSE returns the version.</span></span> <span data-ttu-id="0915e-114">Questo parametro è facoltativo e il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="0915e-114">This parameter is optional, with a default value of FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0915e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0915e-115">Return value</span></span>

<span data-ttu-id="0915e-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0915e-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0915e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0915e-117">Requirements</span></span>



| <span data-ttu-id="0915e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0915e-118">Requirement</span></span> | <span data-ttu-id="0915e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0915e-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0915e-120">Versione</span><span class="sxs-lookup"><span data-stu-id="0915e-120">Version</span></span><br/> | <span data-ttu-id="0915e-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0915e-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0915e-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0915e-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0915e-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0915e-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0915e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0915e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="0915e-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0915e-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0915e-126">IID</span><span class="sxs-lookup"><span data-stu-id="0915e-126">IID</span></span><br/>     | <span data-ttu-id="0915e-127">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0915e-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




