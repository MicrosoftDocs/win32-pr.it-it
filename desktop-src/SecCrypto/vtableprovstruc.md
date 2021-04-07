---
description: Contiene i puntatori alle funzioni di callback che possono essere utilizzati dalle funzioni del provider del servizio di crittografia (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Struttura VTableProvStruc (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759458"
---
# <a name="vtableprovstruc-structure"></a><span data-ttu-id="f558e-103">Struttura VTableProvStruc</span><span class="sxs-lookup"><span data-stu-id="f558e-103">VTableProvStruc structure</span></span>

<span data-ttu-id="f558e-104">La struttura **VTableProvStruc** contiene i puntatori alle funzioni di callback che possono essere utilizzati dalle funzioni del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="f558e-104">The **VTableProvStruc** structure contains pointers to callback functions that can be used by [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f558e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f558e-105">Syntax</span></span>


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a><span data-ttu-id="f558e-106">Members</span><span class="sxs-lookup"><span data-stu-id="f558e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f558e-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f558e-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="f558e-108">Valore **DWORD** che indica la versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="f558e-108">A **DWORD** value that indicates the version of the structure.</span></span> <span data-ttu-id="f558e-109">Vengono utilizzate tre versioni di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="f558e-109">Three versions of this structure are used.</span></span> <span data-ttu-id="f558e-110">Le versioni sono il numero 1, 2 e 3 e determinano quali membri della struttura sono validi.</span><span class="sxs-lookup"><span data-stu-id="f558e-110">The versions are number 1, 2, and 3, and determine which members of the structure are valid.</span></span> <span data-ttu-id="f558e-111">I membri della versione 1 sono validi in tutti i sistemi che supportano questa struttura.</span><span class="sxs-lookup"><span data-stu-id="f558e-111">Version 1 members are valid on all systems that support this structure.</span></span>

<span data-ttu-id="f558e-112">Si tratta di un membro della versione 1.</span><span class="sxs-lookup"><span data-stu-id="f558e-112">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="f558e-113">**FuncVerifyImage**</span><span class="sxs-lookup"><span data-stu-id="f558e-113">**FuncVerifyImage**</span></span>
</dt> <dd>

<span data-ttu-id="f558e-114">Indirizzo di una funzione di callback [**FuncVerifyImage**](funcverifyimage.md) che il CSP utilizza per verificare la firma di tutte le dll che il CSP caricherà.</span><span class="sxs-lookup"><span data-stu-id="f558e-114">The address of a [**FuncVerifyImage**](funcverifyimage.md) callback function that the CSP uses to verify the signature of any DLLs that the CSP will load.</span></span> <span data-ttu-id="f558e-115">Tutte le DLL ausiliarie in cui un CSP effettua chiamate di funzione devono essere firmate nello stesso modo (e con la stessa chiave) della DLL CSP primaria.</span><span class="sxs-lookup"><span data-stu-id="f558e-115">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="f558e-116">Per garantire la firma, le DLL ausiliarie devono essere caricate in modo dinamico tramite la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="f558e-116">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="f558e-117">Ma prima del caricamento della DLL, è necessario verificare la firma della DLL.</span><span class="sxs-lookup"><span data-stu-id="f558e-117">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="f558e-118">Il CSP esegue questa verifica chiamando la funzione **FuncVerifyImage** , come illustrato nell'esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f558e-118">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

<span data-ttu-id="f558e-119">Questo puntatore a funzione può essere archiviato e utilizzato fino a quando non viene rilasciato il contesto CSP.</span><span class="sxs-lookup"><span data-stu-id="f558e-119">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="f558e-120">Si tratta di un membro della versione 1.</span><span class="sxs-lookup"><span data-stu-id="f558e-120">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="f558e-121">**FuncReturnhWnd**</span><span class="sxs-lookup"><span data-stu-id="f558e-121">**FuncReturnhWnd**</span></span>
</dt> <dd>

<span data-ttu-id="f558e-122">Indirizzo di una funzione di callback [**FuncReturnhWnd**](funcreturnhwnd.md) che restituisce l'handle della finestra che deve essere utilizzato dal CSP come padre o proprietario di qualsiasi interfaccia utente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="f558e-122">The address of a [**FuncReturnhWnd**](funcreturnhwnd.md) callback function that returns the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span> <span data-ttu-id="f558e-123">I CSP che non comunicano direttamente con l'utente e i CSP che utilizzano hardware dedicato a questo scopo possono ignorare questa voce.</span><span class="sxs-lookup"><span data-stu-id="f558e-123">CSPs that do not communicate directly with the user and CSPs that use dedicated hardware for this purpose can ignore this entry.</span></span> <span data-ttu-id="f558e-124">Questo handle di finestra è pari a zero per impostazione predefinita, ma un'applicazione può impostarla su un valore diverso usando la funzione [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) per impostare la proprietà **\_ \_ HWND del client PP** .</span><span class="sxs-lookup"><span data-stu-id="f558e-124">This window handle is zero by default, but an application can set this to a different value by using the [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) function to set the **PP\_CLIENT\_HWND** property.</span></span>

<span data-ttu-id="f558e-125">Questo puntatore a funzione può essere archiviato e utilizzato fino a quando non viene rilasciato il contesto CSP.</span><span class="sxs-lookup"><span data-stu-id="f558e-125">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="f558e-126">Si tratta di un membro della versione 1.</span><span class="sxs-lookup"><span data-stu-id="f558e-126">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="f558e-127">**dwProvType**</span><span class="sxs-lookup"><span data-stu-id="f558e-127">**dwProvType**</span></span>
</dt> <dd>

<span data-ttu-id="f558e-128">Valore **DWORD** che specifica il tipo di provider da acquisire.</span><span class="sxs-lookup"><span data-stu-id="f558e-128">A **DWORD** value that specifies the type of provider to acquire.</span></span> <span data-ttu-id="f558e-129">I [*tipi di provider*](../secgloss/p-gly.md) seguenti sono predefiniti e sono descritti in dettaglio nell' [interoperabilità CSP](https://www.bing.com/search?q=CSP+Interoperability):</span><span class="sxs-lookup"><span data-stu-id="f558e-129">The following [*provider types*](../secgloss/p-gly.md) are predefined and are discussed in detail in [CSP Interoperability](https://www.bing.com/search?q=CSP+Interoperability):</span></span>

-   <span data-ttu-id="f558e-130">PROV \_ RSA \_ completo</span><span class="sxs-lookup"><span data-stu-id="f558e-130">PROV\_RSA\_FULL</span></span>
-   <span data-ttu-id="f558e-131">PROVA \_ RSA \_ sig</span><span class="sxs-lookup"><span data-stu-id="f558e-131">PROV\_RSA\_SIG</span></span>
-   <span data-ttu-id="f558e-132">PROVA \_ DSS</span><span class="sxs-lookup"><span data-stu-id="f558e-132">PROV\_DSS</span></span>
-   <span data-ttu-id="f558e-133">PROVA \_ fortezza</span><span class="sxs-lookup"><span data-stu-id="f558e-133">PROV\_FORTEZZA</span></span>
-   <span data-ttu-id="f558e-134">PROVA \_ MS \_ Exchange</span><span class="sxs-lookup"><span data-stu-id="f558e-134">PROV\_MS\_EXCHANGE</span></span>

<span data-ttu-id="f558e-135">Si tratta di un membro della versione 2.</span><span class="sxs-lookup"><span data-stu-id="f558e-135">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="f558e-136">**pbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="f558e-136">**pbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f558e-137">Puntatore a una matrice di informazioni di contesto.</span><span class="sxs-lookup"><span data-stu-id="f558e-137">A pointer to an array of context information.</span></span> <span data-ttu-id="f558e-138">I membri **pbContextInfo** e **cbContextInfo** determinano il set di informazioni usato quando viene chiamata una funzione [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) con le informazioni sul \_ contesto PP \_ impostate.</span><span class="sxs-lookup"><span data-stu-id="f558e-138">The **pbContextInfo** and **cbContextInfo** members together determine the information set used when a [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) function is called with PP\_CONTEXT\_INFO set.</span></span>

<span data-ttu-id="f558e-139">Si tratta di un membro della versione 2.</span><span class="sxs-lookup"><span data-stu-id="f558e-139">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="f558e-140">**cbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="f558e-140">**cbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f558e-141">Valore **DWORD** che indica il numero di elementi nella matrice **pbContextInfo** .</span><span class="sxs-lookup"><span data-stu-id="f558e-141">A **DWORD** value that indicates the number of elements in the **pbContextInfo** array.</span></span>

<span data-ttu-id="f558e-142">Si tratta di un membro della versione 2.</span><span class="sxs-lookup"><span data-stu-id="f558e-142">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="f558e-143">**pszProvName**</span><span class="sxs-lookup"><span data-stu-id="f558e-143">**pszProvName**</span></span>
</dt> <dd>

<span data-ttu-id="f558e-144">Stringa che contiene il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="f558e-144">A string that contains the name of the provider.</span></span>

<span data-ttu-id="f558e-145">Si tratta di un membro della versione 3.</span><span class="sxs-lookup"><span data-stu-id="f558e-145">This is a version 3 member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f558e-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="f558e-146">Remarks</span></span>

<span data-ttu-id="f558e-147">I puntatori nella struttura **VTableProvStruc** sono disponibili solo all'interno della funzione [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) .</span><span class="sxs-lookup"><span data-stu-id="f558e-147">The pointers in the **VTableProvStruc** structure are only available within the [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) function.</span></span> <span data-ttu-id="f558e-148">Se i membri della struttura sono necessari dopo il completamento di una chiamata a **CPAcquireContext** , le copie degli elementi della struttura necessari devono essere eseguite dal CSP.</span><span class="sxs-lookup"><span data-stu-id="f558e-148">If members of the structure are needed after a call to **CPAcquireContext** is completed, copies of the needed structure elements must be made by the CSP.</span></span> <span data-ttu-id="f558e-149">I puntatori a funzione in questa struttura possono essere archiviati e utilizzati fino a quando non viene rilasciato il contesto CSP.</span><span class="sxs-lookup"><span data-stu-id="f558e-149">The function pointers in this structure can be stored and used until the CSP context is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="f558e-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f558e-150">Requirements</span></span>



| <span data-ttu-id="f558e-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="f558e-151">Requirement</span></span> | <span data-ttu-id="f558e-152">Valore</span><span class="sxs-lookup"><span data-stu-id="f558e-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f558e-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f558e-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f558e-154">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f558e-154">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f558e-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f558e-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f558e-156">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f558e-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f558e-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f558e-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f558e-158"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f558e-158"><dt>Cspdk.h</dt></span></span> </dl> |
| <span data-ttu-id="f558e-159">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f558e-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f558e-160">**VTableProvStrucW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="f558e-160">**VTableProvStrucW** (Unicode)</span></span><br/>                                          |



 

 
