---
description: Crea un profilo utente per un utente specificato.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: CreateUserProfileEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982947"
---
# <a name="createuserprofileex-function"></a><span data-ttu-id="df7ef-103">CreateUserProfileEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="df7ef-103">CreateUserProfileEx function</span></span>

<span data-ttu-id="df7ef-104">\[Questa funzione non è disponibile a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="df7ef-104">\[This function is not available as of Windows Vista.\]</span></span>

<span data-ttu-id="df7ef-105">Crea un profilo utente per un utente specificato.</span><span class="sxs-lookup"><span data-stu-id="df7ef-105">Creates a user profile for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="df7ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df7ef-106">Syntax</span></span>


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a><span data-ttu-id="df7ef-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="df7ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df7ef-108">*PSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df7ef-108">*pSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df7ef-109">Tipo: **PSID**</span><span class="sxs-lookup"><span data-stu-id="df7ef-109">Type: **PSID**</span></span>

<span data-ttu-id="df7ef-110">SID del nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="df7ef-110">The SID of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="df7ef-111">*lpUsername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df7ef-111">*lpUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df7ef-112">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="df7ef-112">Type: **LPCTSTR**</span></span>

<span data-ttu-id="df7ef-113">Puntatore a un buffer contenente il nome utente del nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="df7ef-113">Pointer to a buffer that contains the user name of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="df7ef-114">*lpUserHive* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="df7ef-114">*lpUserHive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="df7ef-115">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="df7ef-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="df7ef-116">Puntatore a un buffer che contiene l' [hive del registro di sistema](../sysinfo/registry-hives.md) da usare.</span><span class="sxs-lookup"><span data-stu-id="df7ef-116">Pointer to a buffer that contains the [registry hive](../sysinfo/registry-hives.md) to use.</span></span> <span data-ttu-id="df7ef-117">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df7ef-117">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df7ef-118">*lpProfileDir* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="df7ef-118">*lpProfileDir* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="df7ef-119">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="df7ef-119">Type: **LPTSTR**</span></span>

<span data-ttu-id="df7ef-120">Puntatore a un buffer che, quando questa funzione restituisce, riceve il percorso della directory del profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="df7ef-120">Pointer to a buffer that, when this function returns, receives the user's profile directory path.</span></span> <span data-ttu-id="df7ef-121">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df7ef-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df7ef-122">*dwDirSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df7ef-122">*dwDirSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df7ef-123">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="df7ef-123">Type: **DWORD**</span></span>

<span data-ttu-id="df7ef-124">Dimensioni del buffer specificato da *lpProfileDir*, in TCHARs.</span><span class="sxs-lookup"><span data-stu-id="df7ef-124">Size of the buffer specified by *lpProfileDir*, in TCHARs.</span></span>

</dd> <dt>

<span data-ttu-id="df7ef-125">*bWin9xUpg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df7ef-125">*bWin9xUpg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df7ef-126">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="df7ef-126">Type: **BOOL**</span></span>

<span data-ttu-id="df7ef-127">**True** se il profilo utente viene creato come parte della migrazione di un profilo da Windows 9x; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="df7ef-127">**TRUE** if the user profile is being created as part of a profile migration from Windows 9x; otherwise, **FALSE**.</span></span>

<span data-ttu-id="df7ef-128">Se è **true**, il profilo utente viene configurato nella directory predefinita del profilo, in genere C: \\ Documents and Settings \\ *username*.</span><span class="sxs-lookup"><span data-stu-id="df7ef-128">When **TRUE**, the user profile is set up in the default profile directory—normally C:\\Documents and Settings\\*UserName*.</span></span> <span data-ttu-id="df7ef-129">Se la directory esiste già, viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="df7ef-129">If that directory already exists, it is used.</span></span> <span data-ttu-id="df7ef-130">In caso contrario, viene creato.</span><span class="sxs-lookup"><span data-stu-id="df7ef-130">If it does not, it is created.</span></span>

<span data-ttu-id="df7ef-131">Se **false**, la directory predefinita del profilo viene creata se non esiste.</span><span class="sxs-lookup"><span data-stu-id="df7ef-131">If **FALSE**, the default profile directory is created if it does not exist.</span></span> <span data-ttu-id="df7ef-132">Se la directory predefinita del profilo esiste già, per questo profilo utente viene creata una nuova directory.</span><span class="sxs-lookup"><span data-stu-id="df7ef-132">If the default profile directory already exists, a new directory is created for this user profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df7ef-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df7ef-133">Return value</span></span>

<span data-ttu-id="df7ef-134">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="df7ef-134">Type: **BOOL**</span></span>

<span data-ttu-id="df7ef-135">Restituisce **true** se il nuovo profilo utente è stato creato correttamente; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="df7ef-135">Returns **TRUE** if the new user profile was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="df7ef-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="df7ef-136">Remarks</span></span>

<span data-ttu-id="df7ef-137">Questa funzione non è dichiarata nelle intestazioni Software Development Kit (SDK) e non dispone di librerie di importazione associate.</span><span class="sxs-lookup"><span data-stu-id="df7ef-137">This function is not declared in the software development kit (SDK) headers and has no associated import library.</span></span> <span data-ttu-id="df7ef-138">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento a Userenv.dll.</span><span class="sxs-lookup"><span data-stu-id="df7ef-138">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to link to Userenv.dll.</span></span> <span data-ttu-id="df7ef-139">Viene fatto riferimento alla versione ANSI della funzione **CreateUserProfileExA** da Userenv.dll come ordinale 153.</span><span class="sxs-lookup"><span data-stu-id="df7ef-139">The ANSI version of the function, **CreateUserProfileExA** is referenced from Userenv.dll as ordinal 153.</span></span> <span data-ttu-id="df7ef-140">Per la versione Unicode viene fatto riferimento a **CreateUserProfileExW** come ordinale 154.</span><span class="sxs-lookup"><span data-stu-id="df7ef-140">The Unicode version, **CreateUserProfileExW** is referenced as ordinal 154.</span></span>

## <a name="requirements"></a><span data-ttu-id="df7ef-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df7ef-141">Requirements</span></span>



| <span data-ttu-id="df7ef-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="df7ef-142">Requirement</span></span> | <span data-ttu-id="df7ef-143">Valore</span><span class="sxs-lookup"><span data-stu-id="df7ef-143">Value</span></span> |
|-----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df7ef-144">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="df7ef-144">End of client support</span></span><br/>  | <span data-ttu-id="df7ef-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="df7ef-145">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="df7ef-146">DLL</span><span class="sxs-lookup"><span data-stu-id="df7ef-146">DLL</span></span><br/>                    | <dl> <span data-ttu-id="df7ef-147"><dt>Userenv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df7ef-147"><dt>Userenv.dll</dt></span></span> </dl> |
| <span data-ttu-id="df7ef-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="df7ef-148">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="df7ef-149">**CreateUserProfileExW** (Unicode) e **CreateUserProfileExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="df7ef-149">**CreateUserProfileExW** (Unicode) and **CreateUserProfileExA** (ANSI)</span></span><br/>      |



 

 
