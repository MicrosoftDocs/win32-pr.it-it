---
title: Metodo TaskService. Connect
description: Per lo scripting, si connette a un computer remoto e associa tutte le chiamate successive a questa interfaccia con una sessione remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Metodo Connect Utilità di pianificazione
- Metodo Connect Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963983"
---
# <a name="taskserviceconnect-method"></a><span data-ttu-id="7961f-106">Metodo TaskService. Connect</span><span class="sxs-lookup"><span data-stu-id="7961f-106">TaskService.Connect method</span></span>

<span data-ttu-id="7961f-107">Per lo scripting, si connette a un computer remoto e associa tutte le chiamate successive a questa interfaccia con una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7961f-107">For scripting, connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span> <span data-ttu-id="7961f-108">Se il parametro serverName è vuoto, questo metodo verrà eseguito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="7961f-108">If the serverName parameter is empty, then this method will execute on the local computer.</span></span> <span data-ttu-id="7961f-109">Se l'ID utente non è specificato, viene utilizzato il token corrente.</span><span class="sxs-lookup"><span data-stu-id="7961f-109">If the userId is not specified, then the current token is used.</span></span>

## <a name="syntax"></a><span data-ttu-id="7961f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7961f-110">Syntax</span></span>


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7961f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7961f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7961f-112">*nomeserver* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7961f-112">*serverName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7961f-113">Nome del computer a cui si desidera connettersi.</span><span class="sxs-lookup"><span data-stu-id="7961f-113">The name of the computer that you want to connect to.</span></span> <span data-ttu-id="7961f-114">Se il parametro serverName è vuoto, questo metodo verrà eseguito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="7961f-114">If the serverName parameter is empty, then this method will execute on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="7961f-115">*utente* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7961f-115">*user* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7961f-116">Nome utente utilizzato durante la connessione al computer.</span><span class="sxs-lookup"><span data-stu-id="7961f-116">The user name that is used during the connection to the computer.</span></span> <span data-ttu-id="7961f-117">Se l'utente non è specificato, viene utilizzato il token corrente.</span><span class="sxs-lookup"><span data-stu-id="7961f-117">If the user is not specified, then the current token is used.</span></span>

</dd> <dt>

<span data-ttu-id="7961f-118">*dominio* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7961f-118">*domain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7961f-119">Dominio dell'utente specificato nel parametro *User* .</span><span class="sxs-lookup"><span data-stu-id="7961f-119">The domain of the user specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7961f-120">*password* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7961f-120">*password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7961f-121">Password utilizzata per la connessione al computer.</span><span class="sxs-lookup"><span data-stu-id="7961f-121">The password that is used to connect to the computer.</span></span> <span data-ttu-id="7961f-122">Se il nome utente e la password non sono specificati, viene utilizzato il token corrente.</span><span class="sxs-lookup"><span data-stu-id="7961f-122">If the user name and password are not specified, then the current token is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7961f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7961f-123">Return value</span></span>

<span data-ttu-id="7961f-124">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7961f-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7961f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7961f-125">Remarks</span></span>

<span data-ttu-id="7961f-126">Prima di chiamare uno degli altri metodi [**TaskService**](taskservice.md) , è necessario chiamare il metodo **TaskService. Connect** .</span><span class="sxs-lookup"><span data-stu-id="7961f-126">The **TaskService.Connect** method should be called before calling any of the other [**TaskService**](taskservice.md) methods.</span></span>

<span data-ttu-id="7961f-127">Se il metodo Connect ha esito negativo, è possibile raccogliere l'identificatore di errore per trovare il significato dell'errore.</span><span class="sxs-lookup"><span data-stu-id="7961f-127">If the Connect method fails, you can collect the error identifier to find the meaning of the error.</span></span> <span data-ttu-id="7961f-128">Nella tabella seguente sono elencati gli identificatori di errore e le relative descrizioni.</span><span class="sxs-lookup"><span data-stu-id="7961f-128">The following table lists the error identifiers and their descriptions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7961f-129">Identificatore errore</span><span class="sxs-lookup"><span data-stu-id="7961f-129">Error Identifier</span></span></th>
<th><span data-ttu-id="7961f-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7961f-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7961f-131">0x80070005</span><span class="sxs-lookup"><span data-stu-id="7961f-131">0x80070005</span></span></td>
<td><span data-ttu-id="7961f-132">Accesso negato per la connessione al servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7961f-132">Access is denied to connect to the Task Scheduler service.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7961f-133">0x80041315</span><span class="sxs-lookup"><span data-stu-id="7961f-133">0x80041315</span></span></td>
<td><span data-ttu-id="7961f-134">Il servizio Utilità di pianificazione non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7961f-134">The Task Scheduler service is not running.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7961f-135">0x8007000e</span><span class="sxs-lookup"><span data-stu-id="7961f-135">0x8007000e</span></span></td>
<td><span data-ttu-id="7961f-136">L'applicazione non dispone di memoria sufficiente per completare l'operazione oppure l' <em>utente</em>, la <em>password</em>o il <em>dominio</em> ha almeno un valore null e un valore non null.</span><span class="sxs-lookup"><span data-stu-id="7961f-136">The application does not have enough memory to complete the operation or the <em>user</em>, <em>password</em>, or <em>domain</em> has at least one null and one non-null value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7961f-137">53</span><span class="sxs-lookup"><span data-stu-id="7961f-137">53</span></span></td>
<td><span data-ttu-id="7961f-138">Questo errore viene restituito nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7961f-138">This error is returned in the following situations:</span></span>
<ul>
<li><span data-ttu-id="7961f-139">Il nome computer specificato nel parametro <em>ServerName</em> non esiste.</span><span class="sxs-lookup"><span data-stu-id="7961f-139">The computer name specified in the <em>serverName</em> parameter does not exist.</span></span></li>
<li><span data-ttu-id="7961f-140">Quando si tenta di connettersi a un computer Windows Server 2003 o Windows XP e nel computer remoto non è abilitata l'eccezione del firewall condivisione file e stampanti oppure il servizio Registro di sistema remoto non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7961f-140">When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</span></span></li>
<li><span data-ttu-id="7961f-141">Quando si tenta di connettersi a un computer con Windows Vista e nel computer remoto non è abilitata l'eccezione del firewall Gestione attività pianificate remote e l'eccezione firewall condivisione file e stampanti è abilitata oppure il servizio Registro di sistema remoto non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7961f-141">When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7961f-142">50</span><span class="sxs-lookup"><span data-stu-id="7961f-142">50</span></span></td>
<td><span data-ttu-id="7961f-143">Impossibile specificare i parametri <em>User</em>, <em>password</em>o <em>Domain</em> quando ci si connette a un computer Windows XP o Windows Server 2003 remoto da un computer con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7961f-143">The <em>user</em>, <em>password</em>, or <em>domain</em> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7961f-144">Se ci si connette a un computer Windows Vista remoto da Windows Vista, è necessario consentire l'eccezione del firewall di gestione delle attività pianificate remote nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="7961f-144">If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer.</span></span> <span data-ttu-id="7961f-145">Per consentire questa eccezione, fare clic sul pulsante Start, pannello di controllo, sicurezza, consentire un programma tramite Windows Firewall, quindi selezionare la casella di controllo gestione remota attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="7961f-145">To allow this exception click Start, Control Panel, Security, Allow a program through Windows Firewall, and then select the Remote Scheduled Tasks Management check box.</span></span> <span data-ttu-id="7961f-146">Fare quindi clic sul pulsante OK nella finestra di dialogo Impostazioni Windows Firewall.</span><span class="sxs-lookup"><span data-stu-id="7961f-146">Then click the Ok button in the Windows Firewall Settings dialog box.</span></span>

<span data-ttu-id="7961f-147">Se ci si connette a un computer Windows XP o Windows Server 2003 remoto da un computer con Windows Vista, è necessario consentire l'eccezione del firewall per la condivisione di file e stampanti nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="7961f-147">If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer.</span></span> <span data-ttu-id="7961f-148">Per consentire questa eccezione, fare clic su Start, pannello di controllo, fare doppio clic su Windows Firewall, selezionare la scheda eccezioni, quindi selezionare l'eccezione firewall condivisione file e stampanti.</span><span class="sxs-lookup"><span data-stu-id="7961f-148">To allow this exception click Start, Control Panel, double-click Windows Firewall, select the Exceptions tab, and then select the File and Printer Sharing firewall exception.</span></span> <span data-ttu-id="7961f-149">Fare quindi clic sul pulsante OK nella finestra di dialogo Windows Firewall.</span><span class="sxs-lookup"><span data-stu-id="7961f-149">Then click the OK button in the Windows Firewall dialog box.</span></span> <span data-ttu-id="7961f-150">Anche il servizio Registro di sistema remoto deve essere in esecuzione nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="7961f-150">The Remote Registry service must also be running on the remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7961f-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7961f-151">Requirements</span></span>



| <span data-ttu-id="7961f-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="7961f-152">Requirement</span></span> | <span data-ttu-id="7961f-153">Valore</span><span class="sxs-lookup"><span data-stu-id="7961f-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7961f-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7961f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7961f-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7961f-155">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7961f-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7961f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7961f-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7961f-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7961f-158">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7961f-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="7961f-159"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7961f-159"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7961f-160">DLL</span><span class="sxs-lookup"><span data-stu-id="7961f-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7961f-161"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7961f-161"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





