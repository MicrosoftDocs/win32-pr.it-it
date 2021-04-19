---
description: 'Altre informazioni su: struttura JET_USERDEFINEDDEFAULT'
title: Struttura JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318104"
---
# <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="b21dd-103">Struttura JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="b21dd-103">JET_USERDEFINEDDEFAULT Structure</span></span>


<span data-ttu-id="b21dd-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b21dd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="b21dd-105">Struttura JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="b21dd-105">JET_USERDEFINEDDEFAULT Structure</span></span>

<span data-ttu-id="b21dd-106">La struttura **JET_USERDEFINEDDEFAULT** viene specificata in combinazione con JET_bitColumnUserDefinedDefault per assegnare a una nuova colonna un valore predefinito che viene determinato tramite un callback.</span><span class="sxs-lookup"><span data-stu-id="b21dd-106">The **JET_USERDEFINEDDEFAULT** structure is specified in conjunction with JET_bitColumnUserDefinedDefault to give a new column a default value that is determined using a callback.</span></span> <span data-ttu-id="b21dd-107">Questa tecnica può essere utilizzata per implementare le colonne calcolate.</span><span class="sxs-lookup"><span data-stu-id="b21dd-107">This technique can be used to implement computed columns.</span></span>

<span data-ttu-id="b21dd-108">**Windows XP:** La struttura **JET_USERDEFINEDDEFAULT** è stata introdotta in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b21dd-108">**Windows XP:** The **JET_USERDEFINEDDEFAULT** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a><span data-ttu-id="b21dd-109">Membri</span><span class="sxs-lookup"><span data-stu-id="b21dd-109">Members</span></span>

<span data-ttu-id="b21dd-110">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="b21dd-110">**szCallback**</span></span>

<span data-ttu-id="b21dd-111">Nome di esportazione della funzione che implementa il callback nel \! formato "funzione modulo".</span><span class="sxs-lookup"><span data-stu-id="b21dd-111">The export name of the function that implements the callback in "module\!function" format.</span></span>

<span data-ttu-id="b21dd-112">Il callback viene mantenuto come parte dello schema della colonna.</span><span class="sxs-lookup"><span data-stu-id="b21dd-112">The callback persists as a part of the column schema.</span></span> <span data-ttu-id="b21dd-113">Il file eseguibile host effettivo e il nome di esportazione della funzione devono essere salvati in modo permanente per abilitare la ricerca dell'indirizzo reale della funzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b21dd-113">The actual host executable and export name of the function must persist to enable the lookup of the true address of the function at run time.</span></span>

<span data-ttu-id="b21dd-114">Il nome del modulo è il nome del file binario host che contiene la funzione.</span><span class="sxs-lookup"><span data-stu-id="b21dd-114">The module name is the name of the host binary that contains the function.</span></span> <span data-ttu-id="b21dd-115">Il nome della funzione è il nome dell'esportazione per la funzione.</span><span class="sxs-lookup"><span data-stu-id="b21dd-115">The function name is the name of the export for that function.</span></span> <span data-ttu-id="b21dd-116">Queste due informazioni verranno usate dal motore di database in fase di esecuzione per individuare il vero indirizzo del callback eseguendo una chiamata [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sul nome del modulo seguito da una chiamata [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) sul nome della funzione.</span><span class="sxs-lookup"><span data-stu-id="b21dd-116">These two pieces of information will be used by the database engine at runtime to locate the true address of the callback by executing a [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) call on the module name followed by a [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) call on the function name.</span></span>

<span data-ttu-id="b21dd-117">Se, ad esempio, il callback è stato implementato in una DLL denominata MyCallback.DLL e tale DLL è stata archiviata in C: \\ MyApplication e la funzione che implementa il callback è stata esportata dalla dll come UserDefinedDefaultCallback, la stringa richiesta sarà "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".</span><span class="sxs-lookup"><span data-stu-id="b21dd-117">For example, if the callback were implemented in a DLL called MyCallback.DLL and that DLL were stored in C:\\MyApplication and the function implementing the callback were exported from the DLL as UserDefinedDefaultCallback, then the required string would be "C:\\MyApplication\\MyCallback.DLL\!UserDefinedDefaultCallback".</span></span>

<span data-ttu-id="b21dd-118">**Nota**  Incorporato " \! "</span><span class="sxs-lookup"><span data-stu-id="b21dd-118">**Note**  Embedded "\!"</span></span> <span data-ttu-id="b21dd-119">i caratteri nella parte del modulo del nome del callback non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="b21dd-119">characters in the module portion of the callback name are not supported.</span></span>

<span data-ttu-id="b21dd-120">Si consiglia vivamente di utilizzare un nome di callback che non sia una funzione dell'architettura host.</span><span class="sxs-lookup"><span data-stu-id="b21dd-120">It is highly recommended that you use a callback name that is not a function of the host architecture.</span></span> <span data-ttu-id="b21dd-121">Ad esempio, non usare le esportazioni decorate come stdcall ( UserDefinedDefaultCallback@32 ) perché questa convenzione di chiamata è supportata solo su computer x86.</span><span class="sxs-lookup"><span data-stu-id="b21dd-121">For example, do not use exports decorated as stdcall (UserDefinedDefaultCallback@32) because this calling convention is only supported on x86 machines.</span></span> <span data-ttu-id="b21dd-122">Se è stato usato un callback di questo tipo, il database può essere usato solo in un computer x86.</span><span class="sxs-lookup"><span data-stu-id="b21dd-122">If such a callback were used then the database could only be used on an x86 machine.</span></span> <span data-ttu-id="b21dd-123">In questo caso, è necessario usare un alias per eseguire un'esportazione indipendente dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="b21dd-123">An alias should be used to make a platform-agnostic export in this case.</span></span>

<span data-ttu-id="b21dd-124">Si consiglia vivamente di usare il percorso completo del nome del modulo che implementa il callback.</span><span class="sxs-lookup"><span data-stu-id="b21dd-124">It is highly recommended that you use the full path of the module name that is implementing the callback.</span></span> <span data-ttu-id="b21dd-125">Se viene utilizzato un percorso relativo, il processo che ospita il database potrebbe essere soggetto ad attacchi da parte di un file binario non autorizzato.</span><span class="sxs-lookup"><span data-stu-id="b21dd-125">If a relative path is used then the process that is hosting the database might be susceptible to attack by a rogue binary.</span></span>

<span data-ttu-id="b21dd-126">L'applicazione deve passare solo i callback attendibili al motore di database.</span><span class="sxs-lookup"><span data-stu-id="b21dd-126">The application should pass only trusted callbacks to the database engine.</span></span> <span data-ttu-id="b21dd-127">Il motore di database caricherà il file binario per verificarne l'esistenza quando viene creata la colonna associata.</span><span class="sxs-lookup"><span data-stu-id="b21dd-127">The database engine will load the binary to verify its existence when the associated column is created.</span></span> <span data-ttu-id="b21dd-128">Se il percorso del file binario non viene convalidato o considerato attendibile, potrebbe attaccare il processo che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="b21dd-128">If the path to the binary is not validated or known to be trusted then it could attack the process that is hosting the database.</span></span>

<span data-ttu-id="b21dd-129">**pbUserData**</span><span class="sxs-lookup"><span data-stu-id="b21dd-129">**pbUserData**</span></span>

<span data-ttu-id="b21dd-130">Blocco autonomo di dati definiti dall'utente da passare al callback quando viene richiamato. Il blocco di dati fornito verrà mantenuto come parte dello schema della colonna.</span><span class="sxs-lookup"><span data-stu-id="b21dd-130">A self-contained block of user-defined data to be passed to the callback when invoked.The data block that is provided will persist as a part of the column schema.</span></span> <span data-ttu-id="b21dd-131">Di conseguenza, il blocco di dati deve essere completamente indipendente e non può fare riferimento ad alcun dato esterno all'ambito del database.</span><span class="sxs-lookup"><span data-stu-id="b21dd-131">As a result, the data block must be entirely self-contained and cannot refer to any data that is outside the scope of the database.</span></span>

<span data-ttu-id="b21dd-132">Se **pbUserData** è zero, il valore di **cbUserData** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b21dd-132">If **pbUserData** is zero then the value of **cbUserData** is ignored.</span></span> <span data-ttu-id="b21dd-133">In questo caso, non verrà passato alcun dato definito dall'utente al callback quando viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="b21dd-133">In this case, no user-defined data will be passed to the callback when invoked.</span></span>

<span data-ttu-id="b21dd-134">**cbUserData**</span><span class="sxs-lookup"><span data-stu-id="b21dd-134">**cbUserData**</span></span>

<span data-ttu-id="b21dd-135">Vedere **pbUserData**.</span><span class="sxs-lookup"><span data-stu-id="b21dd-135">See **pbUserData**.</span></span>

<span data-ttu-id="b21dd-136">**szDependantColumns**</span><span class="sxs-lookup"><span data-stu-id="b21dd-136">**szDependantColumns**</span></span>

<span data-ttu-id="b21dd-137">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="b21dd-137">Reserved for future use.</span></span>

<span data-ttu-id="b21dd-138">Questo membro deve essere sempre impostato su NULL.</span><span class="sxs-lookup"><span data-stu-id="b21dd-138">This member should always be set to NULL.</span></span>

### <a name="requirements"></a><span data-ttu-id="b21dd-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b21dd-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b21dd-140"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b21dd-140"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b21dd-141">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b21dd-141">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b21dd-142"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b21dd-142"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b21dd-143">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b21dd-143">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b21dd-144"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b21dd-144"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b21dd-145">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b21dd-145">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b21dd-146"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b21dd-146"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b21dd-147">Implementato come <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) e <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b21dd-147">Implemented as <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) and <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b21dd-148">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b21dd-148">See Also</span></span>

[<span data-ttu-id="b21dd-149">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="b21dd-149">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="b21dd-150">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="b21dd-150">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="b21dd-151">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="b21dd-151">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)
