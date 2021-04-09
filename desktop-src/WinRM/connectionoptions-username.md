---
title: Proprietà ConnectionOptions. UserName (WSManDisp. h)
description: Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto. Questa proprietà determina il nome utente per l'autenticazione.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Gestione remota Windows
- Gestione remota Windows proprietà nomeutente, oggetto ConnectionOptions
- Oggetto ConnectionOptions Gestione remota Windows, proprietà UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120374"
---
# <a name="connectionoptionsusername-property"></a><span data-ttu-id="710fb-107">Proprietà ConnectionOptions. UserName</span><span class="sxs-lookup"><span data-stu-id="710fb-107">ConnectionOptions.UserName property</span></span>

<span data-ttu-id="710fb-108">Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="710fb-108">Sets and gets the user name of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="710fb-109">Questa proprietà determina il nome utente per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="710fb-109">This property determines the user name for authentication.</span></span> <span data-ttu-id="710fb-110">Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="710fb-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="710fb-111">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="710fb-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="710fb-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="710fb-112">Syntax</span></span>


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a><span data-ttu-id="710fb-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="710fb-113">Property value</span></span>

<span data-ttu-id="710fb-114">Stringa che contiene il nome utente di un account locale o di dominio nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="710fb-114">String that contains the user name of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="710fb-115">Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** non è impostato, viene usato il nome utente dell'account che esegue lo script.</span><span class="sxs-lookup"><span data-stu-id="710fb-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the user name of the account that is running the script is used.</span></span>

<span data-ttu-id="710fb-116">Se non viene specificato alcun valore e viene impostato il flag **WSManFlagCredUsernamePassword** , lo script richiede all'utente di immettere il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="710fb-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the user name and password.</span></span> <span data-ttu-id="710fb-117">Se non viene immesso un nome utente e una password validi, viene restituito un errore di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="710fb-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="710fb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="710fb-118">Remarks</span></span>

<span data-ttu-id="710fb-119">Per specificare questa proprietà, viene usata la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="710fb-119">The following syntax is used to specify this property.</span></span>


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



<span data-ttu-id="710fb-120">È possibile specificare **nome utente** e [**password**](connectionoptions-password.md) per un account di dominio quando si usa l'autenticazione [*Negotiate*](windows-remote-management-glossary.md) o *Kerberos* o per un account locale con autenticazione di [*base*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="710fb-120">You can supply **UserName** and [**Password**](connectionoptions-password.md) for a domain account when using [*negotiate*](windows-remote-management-glossary.md) or *Kerberos* authentication, or for a local account with [*Basic*](windows-remote-management-glossary.md) authentication.</span></span> <span data-ttu-id="710fb-121">Per connettersi a un account locale, i flag [**WSMan. CreateSession**](wsman-createsession.md) devono contenere la combinazione del flag **WSManFlagUseBasic** e del flag **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="710fb-121">To connect to a local account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseBasic** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="710fb-122">Per connettersi a un account di dominio, i flag **WSMan. CreateSession** devono contenere la combinazione del flag **WSManFlagUseNegotiate** e del flag **WsmanFlagCredUserNamePassword** oppure la combinazione del flag **WSManFlagUseKerberos** e del flag **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="710fb-122">To connect to a domain account, the **WSMan.CreateSession** flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag, or the combination of the **WSManFlagUseKerberos** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="710fb-123">Per un account di dominio, il nome **utente** deve essere specificato nel formato "computer \\ nomeutente", dove la parte "computer" della stringa può essere il nome o l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="710fb-123">For a domain account, **UserName** must be specified in the form "computer\\username", where the "computer" part of the string can be either the name or the IP address.</span></span> <span data-ttu-id="710fb-124">Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="710fb-124">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



<span data-ttu-id="710fb-125">Per la connessione a un account di dominio, i flag [**WSMan. CreateSession**](wsman-createsession.md) devono contenere la combinazione del flag **WSManFlagUseNegotiate** e il flag **WsmanFlagCredUserNamePassword** per la connessione a un account di dominio, che richiede l'autenticazione Negotiate.</span><span class="sxs-lookup"><span data-stu-id="710fb-125">For connecting to a domain account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag for connecting to a domain account, which requires Negotiate authentication.</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a><span data-ttu-id="710fb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="710fb-126">Requirements</span></span>



| <span data-ttu-id="710fb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="710fb-127">Requirement</span></span> | <span data-ttu-id="710fb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="710fb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="710fb-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710fb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="710fb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="710fb-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="710fb-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710fb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="710fb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="710fb-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="710fb-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="710fb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="710fb-134"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="710fb-134"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="710fb-135">IDL</span><span class="sxs-lookup"><span data-stu-id="710fb-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="710fb-136"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="710fb-136"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="710fb-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="710fb-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="710fb-138"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="710fb-138"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="710fb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="710fb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="710fb-140"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="710fb-140"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="710fb-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="710fb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710fb-142">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="710fb-142">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





