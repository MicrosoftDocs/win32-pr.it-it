---
title: Proprietà ConnectionOptions. password (WSManDisp. h)
description: Imposta la password di un account locale o di dominio nel computer remoto. Questa proprietà determina la password per l'autenticazione.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà password
- Gestione remota Windows proprietà password, oggetto ConnectionOptions
- Gestione remota Windows oggetto ConnectionOptions, proprietà password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120375"
---
# <a name="connectionoptionspassword-property"></a><span data-ttu-id="b9c64-107">Proprietà ConnectionOptions. password</span><span class="sxs-lookup"><span data-stu-id="b9c64-107">ConnectionOptions.Password property</span></span>

<span data-ttu-id="b9c64-108">Imposta la password di un account locale o di dominio nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b9c64-108">Sets the password of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="b9c64-109">Questa proprietà determina la password per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b9c64-109">This property determines the password for authentication.</span></span> <span data-ttu-id="b9c64-110">Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="b9c64-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="b9c64-111">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b9c64-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c64-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9c64-112">Syntax</span></span>


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a><span data-ttu-id="b9c64-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b9c64-113">Property value</span></span>

<span data-ttu-id="b9c64-114">Stringa che contiene la password di un account locale o di dominio nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b9c64-114">String that contains the password of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="b9c64-115">Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** non è impostato, verrà usata la password dell'account che esegue lo script.</span><span class="sxs-lookup"><span data-stu-id="b9c64-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the password of the account that is running the script is used.</span></span>

<span data-ttu-id="b9c64-116">Se non viene specificato alcun valore e viene impostato il flag **WSManFlagCredUsernamePassword** , lo script richiede all'utente di immettere la password (e il nome utente, se non viene fornito).</span><span class="sxs-lookup"><span data-stu-id="b9c64-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the password (and the user name, if this is not supplied).</span></span> <span data-ttu-id="b9c64-117">Se non viene immesso un nome utente e una password validi, viene restituito un errore di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="b9c64-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9c64-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9c64-118">Remarks</span></span>

<span data-ttu-id="b9c64-119">Tenere presente che non è possibile recuperare la password.</span><span class="sxs-lookup"><span data-stu-id="b9c64-119">Be aware that you cannot retrieve the password.</span></span> <span data-ttu-id="b9c64-120">La password può essere impostata solo con questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b9c64-120">The password can only be set with this property.</span></span>

<span data-ttu-id="b9c64-121">Se si crea un oggetto [**ConnectionOptions**](connectionoptions.md) e si usano un nome utente e una password per connettersi a gestione remota Windows, il flag **WSManFlagCredUserNamePassword** deve essere impostato sulla chiamata a [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="b9c64-121">If you create a [**ConnectionOptions**](connectionoptions.md) object and use a user name and password to connect to Windows Remote Management, then the **WSManFlagCredUserNamePassword** flag should be set on the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

<span data-ttu-id="b9c64-122">Per ulteriori informazioni sull'impostazione delle password, vedere la sezione Osservazioni in [**ConnectionOptions**](connectionoptions.md).</span><span class="sxs-lookup"><span data-stu-id="b9c64-122">For more information about setting passwords, see the Remarks section in [**ConnectionOptions**](connectionoptions.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9c64-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="b9c64-123">Examples</span></span>

<span data-ttu-id="b9c64-124">L'esempio di codice seguente crea un oggetto [**ConnectionOptions**](connectionoptions.md) e imposta la **password**.</span><span class="sxs-lookup"><span data-stu-id="b9c64-124">The following code example creates a [**ConnectionOptions**](connectionoptions.md) object and sets the **Password**.</span></span>


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a><span data-ttu-id="b9c64-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9c64-125">Requirements</span></span>



| <span data-ttu-id="b9c64-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c64-126">Requirement</span></span> | <span data-ttu-id="b9c64-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b9c64-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c64-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c64-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c64-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9c64-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b9c64-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c64-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c64-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9c64-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b9c64-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9c64-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9c64-133"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9c64-133"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9c64-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b9c64-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9c64-135"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9c64-135"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9c64-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9c64-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9c64-137"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b9c64-137"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b9c64-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b9c64-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9c64-139"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9c64-139"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9c64-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9c64-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c64-141">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="b9c64-141">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





