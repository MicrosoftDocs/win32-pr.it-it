---
description: Inserisce l'oggetto utente specificato accanto alla riga per la risoluzione dei nomi.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Metodo DiskQuotaControl. GiveUserNameResolutionPriority (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525332"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a><span data-ttu-id="bd4ef-103">DiskQuotaControl. GiveUserNameResolutionPriority, metodo</span><span class="sxs-lookup"><span data-stu-id="bd4ef-103">DiskQuotaControl.GiveUserNameResolutionPriority method</span></span>

<span data-ttu-id="bd4ef-104">Inserisce l'oggetto utente specificato accanto alla riga per la risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bd4ef-104">Places the specified user object next in line for name resolution.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd4ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd4ef-105">Syntax</span></span>


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="bd4ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd4ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd4ef-107">*oUser (valore*</span><span class="sxs-lookup"><span data-stu-id="bd4ef-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="bd4ef-108">Tipo: **Object**</span><span class="sxs-lookup"><span data-stu-id="bd4ef-108">Type: **Object**</span></span>

<span data-ttu-id="bd4ef-109">Espressione di oggetto che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bd4ef-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd4ef-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd4ef-110">Return value</span></span>

<span data-ttu-id="bd4ef-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bd4ef-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd4ef-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd4ef-112">Remarks</span></span>

<span data-ttu-id="bd4ef-113">Se la risoluzione dei nomi asincrona è abilitata, gli oggetti utente vengono inseriti in una coda.</span><span class="sxs-lookup"><span data-stu-id="bd4ef-113">If asynchronous name resolution is enabled, user objects are placed in a queue.</span></span> <span data-ttu-id="bd4ef-114">Per impostazione predefinita, vengono serviti nell'ordine in cui vengono inseriti nella coda.</span><span class="sxs-lookup"><span data-stu-id="bd4ef-114">By default, they are serviced in the order they are placed in the queue.</span></span> <span data-ttu-id="bd4ef-115">Il metodo **GiveUserNameResolutionPriority** sposta un oggetto all'inizio della coda in modo che sia successivo in linea da servire.</span><span class="sxs-lookup"><span data-stu-id="bd4ef-115">The **GiveUserNameResolutionPriority** method moves an object to the front of the queue so that it is next in line to be serviced.</span></span>

<span data-ttu-id="bd4ef-116">Utilizzare la proprietà [**UserNameResolution**](diskquotacontrol-usernameresolution.md) per abilitare la risoluzione dei nomi asincrona.</span><span class="sxs-lookup"><span data-stu-id="bd4ef-116">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to enable asynchronous name resolution.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd4ef-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd4ef-117">Requirements</span></span>



| <span data-ttu-id="bd4ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd4ef-118">Requirement</span></span> | <span data-ttu-id="bd4ef-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bd4ef-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd4ef-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd4ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd4ef-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd4ef-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd4ef-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd4ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd4ef-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd4ef-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bd4ef-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd4ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd4ef-125"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd4ef-125"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="bd4ef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bd4ef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd4ef-127"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bd4ef-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd4ef-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd4ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd4ef-129">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="bd4ef-129">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




