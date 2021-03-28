---
description: Si verifica quando sono state risolte le informazioni sul nome per un oggetto DIDiskQuotaUser.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Funzione OnUserNameChanged (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346436"
---
# <a name="onusernamechanged-function"></a><span data-ttu-id="9357d-103">OnUserNameChanged (funzione)</span><span class="sxs-lookup"><span data-stu-id="9357d-103">OnUserNameChanged function</span></span>

<span data-ttu-id="9357d-104">Si verifica quando sono state risolte le informazioni sul nome per un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9357d-104">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span>

## <a name="parameters"></a><span data-ttu-id="9357d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="9357d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9357d-106">*oUser (valore*</span><span class="sxs-lookup"><span data-stu-id="9357d-106">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="9357d-107">**Oggetto** che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) associato all'utente il cui nome è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="9357d-107">The **Object** that evaluates to the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the user whose name has been resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9357d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9357d-108">Return value</span></span>

<span data-ttu-id="9357d-109">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9357d-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9357d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9357d-110">Remarks</span></span>

<span data-ttu-id="9357d-111">Quando un client [**enumera gli utenti**](didiskquotauser-object.md)o chiama il metodo [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md) , il nome utente deve essere risolto nell'ID di sicurezza (SID) associato.</span><span class="sxs-lookup"><span data-stu-id="9357d-111">When a client [**enumerates users**](didiskquotauser-object.md), or calls the [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md) method, the user name must be resolved to the associated security ID (SID).</span></span> <span data-ttu-id="9357d-112">Poiché questa procedura può richiedere molto tempo, un client può avere la risoluzione dei nomi eseguita in modo asincrono in un thread in background.</span><span class="sxs-lookup"><span data-stu-id="9357d-112">Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread.</span></span> <span data-ttu-id="9357d-113">Quando il nome di un utente viene risolto, l'oggetto [**DiskQuotaControl**](diskquotacontrol-object.md) invia una notifica al client generando l'evento **OnUserNameChanged** .</span><span class="sxs-lookup"><span data-stu-id="9357d-113">When a user's name is resolved, the [**DiskQuotaControl**](diskquotacontrol-object.md) object notifies its client by firing the **OnUserNameChanged** event.</span></span> <span data-ttu-id="9357d-114">Un oggetto **DIDiskQuotaUser** associato all'utente viene passato come parametro.</span><span class="sxs-lookup"><span data-stu-id="9357d-114">A **DIDiskQuotaUser** object associated with the user is passed as a parameter.</span></span> <span data-ttu-id="9357d-115">Questo oggetto consente al client di modificare le impostazioni di quota dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9357d-115">This object allows the client to modify the user's quota settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="9357d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9357d-116">Requirements</span></span>



| <span data-ttu-id="9357d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9357d-117">Requirement</span></span> | <span data-ttu-id="9357d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9357d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9357d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9357d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9357d-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9357d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9357d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9357d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9357d-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9357d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9357d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9357d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9357d-124"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="9357d-124"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="9357d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9357d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9357d-126"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="9357d-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9357d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9357d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9357d-128">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="9357d-128">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




