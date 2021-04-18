---
description: Scrive l'hive del registro di sistema offline specificato in un file.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Funzione ORSaveHive (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325102"
---
# <a name="orsavehive-function"></a><span data-ttu-id="2baa4-103">ORSaveHive (funzione)</span><span class="sxs-lookup"><span data-stu-id="2baa4-103">ORSaveHive function</span></span>

<span data-ttu-id="2baa4-104">Scrive l'hive del registro di sistema offline specificato in un file.</span><span class="sxs-lookup"><span data-stu-id="2baa4-104">Writes the specified offline registry hive to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2baa4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2baa4-105">Syntax</span></span>


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="2baa4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2baa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2baa4-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2baa4-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2baa4-108">Handle per l'hive del registro di sistema offline da salvare.</span><span class="sxs-lookup"><span data-stu-id="2baa4-108">A handle to the offline registry hive to save.</span></span>

</dd> <dt>

<span data-ttu-id="2baa4-109">*lpHivePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2baa4-109">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2baa4-110">Puntatore a una stringa Unicode che specifica il nome del file hive del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2baa4-110">A pointer to a Unicode string that specifies the name of the registry hive file.</span></span> <span data-ttu-id="2baa4-111">Non può corrispondere al nome di un file esistente.</span><span class="sxs-lookup"><span data-stu-id="2baa4-111">This cannot be the name of an existing file.</span></span>

</dd> <dt>

<span data-ttu-id="2baa4-112">*dwOsMajorVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2baa4-112">*dwOsMajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2baa4-113">Numero di versione principale del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2baa4-113">The major version number of the operating system.</span></span> <span data-ttu-id="2baa4-114">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2baa4-114">This member can be one of the following values.</span></span>



| <span data-ttu-id="2baa4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2baa4-115">Value</span></span>                                                                        | <span data-ttu-id="2baa4-116">Significato</span><span class="sxs-lookup"><span data-stu-id="2baa4-116">Meaning</span></span>                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2baa4-117"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2baa4-117"><dt>5</dt></span></span> </dl> | <span data-ttu-id="2baa4-118">Se *dwOsMinorVersion* è 1, il sistema operativo è Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2baa4-118">If *dwOsMinorVersion* is 1, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="2baa4-119">Se *dwOsMinorVersion* è 2, il sistema operativo è windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="2baa4-119">If *dwOsMinorVersion* is 2, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span><br/> |
| <dl> <span data-ttu-id="2baa4-120"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2baa4-120"><dt>6</dt></span></span> </dl> | <span data-ttu-id="2baa4-121">Se *dwOsMinorVersion* è 0, il sistema operativo è windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2baa4-121">If *dwOsMinorVersion* is 0, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/> <span data-ttu-id="2baa4-122">Se *dwOsMinorVersion* è 1, il sistema operativo è windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2baa4-122">If *dwOsMinorVersion* is 1, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="2baa4-123">*dwOsMinorVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2baa4-123">*dwOsMinorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2baa4-124">Numero di versione secondario del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2baa4-124">The minor version number of the operating system.</span></span> <span data-ttu-id="2baa4-125">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2baa4-125">This member can be one of the following values.</span></span>



| <span data-ttu-id="2baa4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2baa4-126">Value</span></span>                                                                        | <span data-ttu-id="2baa4-127">Significato</span><span class="sxs-lookup"><span data-stu-id="2baa4-127">Meaning</span></span>                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2baa4-128"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2baa4-128"><dt>0</dt></span></span> </dl> | <span data-ttu-id="2baa4-129">Se *dwOsMajorVersion* è 6, il sistema operativo è windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2baa4-129">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="2baa4-130"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2baa4-130"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2baa4-131">Se *dwOsMajorVersion* è 5, il sistema operativo è Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2baa4-131">If *dwOsMajorVersion* is 5, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="2baa4-132">Se *dwOsMajorVersion* è 6, il sistema operativo è windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2baa4-132">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="2baa4-133"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2baa4-133"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2baa4-134">Se *dwOsMajorVersion* è 5, il sistema operativo è windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="2baa4-134">If *dwOsMajorVersion* is 5, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span> <br/> <span data-ttu-id="2baa4-135">Se *dwOsMajorVersion* è 6, il parametro *dwOsMinorVersion* deve essere 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="2baa4-135">If *dwOsMajorVersion* is 6, the *dwOsMinorVersion* parameter must be 0 or 1.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2baa4-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2baa4-136">Return value</span></span>

<span data-ttu-id="2baa4-137">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2baa4-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="2baa4-138">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="2baa4-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="2baa4-139">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="2baa4-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="2baa4-140">I codici di errore possibili includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2baa4-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="2baa4-141">Se il chiamante non dispone dei diritti di accesso necessari per scrivere il file, la funzione restituisce l'errore di \_ accesso \_ negato.</span><span class="sxs-lookup"><span data-stu-id="2baa4-141">If the caller does not have the necessary access rights to write the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="2baa4-142">Se il file specificato esiste già, la funzione restituisce un errore \_ già \_ esistente.</span><span class="sxs-lookup"><span data-stu-id="2baa4-142">If the specified file already exists, the function returns ERROR\_ALREADY\_EXISTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="2baa4-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="2baa4-143">Remarks</span></span>

<span data-ttu-id="2baa4-144">Per salvare le modifiche apportate a un hive del registro di sistema offline, è necessario usare la funzione **ORSaveHive** .</span><span class="sxs-lookup"><span data-stu-id="2baa4-144">The **ORSaveHive** function must be used to save changes made to an offline registry hive.</span></span> <span data-ttu-id="2baa4-145">Le modifiche non vengono mantenute fino a quando non viene chiamato **ORSaveHive** per salvare l'hive in un file.</span><span class="sxs-lookup"><span data-stu-id="2baa4-145">Changes are not preserved until **ORSaveHive** is called to save the hive to a file.</span></span>

<span data-ttu-id="2baa4-146">I parametri *dwOsMajorVersion* e *dwOsMinorVersion* insieme specificano il formato di destinazione del file hive del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2baa4-146">The *dwOsMajorVersion* and *dwOsMinorVersion* parameters together specify the target format of the registry hive file.</span></span> <span data-ttu-id="2baa4-147">Nella tabella seguente sono riepilogati i numeri di versione del sistema operativo più recenti.</span><span class="sxs-lookup"><span data-stu-id="2baa4-147">The following table summarizes the most recent operating system version numbers.</span></span>



| <span data-ttu-id="2baa4-148">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2baa4-148">Operating system</span></span>                    | <span data-ttu-id="2baa4-149">Numero di versione</span><span class="sxs-lookup"><span data-stu-id="2baa4-149">Version number</span></span> |
|-------------------------------------|----------------|
| <span data-ttu-id="2baa4-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2baa4-150">Windows Server 2008 R2</span></span>              | <span data-ttu-id="2baa4-151">6.1</span><span class="sxs-lookup"><span data-stu-id="2baa4-151">6.1</span></span>            |
| <span data-ttu-id="2baa4-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2baa4-152">Windows 7</span></span>                           | <span data-ttu-id="2baa4-153">6.1</span><span class="sxs-lookup"><span data-stu-id="2baa4-153">6.1</span></span>            |
| <span data-ttu-id="2baa4-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2baa4-154">Windows Server 2008</span></span>                 | <span data-ttu-id="2baa4-155">6.0</span><span class="sxs-lookup"><span data-stu-id="2baa4-155">6.0</span></span>            |
| <span data-ttu-id="2baa4-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2baa4-156">Windows Vista</span></span>                       | <span data-ttu-id="2baa4-157">6.0</span><span class="sxs-lookup"><span data-stu-id="2baa4-157">6.0</span></span>            |
| <span data-ttu-id="2baa4-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2baa4-158">Windows Server 2003 R2</span></span>              | <span data-ttu-id="2baa4-159">5,2</span><span class="sxs-lookup"><span data-stu-id="2baa4-159">5.2</span></span>            |
| <span data-ttu-id="2baa4-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2baa4-160">Windows Server 2003</span></span>                 | <span data-ttu-id="2baa4-161">5,2</span><span class="sxs-lookup"><span data-stu-id="2baa4-161">5.2</span></span>            |
| <span data-ttu-id="2baa4-162">Windows XP Professional x64 Edition</span><span class="sxs-lookup"><span data-stu-id="2baa4-162">Windows XP Professional x64 Edition</span></span> | <span data-ttu-id="2baa4-163">5,2</span><span class="sxs-lookup"><span data-stu-id="2baa4-163">5.2</span></span>            |
| <span data-ttu-id="2baa4-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2baa4-164">Windows XP</span></span>                          | <span data-ttu-id="2baa4-165">5.1</span><span class="sxs-lookup"><span data-stu-id="2baa4-165">5.1</span></span>            |



 

<span data-ttu-id="2baa4-166">Utilizzare la funzione [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) per recuperare le informazioni sul sistema operativo corrente.</span><span class="sxs-lookup"><span data-stu-id="2baa4-166">Use the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to retrieve information about the current operating system.</span></span>

<span data-ttu-id="2baa4-167">La funzione **ORSaveHive** blocca l'hive del registro di sistema mentre scrive l'hive nel file, quindi chiude il file e rilascia il blocco.</span><span class="sxs-lookup"><span data-stu-id="2baa4-167">The **ORSaveHive** function locks the registry hive while it is writing the hive to the file, then closes the file and releases the lock.</span></span> <span data-ttu-id="2baa4-168">L'hive del registro di sistema rimane in memoria fino a quando non viene chiuso chiamando la funzione [**ORCloseHive**](orclosehive.md) .</span><span class="sxs-lookup"><span data-stu-id="2baa4-168">The registry hive remains in memory until it is closed by calling the [**ORCloseHive**](orclosehive.md) function.</span></span> <span data-ttu-id="2baa4-169">È possibile apportare ulteriori modifiche all'hive del registro di sistema mentre è aperto. Tuttavia, per mantenere queste modifiche, è necessario salvare l'hive in un nuovo file, perché la funzione **ORSaveHive** non sovrascriverà un file esistente.</span><span class="sxs-lookup"><span data-stu-id="2baa4-169">It is possible to make further changes to the registry hive while it is open; however, to preserve these changes the hive must be saved to a new file, because the **ORSaveHive** function will not overwrite an existing file.</span></span>

<span data-ttu-id="2baa4-170">La funzione **ORSaveHive** può essere usata per salvare parte dell'hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="2baa4-170">The **ORSaveHive** function can be used to save part of the offline registry hive.</span></span> <span data-ttu-id="2baa4-171">La chiave specificata nel parametro *handle* diventa la chiave radice di un hive costituita dalla chiave specificata e da tutte le relative sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="2baa4-171">The key specified in the *Handle* parameter becomes the root key of a hive that consists of the specified key and all of its subkeys.</span></span>

## <a name="requirements"></a><span data-ttu-id="2baa4-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2baa4-172">Requirements</span></span>



| <span data-ttu-id="2baa4-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="2baa4-173">Requirement</span></span> | <span data-ttu-id="2baa4-174">Valore</span><span class="sxs-lookup"><span data-stu-id="2baa4-174">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2baa4-175">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2baa4-175">Redistributable</span></span><br/> | <span data-ttu-id="2baa4-176">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="2baa4-176">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="2baa4-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2baa4-177">Header</span></span><br/>          | <dl> <span data-ttu-id="2baa4-178"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2baa4-178"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="2baa4-179">DLL</span><span class="sxs-lookup"><span data-stu-id="2baa4-179">DLL</span></span><br/>             | <dl> <span data-ttu-id="2baa4-180"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2baa4-180"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2baa4-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2baa4-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2baa4-182">GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="2baa4-182">GetVersionEx</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[<span data-ttu-id="2baa4-183">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="2baa4-183">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="2baa4-184">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="2baa4-184">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
