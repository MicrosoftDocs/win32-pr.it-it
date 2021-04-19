---
description: Definisce i dati da utilizzare nella verifica Microsoft Authenticode dei dati dell'elemento.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: Struttura PST_AUTHENTICODEDATA (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328038"
---
# <a name="pst_authenticodedata-structure"></a><span data-ttu-id="5c5fe-103">\_Struttura AUTHENTICODEDATA PST</span><span class="sxs-lookup"><span data-stu-id="5c5fe-103">PST\_AUTHENTICODEDATA structure</span></span>

<span data-ttu-id="5c5fe-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5c5fe-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5c5fe-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5c5fe-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="5c5fe-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5c5fe-108">Definisce i dati da utilizzare nella verifica Microsoft Authenticode dei dati dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-108">Defines data to be used in Microsoft Authenticode verification of item data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5fe-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c5fe-109">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a><span data-ttu-id="5c5fe-110">Members</span><span class="sxs-lookup"><span data-stu-id="5c5fe-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c5fe-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="5c5fe-112">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-113">**dwModifiers**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-113">**dwModifiers**</span></span>
</dt> <dd>

<span data-ttu-id="5c5fe-114">Valore che identifica il modificatore che una di una catena di chiamanti deve verificare.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-114">A value that identifies the modifier that one of a chain of callers must verify.</span></span>



| <span data-ttu-id="5c5fe-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5c5fe-115">Value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="5c5fe-116">Significato</span><span class="sxs-lookup"><span data-stu-id="5c5fe-116">Meaning</span></span>                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <span data-ttu-id="5c5fe-117"><dt>**Pst \_ \_Singolo \_ chiamante AC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-117"><dt>**PST\_AC\_SINGLE\_CALLER**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="5c5fe-118">Solo un singolo livello nella catena di chiamate a PStore.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-118">Only a single level in the call chain to PStore.</span></span> <span data-ttu-id="5c5fe-119">Il chiamante supera il controllo di verifica.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-119">The caller passes the verification check.</span></span> <span data-ttu-id="5c5fe-120">L'immagine specificata è il chiamante immediato e è un'applicazione (exe).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-120">The specified image is the immediate caller, and is an application (.exe).</span></span><br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <span data-ttu-id="5c5fe-121"><dt>**Pst \_ \_Chiamante di \_ livello \_ superiore AC**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-121"><dt>**PST\_AC\_TOP\_LEVEL\_CALLER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="5c5fe-122">Il chiamante di livello superiore deve superare il controllo, ma potrebbero essere presenti dll intermedie.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-122">The top-level caller must pass the check, but there may be intermediate DLLs.</span></span> <span data-ttu-id="5c5fe-123">L'immagine specificata non è necessariamente il chiamante immediato e è un'applicazione (exe).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-123">The specified image is not necessarily the immediate caller, and is an application (.exe).</span></span><br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <span data-ttu-id="5c5fe-124"><dt>**Pst \_ \_ \_ Chiamante immediato AC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-124"><dt>**PST\_AC\_IMMEDIATE\_CALLER**</dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="5c5fe-125">Il chiamante immediato deve superare il controllo, ma non deve essere il processo di primo livello.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-125">The immediate caller must pass the check, but need not be the top-level process.</span></span> <span data-ttu-id="5c5fe-126">L'immagine specificata è il chiamante immediato e l'immagine può essere un'applicazione (con estensione exe) o una DLL.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-126">The specified image is the immediate caller, and the image can be an application (.exe) or a DLL.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c5fe-127">**szRootCA**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-127">**szRootCA**</span></span>
</dt> <dd>

<span data-ttu-id="5c5fe-128">Puntatore a una stringa di caratteri wide che rappresenta l'autorità di certificazione radice (CA) per il certificato. usare **null** per usare un'autorità di certificazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-128">A pointer to a wide character string that represents the root certification authority (CA) for the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-129">**szIssuer**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-129">**szIssuer**</span></span>
</dt> <dd>

<span data-ttu-id="5c5fe-130">Puntatore a una stringa di caratteri wide che rappresenta l'autorità di certificazione che ha emesso il certificato. usare **null** per usare un'autorità di certificazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-130">A pointer to a wide character string that represents the CA that issued the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-131">**szPublisher**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-131">**szPublisher**</span></span>
</dt> <dd>

<span data-ttu-id="5c5fe-132">Puntatore a una stringa di caratteri wide che rappresenta l'autore del software; usare **null** per usare un'autorità di certificazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-132">A pointer to a wide character string that represents the software publisher; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-133">**szProgramName**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-133">**szProgramName**</span></span>
</dt> <dd>

<span data-ttu-id="5c5fe-134">Puntatore a una stringa di caratteri wide che rappresenta il nome del programma; usare **null** per usare un'autorità di certificazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-134">A pointer to a wide character string that represents the program name; use **NULL** to use any available CA.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c5fe-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c5fe-135">Requirements</span></span>



| <span data-ttu-id="5c5fe-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c5fe-136">Requirement</span></span> | <span data-ttu-id="5c5fe-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5c5fe-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5fe-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c5fe-138">Header</span></span><br/> | <dl> <span data-ttu-id="5c5fe-139"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-139"><dt>Pstore.h</dt></span></span> </dl> |



 

 
