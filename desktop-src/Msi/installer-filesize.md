---
description: Il metodo Filesize dell'oggetto Installer usa le chiamate API Win32 per restituire le dimensioni del file specificato in path.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Metodo Installer. Filesize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324623"
---
# <a name="installerfilesize-method"></a><span data-ttu-id="e8935-103">Metodo Installer. Filesize</span><span class="sxs-lookup"><span data-stu-id="e8935-103">Installer.FileSize method</span></span>

<span data-ttu-id="e8935-104">Il metodo **Filesize** dell'oggetto [**Installer**](installer-object.md) usa le chiamate API Win32 per restituire le dimensioni del file specificato in *path*.</span><span class="sxs-lookup"><span data-stu-id="e8935-104">The **FileSize** method of the [**Installer**](installer-object.md) object uses Win32 API calls to return the size of the file specified in *Path*.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8935-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8935-105">Syntax</span></span>


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="e8935-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8935-107">*Percorso*</span><span class="sxs-lookup"><span data-stu-id="e8935-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="e8935-108">Stringa obbligatoria contenente il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="e8935-108">Required string containing the path to the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8935-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8935-109">Return value</span></span>

<span data-ttu-id="e8935-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e8935-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8935-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8935-111">Requirements</span></span>



| <span data-ttu-id="e8935-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8935-112">Requirement</span></span> | <span data-ttu-id="e8935-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e8935-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8935-114">Versione</span><span class="sxs-lookup"><span data-stu-id="e8935-114">Version</span></span><br/> | <span data-ttu-id="e8935-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e8935-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e8935-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8935-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e8935-117">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8935-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e8935-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e8935-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="e8935-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8935-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e8935-120">IID</span><span class="sxs-lookup"><span data-stu-id="e8935-120">IID</span></span><br/>     | <span data-ttu-id="e8935-121">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e8935-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




