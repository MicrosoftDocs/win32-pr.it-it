---
description: Arresta il thread di risoluzione del nome utente.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Metodo DiskQuotaControl. ShutdownNameResolution (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049438"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a><span data-ttu-id="8534d-103">DiskQuotaControl. ShutdownNameResolution, metodo</span><span class="sxs-lookup"><span data-stu-id="8534d-103">DiskQuotaControl.ShutdownNameResolution method</span></span>

<span data-ttu-id="8534d-104">Arresta il thread di risoluzione del nome utente.</span><span class="sxs-lookup"><span data-stu-id="8534d-104">Shuts down the user name resolution thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="8534d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8534d-105">Syntax</span></span>


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a><span data-ttu-id="8534d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8534d-106">Parameters</span></span>

<span data-ttu-id="8534d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8534d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8534d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8534d-108">Return value</span></span>

<span data-ttu-id="8534d-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8534d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8534d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8534d-110">Remarks</span></span>

<span data-ttu-id="8534d-111">Il resolver di nomi SID (ID di sicurezza) converte il SID in nomi utente in un thread in background.</span><span class="sxs-lookup"><span data-stu-id="8534d-111">The security identifier (SID) name resolver translates SID to user names on a background thread.</span></span> <span data-ttu-id="8534d-112">Questo thread viene arrestato automaticamente quando l'oggetto di controllo della quota associato viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="8534d-112">This thread is shut down automatically when the associated quota control object is destroyed.</span></span> <span data-ttu-id="8534d-113">Tuttavia, esistono alcuni casi in cui il thread non è più necessario, ma l'oggetto non è ancora pronto per essere eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="8534d-113">However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.</span></span> <span data-ttu-id="8534d-114">Un esempio tipico è quando non vengono eseguite altre elaborazioni, ma i client continuano a mantenere i riferimenti all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8534d-114">A typical example is when no further processing is taking place, but clients are still holding references to the object.</span></span> <span data-ttu-id="8534d-115">Il metodo **ShutdownNameResolution** consente di terminare il thread del resolver e liberare le risorse associate senza eliminare definitivamente l'oggetto di controllo della quota.</span><span class="sxs-lookup"><span data-stu-id="8534d-115">The **ShutdownNameResolution** method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.</span></span>

> [!Note]  
> <span data-ttu-id="8534d-116">Quando si arresta il thread del resolver, la risoluzione dei nomi asincrona viene arrestata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="8534d-116">When you shut down the resolver thread, asynchronous name resolution immediately stops.</span></span> <span data-ttu-id="8534d-117">Se vengono successivamente effettuate chiamate a metodi quali [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md), l'oggetto quota potrebbe ricreare il thread del resolver.</span><span class="sxs-lookup"><span data-stu-id="8534d-117">If calls are subsequently made to methods such as [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md), the quota object might re-create the resolver thread.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8534d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8534d-118">Requirements</span></span>



| <span data-ttu-id="8534d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8534d-119">Requirement</span></span> | <span data-ttu-id="8534d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8534d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8534d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8534d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8534d-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8534d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8534d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8534d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8534d-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8534d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8534d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8534d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8534d-126"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="8534d-126"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="8534d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8534d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8534d-128"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8534d-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8534d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8534d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8534d-130">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="8534d-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




