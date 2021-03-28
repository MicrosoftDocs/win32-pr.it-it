---
description: Invalida la cache del nome utente dell'ID di sicurezza.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Metodo DiskQuotaControl. InvalidateSidNameCache (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966521"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a><span data-ttu-id="b602b-103">DiskQuotaControl. InvalidateSidNameCache, metodo</span><span class="sxs-lookup"><span data-stu-id="b602b-103">DiskQuotaControl.InvalidateSidNameCache method</span></span>

<span data-ttu-id="b602b-104">Invalida la cache del nome utente dell'ID di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b602b-104">Invalidates the security ID user name cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="b602b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b602b-105">Syntax</span></span>


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a><span data-ttu-id="b602b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b602b-106">Parameters</span></span>

<span data-ttu-id="b602b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b602b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b602b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b602b-108">Return value</span></span>

<span data-ttu-id="b602b-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b602b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b602b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b602b-110">Remarks</span></span>

<span data-ttu-id="b602b-111">I nomi utente e gli ID di sicurezza associati vengono archiviati in una cache.</span><span class="sxs-lookup"><span data-stu-id="b602b-111">User names and associated security IDs are stored in a cache.</span></span> <span data-ttu-id="b602b-112">È possibile cancellare la cache chiamando **InvalidateSidNameCache**.</span><span class="sxs-lookup"><span data-stu-id="b602b-112">You can clear this cache by calling **InvalidateSidNameCache**.</span></span> <span data-ttu-id="b602b-113">Se successivamente si crea un nuovo oggetto utente, le informazioni dovranno essere ottenute dal controller di dominio e sarà necessario ristabilire la cache.</span><span class="sxs-lookup"><span data-stu-id="b602b-113">If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.</span></span>

## <a name="requirements"></a><span data-ttu-id="b602b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b602b-114">Requirements</span></span>



| <span data-ttu-id="b602b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b602b-115">Requirement</span></span> | <span data-ttu-id="b602b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b602b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b602b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b602b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b602b-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b602b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b602b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b602b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b602b-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b602b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b602b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b602b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b602b-122"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="b602b-122"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="b602b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b602b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b602b-124"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b602b-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b602b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b602b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b602b-126">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="b602b-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




