---
title: Errore. Webhelp (metodo)
description: Il metodo WebHelp avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero). | Errore. Webhelp (metodo)
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- Metodo WebHelp Media Player Windows
- Metodo WebHelp Media Player Windows, classe Error
- Classe Error Media Player Windows, metodo Webhelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331587"
---
# <a name="errorwebhelp-method"></a><span data-ttu-id="8d061-107">Errore. Webhelp (metodo)</span><span class="sxs-lookup"><span data-stu-id="8d061-107">Error.webHelp method</span></span>

<span data-ttu-id="8d061-108">Il metodo **WebHelp** avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero).</span><span class="sxs-lookup"><span data-stu-id="8d061-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d061-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d061-109">Syntax</span></span>


```JScript
Error.webHelp()
```



## <a name="parameters"></a><span data-ttu-id="8d061-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d061-110">Parameters</span></span>

<span data-ttu-id="8d061-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8d061-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d061-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d061-112">Return value</span></span>

<span data-ttu-id="8d061-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8d061-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d061-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d061-114">Remarks</span></span>

<span data-ttu-id="8d061-115">Le pagine della Guida Web contengono sempre le informazioni più recenti e dettagliate sugli errori di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8d061-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="8d061-116">Questo metodo trasferisce automaticamente le altre informazioni richieste dalla guida Web, ad esempio la versione del sistema operativo in uso.</span><span class="sxs-lookup"><span data-stu-id="8d061-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="8d061-117">Per accedere direttamente alle pagine della Guida Web, usare i collegamenti seguenti per il codice di errore e il supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="8d061-117">To access the Web Help pages directly, use the following error code and support center links.</span></span>

-   [<span data-ttu-id="8d061-118">Informazioni sul codice di errore di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="8d061-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="8d061-119">Centro soluzioni Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="8d061-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

<span data-ttu-id="8d061-120">**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="8d061-120">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="examples"></a><span data-ttu-id="8d061-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="8d061-121">Examples</span></span>

<span data-ttu-id="8d061-122">Nell'esempio seguente viene creato un elemento BUTTON HTML che avvia la pagina della Guida Web di Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8d061-122">The following example creates an HTML BUTTON element that launches the Microsoft Windows Media Player Web Help page.</span></span> <span data-ttu-id="8d061-123">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8d061-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a><span data-ttu-id="8d061-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d061-124">Requirements</span></span>



| <span data-ttu-id="8d061-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d061-125">Requirement</span></span> | <span data-ttu-id="8d061-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8d061-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d061-127">Versione</span><span class="sxs-lookup"><span data-stu-id="8d061-127">Version</span></span><br/> | <span data-ttu-id="8d061-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="8d061-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8d061-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8d061-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d061-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d061-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d061-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d061-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d061-132">**Oggetto Error**</span><span class="sxs-lookup"><span data-stu-id="8d061-132">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





