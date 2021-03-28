---
description: Abilita le pagine lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Metodo NewWDEvents. PassportAuthenticate (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760514"
---
# <a name="newwdeventspassportauthenticate-method"></a><span data-ttu-id="7b671-103">NewWDEvents. PassportAuthenticate, metodo</span><span class="sxs-lookup"><span data-stu-id="7b671-103">NewWDEvents.PassportAuthenticate method</span></span>

<span data-ttu-id="7b671-104">Abilita le pagine lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b671-104">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b671-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b671-105">Syntax</span></span>


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a><span data-ttu-id="7b671-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b671-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b671-107">*bstrSignInUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b671-107">*bstrSignInUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b671-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7b671-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7b671-109">Stringa contenente l'URL di una pagina Web che reindirizza all'interfaccia utente di accesso account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b671-109">A string containing the URL of a webpage that redirects to the Microsoft account log on UI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b671-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b671-110">Return value</span></span>

<span data-ttu-id="7b671-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7b671-111">Type: **Boolean**</span></span>

<span data-ttu-id="7b671-112">Impostare su **true** se l'autenticazione ha esito positivo; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="7b671-112">Set to **true** if authentication succeeds, **false** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b671-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b671-113">Remarks</span></span>

<span data-ttu-id="7b671-114">Questo metodo può essere chiamato anche se un utente è già connesso a un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b671-114">This method may be called even if a user is already logged on to a Microsoft account.</span></span> <span data-ttu-id="7b671-115">In tal caso, il metodo restituisce **true** senza visualizzare l'account Microsoft l'interfaccia utente di accesso.</span><span class="sxs-lookup"><span data-stu-id="7b671-115">In that case, the method returns **true** without displaying the Microsoft account log on UI.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b671-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b671-116">Requirements</span></span>



| <span data-ttu-id="7b671-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b671-117">Requirement</span></span> | <span data-ttu-id="7b671-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7b671-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b671-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b671-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b671-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7b671-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7b671-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b671-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b671-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b671-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7b671-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b671-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b671-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b671-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7b671-125">IDL</span><span class="sxs-lookup"><span data-stu-id="7b671-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b671-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b671-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7b671-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7b671-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b671-128"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7b671-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
