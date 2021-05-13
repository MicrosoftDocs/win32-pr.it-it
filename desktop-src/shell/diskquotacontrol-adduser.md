---
description: Assegna una quota disco non predefinita a un nuovo utente.
title: Metodo DiskQuotaControl.AddUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841532"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="eff2c-103">Metodo DiskQuotaControl.AddUser</span><span class="sxs-lookup"><span data-stu-id="eff2c-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="eff2c-104">Assegna una quota disco non predefinita a un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="eff2c-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="eff2c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eff2c-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="eff2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eff2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eff2c-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="eff2c-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="eff2c-108">Tipo: **CHAR**</span><span class="sxs-lookup"><span data-stu-id="eff2c-108">Type: **CHAR**</span></span>

<span data-ttu-id="eff2c-109">Valore stringa che contiene il nome di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eff2c-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="eff2c-110">Usare la [**proprietà UserNameResolution**](diskquotacontrol-usernameresolution.md) per specificare la modalità di risoluzione del nome.</span><span class="sxs-lookup"><span data-stu-id="eff2c-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eff2c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eff2c-111">Return value</span></span>

<span data-ttu-id="eff2c-112">Tipo: **Oggetto**</span><span class="sxs-lookup"><span data-stu-id="eff2c-112">Type: **Object**</span></span>

<span data-ttu-id="eff2c-113">Restituisce un'espressione oggetto che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eff2c-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eff2c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="eff2c-114">Remarks</span></span>

<span data-ttu-id="eff2c-115">L'file system NTFS crea automaticamente una voce di quota utente quando un utente scrive per la prima volta nel volume.</span><span class="sxs-lookup"><span data-stu-id="eff2c-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="eff2c-116">Alle voci create in questo modo vengono assegnati i valori predefiniti di soglia di avviso e limite di quota rigida per il volume.</span><span class="sxs-lookup"><span data-stu-id="eff2c-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="eff2c-117">Questo metodo consente di creare una voce di quota utente prima che un utente scrive informazioni nel volume.</span><span class="sxs-lookup"><span data-stu-id="eff2c-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="eff2c-118">Restituisce un [**oggetto DIDiskQuotaUser**](didiskquotauser-object.md) che può essere usato per assegnare una soglia di avviso o un valore limite di quota diverso dalle impostazioni predefinite per il volume.</span><span class="sxs-lookup"><span data-stu-id="eff2c-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="eff2c-119">Se l'utente esiste già, non viene creata alcuna nuova voce.</span><span class="sxs-lookup"><span data-stu-id="eff2c-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="eff2c-120">Il metodo restituisce [**l'oggetto DIDiskQuotaUser**](didiskquotauser-object.md) associato alla voce esistente.</span><span class="sxs-lookup"><span data-stu-id="eff2c-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="eff2c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eff2c-121">Requirements</span></span>



| <span data-ttu-id="eff2c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eff2c-122">Requirement</span></span> | <span data-ttu-id="eff2c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="eff2c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eff2c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eff2c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eff2c-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eff2c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eff2c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eff2c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eff2c-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eff2c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eff2c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="eff2c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eff2c-129"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="eff2c-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eff2c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eff2c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff2c-131">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="eff2c-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="eff2c-132">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="eff2c-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="eff2c-133">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="eff2c-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




