---
title: attributo system_handle
description: L'attributo \ system_handle \ specifica un tipo di handle definito dal sistema.
keywords:
- attributo system_handle MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320726"
---
# <a name="system_handle-attribute"></a><span data-ttu-id="ea8bf-104">attributo system_handle</span><span class="sxs-lookup"><span data-stu-id="ea8bf-104">system_handle attribute</span></span>

<span data-ttu-id="ea8bf-105">L' \[  \] attributo system_handle specifica un tipo di handle definito dal sistema che rappresenta l'accesso a un oggetto di sistema.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-105">The \[**system_handle**\] attribute specifies a system-defined handle type that represents access to a system object.</span></span>

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a><span data-ttu-id="ea8bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea8bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8bf-107">*tipo di handle di sistema*</span><span class="sxs-lookup"><span data-stu-id="ea8bf-107">*system-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8bf-108">Specifica una delle opzioni del tipo di handle di sistema.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-108">Specifies one of the system handle type options.</span></span>

<span data-ttu-id="ea8bf-109">Le opzioni valide sono:</span><span class="sxs-lookup"><span data-stu-id="ea8bf-109">The valid options are:</span></span>
* <span data-ttu-id="ea8bf-110">[sh_composition](sh-composition.md) un handle di superficie DirectComposition</span><span class="sxs-lookup"><span data-stu-id="ea8bf-110">[sh_composition](sh-composition.md) - A DirectComposition surface handle</span></span>
* <span data-ttu-id="ea8bf-111">[sh_event](sh-event.md) : oggetto evento denominato o senza nome</span><span class="sxs-lookup"><span data-stu-id="ea8bf-111">[sh_event](sh-event.md) - A named or unnamed event object</span></span>
* <span data-ttu-id="ea8bf-112">[sh_file](sh-file.md) : un file o un dispositivo I/O</span><span class="sxs-lookup"><span data-stu-id="ea8bf-112">[sh_file](sh-file.md) - A file or I/O device</span></span>
* <span data-ttu-id="ea8bf-113">[sh_job](sh-job.md) -un oggetto processo</span><span class="sxs-lookup"><span data-stu-id="ea8bf-113">[sh_job](sh-job.md) - A job object</span></span>
* <span data-ttu-id="ea8bf-114">[sh_mutex](sh-mutex.md) : oggetto mutex denominato o senza nome</span><span class="sxs-lookup"><span data-stu-id="ea8bf-114">[sh_mutex](sh-mutex.md) - A named or unnamed mutex object</span></span>
* <span data-ttu-id="ea8bf-115">[sh_pipe](sh-pipe.md) : oggetto anonimo o named pipe</span><span class="sxs-lookup"><span data-stu-id="ea8bf-115">[sh_pipe](sh-pipe.md) - An anonymous or named pipe object</span></span>
* <span data-ttu-id="ea8bf-116">[sh_process](sh-process.md) un oggetto processo</span><span class="sxs-lookup"><span data-stu-id="ea8bf-116">[sh_process](sh-process.md) - A process object</span></span>
* <span data-ttu-id="ea8bf-117">[sh_reg_key](sh-reg-key.md) -una chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ea8bf-117">[sh_reg_key](sh-reg-key.md) - A registry key</span></span>
* <span data-ttu-id="ea8bf-118">[sh_section](sh-section.md) -una sezione di memoria condivisa</span><span class="sxs-lookup"><span data-stu-id="ea8bf-118">[sh_section](sh-section.md) - A shared memory section</span></span>
* <span data-ttu-id="ea8bf-119">[sh_semaphore](sh-semaphore.md) : oggetto semaforo denominato o senza nome</span><span class="sxs-lookup"><span data-stu-id="ea8bf-119">[sh_semaphore](sh-semaphore.md) - A named or unnamed semaphore object</span></span>
* <span data-ttu-id="ea8bf-120">[sh_socket](sh-socket.md) : oggetto socket Winsock</span><span class="sxs-lookup"><span data-stu-id="ea8bf-120">[sh_socket](sh-socket.md) - A WinSock socket object</span></span>
* <span data-ttu-id="ea8bf-121">[sh_thread](sh-thread.md) -oggetto thread</span><span class="sxs-lookup"><span data-stu-id="ea8bf-121">[sh_thread](sh-thread.md) - A thread object</span></span>
* <span data-ttu-id="ea8bf-122">[sh_token](sh-token.md) -un oggetto token di accesso</span><span class="sxs-lookup"><span data-stu-id="ea8bf-122">[sh_token](sh-token.md) - An access token object</span></span>

</dd> <dt>

<span data-ttu-id="ea8bf-123">*facoltativo-accesso-maschera*</span><span class="sxs-lookup"><span data-stu-id="ea8bf-123">*optional-access-mask*</span></span>
</dt> <dd>

<span data-ttu-id="ea8bf-124">Facoltativamente, richiede diritti di accesso specifici applicati all'handle duplicato.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-124">Optionally requests specific access rights applied to the duplicated handle.</span></span> <span data-ttu-id="ea8bf-125">Per impostazione predefinita, quando non è specificato, l'handle verrà duplicato con lo stesso accesso.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-125">By default when this is unspecified, the handle will be duplicated with the same access.</span></span> 

<span data-ttu-id="ea8bf-126">Per specificare un livello di accesso diverso, usare i diritti di accesso specifici dell'oggetto corrispondenti all'oggetto di sistema sottostante selezionato.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-126">To specify a different level of access, use object specific access rights corresponding to the underlying system object selected.</span></span>

<span data-ttu-id="ea8bf-127">Altre informazioni su come vengono propagati i diritti di accesso durante la duplicazione sono disponibili nella documentazione di [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="ea8bf-127">More information on how access rights are propagated during duplication can be found on the [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) documentation.</span></span>

<span data-ttu-id="ea8bf-128">I collegamenti agli elenchi di diritti di accesso per ogni tipo di oggetto sono reperibili nel riferimento *DuplicateHandle* , oltre che nella pagina **vedere anche** intestazioni di ogni `sh_*` parametro.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-128">Links to lists of access rights for each type of object can be found in the *DuplicateHandle* reference as well as in the **See also** headings of each `sh_*` parameter page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea8bf-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea8bf-129">Remarks</span></span>

<span data-ttu-id="ea8bf-130">Per usare questo attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-130">In order to use this attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

<span data-ttu-id="ea8bf-131">Gli handle di sistema sono handle definiti dal sistema operativo per fornire l'accesso a una risorsa di sistema.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-131">System handles are handles that are defined by the operating system to provide access to a system resource.</span></span> <span data-ttu-id="ea8bf-132">Quando si dichiara l'attributo, è necessario specificare il tipo specifico dell'oggetto sottostante all'handle.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-132">The specific type of the object behind the handle must be specified when declaring the attribute.</span></span>

<span data-ttu-id="ea8bf-133">Per un handle contrassegnato `[in]` , l'handle verrà duplicato nella procedura remota e rimarrà valido per la durata di tale procedura.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-133">For a handle marked `[in]`, the handle will be duplicated into the remote procedure and remains valid for the duration of that procedure.</span></span> <span data-ttu-id="ea8bf-134">Al ritorno dalla procedura remota, l'handle duplicato viene liberato.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-134">On return from the remote procedure, the duplicated handle is freed.</span></span> <span data-ttu-id="ea8bf-135">Per mantenere l'accesso all'oggetto sottostante, l'applicazione remota deve duplicare l'handle nello spazio degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-135">To maintain access to the underlying object, the remote application must duplicate the handle into its own address space.</span></span>

<span data-ttu-id="ea8bf-136">Al contrario, per un handle contrassegnato `[out]` , quando una procedura remota restituisce un handle da una chiamata, la procedura remota ne perderà la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-136">By contrast, for a handle marked `[out]`, when a remote procedure returns a handle from a call, the remote procedure will lose ownership of it.</span></span> <span data-ttu-id="ea8bf-137">Per mantenere l'accesso all'oggetto sottostante, la procedura remota deve duplicare l'handle e restituire il duplicato.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-137">To maintain access to the underlying object, the remote procedure should duplicate the handle and return the duplicate.</span></span> <span data-ttu-id="ea8bf-138">L'handle restituito diventa quindi di proprietà del chiamante che presuppone che venga chiuso quando l'accesso all'oggetto di sistema sottostante non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-138">The returned handle then becomes owned by the caller who assumes a responsibility to close it when access to the underlying system object is no longer necessary.</span></span>

<span data-ttu-id="ea8bf-139">Poiché si tratta di un meccanismo per inoltrare l'accesso a un oggetto di sistema, questo attributo è applicabile solo alle chiamate tra routine nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-139">As this is a mechanism for relaying access to a system object, this attribute is only applicable to calls between procedures on the same machine.</span></span>

<span data-ttu-id="ea8bf-140">I parametri di creazione e di accesso forniti all'oggetto sottostante dietro l'handle di sistema durante la creazione stabiliranno se è possibile eseguire correttamente il marshalling nel contesto della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="ea8bf-140">The creation and access parameters given to the underlying object behind the system handle on its creation will dictate whether it can be successfully marshalled to the remote procedure context.</span></span>

<span data-ttu-id="ea8bf-141">Una matrice di `system_handle` può essere passata all'interno o all'esterno con la sintassi disponibile nella documentazione relativa all' [**attributo size_is**](size-is.md) .</span><span class="sxs-lookup"><span data-stu-id="ea8bf-141">An array of `system_handle` can be passed either in or out with the syntax found in the [**size_is attribute**](size-is.md) documentation.</span></span>

## <a name="examples"></a><span data-ttu-id="ea8bf-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea8bf-142">Examples</span></span>

<span data-ttu-id="ea8bf-143">Negli esempi seguenti vengono usati diversi usi di `system_handle` .</span><span class="sxs-lookup"><span data-stu-id="ea8bf-143">The following examples several uses of `system_handle`.</span></span> <span data-ttu-id="ea8bf-144">Per un esempio completo, vedere l'esempio [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .</span><span class="sxs-lookup"><span data-stu-id="ea8bf-144">For a complete sample, see the [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) sample.</span></span>

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a><span data-ttu-id="ea8bf-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea8bf-145">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="ea8bf-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea8bf-146">Minimum supported client</span></span> | <span data-ttu-id="ea8bf-147">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="ea8bf-147">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="ea8bf-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea8bf-148">Minimum supported server</span></span> | <span data-ttu-id="ea8bf-149">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="ea8bf-149">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ea8bf-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea8bf-150">See also</span></span>

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[<span data-ttu-id="ea8bf-151">opzione/target</span><span class="sxs-lookup"><span data-stu-id="ea8bf-151">/target switch</span></span>](./-target.md)
</dt> <dt>

[<span data-ttu-id="ea8bf-152">Binding e handle</span><span class="sxs-lookup"><span data-stu-id="ea8bf-152">Binding and Handles</span></span>](../Rpc/binding-and-handles.md)
</dt> <dt>

[<span data-ttu-id="ea8bf-153">Handle e oggetti</span><span class="sxs-lookup"><span data-stu-id="ea8bf-153">Handles and Objects</span></span>](../sysinfo/handles-and-objects.md)
</dt> <dt>

[<span data-ttu-id="ea8bf-154">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="ea8bf-154">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ea8bf-155">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="ea8bf-155">**DuplicateHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="ea8bf-156">Descrittori di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ea8bf-156">Security Descriptors</span></span>](../secauthz/security-descriptors.md)
</dt></dl>
