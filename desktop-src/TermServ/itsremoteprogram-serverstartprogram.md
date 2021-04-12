---
title: Metodo ITSRemoteProgram ServerStartProgram
description: Specifica un programma RemoteApp da avviare nella sessione remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ServerStartProgram
- Metodo ServerStartProgram Servizi Desktop remoto, interfaccia ITSRemoteProgram
- Interfaccia ITSRemoteProgram Servizi Desktop remoto, metodo ServerStartProgram
- Metodo ServerStartProgram Servizi Desktop remoto, interfaccia ITSRemoteProgram2
- Interfaccia ITSRemoteProgram2 Servizi Desktop remoto, metodo ServerStartProgram
- Metodo ServerStartProgram Servizi Desktop remoto, interfaccia ITSRemoteProgram3
- Interfaccia ITSRemoteProgram3 Servizi Desktop remoto, metodo ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518045"
---
# <a name="itsremoteprogramserverstartprogram-method"></a><span data-ttu-id="1abd0-110">Metodo ITSRemoteProgram:: ServerStartProgram</span><span class="sxs-lookup"><span data-stu-id="1abd0-110">ITSRemoteProgram::ServerStartProgram method</span></span>

<span data-ttu-id="1abd0-111">Specifica un programma RemoteApp da avviare nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="1abd0-111">Specifies a RemoteApp program to start in the remote session.</span></span> <span data-ttu-id="1abd0-112">Questa funzione deve essere richiamata in una sessione connessa (dopo che la notifica connessa alla sessione viene ricevuta dal client).</span><span class="sxs-lookup"><span data-stu-id="1abd0-112">This function must be invoked on a connected session (after the session connected notification is received at the client).</span></span> <span data-ttu-id="1abd0-113">Un numero qualsiasi di programmi RemoteApp può essere avviato in una sessione.</span><span class="sxs-lookup"><span data-stu-id="1abd0-113">Any number of RemoteApp programs can be started in a session.</span></span> <span data-ttu-id="1abd0-114">Si verifica il timeout di una sessione RemoteApp se nessun programma RemoteApp viene avviato nella sessione entro il limite di timeout, che è di due minuti per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1abd0-114">A RemoteApp session will time out if no RemoteApp program is started in the session within the time-out limit, which is two minutes for Windows Server 2008.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abd0-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1abd0-115">Syntax</span></span>


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="1abd0-116">Parametri</span><span class="sxs-lookup"><span data-stu-id="1abd0-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1abd0-117">*bstrExecutablePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1abd0-117">*bstrExecutablePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1abd0-118">Percorso del file eseguibile del programma RemoteApp nel server.</span><span class="sxs-lookup"><span data-stu-id="1abd0-118">The path of the RemoteApp program executable file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="1abd0-119">*bstrFilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1abd0-119">*bstrFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1abd0-120">Percorso di un file da aprire sul server tramite un'associazione di file, ad esempio "C: \\ \\ documents \\ \\MyReport.docx".</span><span class="sxs-lookup"><span data-stu-id="1abd0-120">The path of a file to open on the server through a file association, for example "C:\\\\Documents\\\\MyReport.docx".</span></span> <span data-ttu-id="1abd0-121">Se si specifica *bstrFilePath*, non è necessario specificare il parametro *bstrExecutablePath* e viceversa.</span><span class="sxs-lookup"><span data-stu-id="1abd0-121">If you specify *bstrFilePath*, you should not specify the *bstrExecutablePath* parameter, and vice versa.</span></span> <span data-ttu-id="1abd0-122">È necessario specificare solo uno dei parametri.</span><span class="sxs-lookup"><span data-stu-id="1abd0-122">You should only specify one of the parameters.</span></span>

</dd> <dt>

<span data-ttu-id="1abd0-123">*bstrWorkingDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1abd0-123">*bstrWorkingDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1abd0-124">Directory di lavoro sul server per il programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1abd0-124">The working directory on the server for the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="1abd0-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1abd0-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1abd0-126">Indica se il server deve espandere le variabili di ambiente nel percorso della directory di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1abd0-126">Indicates whether the server should expand environment variables in the working directory path.</span></span> <span data-ttu-id="1abd0-127">Impostare questo parametro su **Variant \_ true** se il percorso della directory di lavoro contiene le variabili di ambiente oppure **Variant \_ false** se il percorso della directory di lavoro non contiene variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="1abd0-127">Set this parameter to **VARIANT\_TRUE** if the working directory path contains environment variables, or **VARIANT\_FALSE** if the working directory path does not contain environment variables.</span></span>

</dd> <dt>

<span data-ttu-id="1abd0-128">*bstrArguments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1abd0-128">*bstrArguments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1abd0-129">Argomenti della riga di comando per il programma RemoteApp specificati in *bstrExecutablePath*.</span><span class="sxs-lookup"><span data-stu-id="1abd0-129">The command-line arguments for the RemoteApp program that are specified in *bstrExecutablePath*.</span></span> <span data-ttu-id="1abd0-130">Impostare su **null** se *bstrExecutablePath* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="1abd0-130">Set this to **NULL** if *bstrExecutablePath* is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="1abd0-131">*vbExpandEnvVarInArgumentsOnServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1abd0-131">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1abd0-132">Indica se il server deve espandere le variabili di ambiente negli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="1abd0-132">Indicates whether the server should expand environment variables in the command-line arguments.</span></span> <span data-ttu-id="1abd0-133">Impostare questo parametro su **Variant \_ true** se gli argomenti contengono variabili di ambiente o **Variant \_ false** se gli argomenti non contengono variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="1abd0-133">Set this parameter to **VARIANT\_TRUE** if the arguments contain environment variables, or **VARIANT\_FALSE** if the arguments do not contain environment variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1abd0-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1abd0-134">Return value</span></span>

<span data-ttu-id="1abd0-135">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1abd0-135">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="1abd0-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1abd0-136">Requirements</span></span>



| <span data-ttu-id="1abd0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1abd0-137">Requirement</span></span> | <span data-ttu-id="1abd0-138">Valore</span><span class="sxs-lookup"><span data-stu-id="1abd0-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1abd0-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1abd0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1abd0-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1abd0-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1abd0-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1abd0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1abd0-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1abd0-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1abd0-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1abd0-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="1abd0-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1abd0-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1abd0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1abd0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1abd0-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1abd0-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1abd0-147">IID</span><span class="sxs-lookup"><span data-stu-id="1abd0-147">IID</span></span><br/>                      | <span data-ttu-id="1abd0-148">IID \_ ITSRemoteProgram è definito come FDD029F9-467a-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="1abd0-148">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="1abd0-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1abd0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abd0-150">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="1abd0-150">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="1abd0-151">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="1abd0-151">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="1abd0-152">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="1abd0-152">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





