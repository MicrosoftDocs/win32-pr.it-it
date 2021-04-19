---
title: Metodo WebHelp IWMPError
description: Il metodo WebHelp avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero). | Metodo WebHelp IWMPError
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- Metodo WebHelp Media Player Windows
- Metodo WebHelp Media Player Windows, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player, metodo Webhelp
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332434"
---
# <a name="iwmperrorwebhelp-method"></a><span data-ttu-id="b41b9-107">Metodo IWMPError:: Webhelp</span><span class="sxs-lookup"><span data-stu-id="b41b9-107">IWMPError::webHelp method</span></span>

<span data-ttu-id="b41b9-108">Il metodo **WebHelp** avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero).</span><span class="sxs-lookup"><span data-stu-id="b41b9-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="b41b9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b41b9-109">Syntax</span></span>


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a><span data-ttu-id="b41b9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b41b9-110">Parameters</span></span>

<span data-ttu-id="b41b9-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b41b9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b41b9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b41b9-112">Return value</span></span>

<span data-ttu-id="b41b9-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b41b9-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b41b9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b41b9-114">Remarks</span></span>

<span data-ttu-id="b41b9-115">Le pagine della Guida Web contengono sempre le informazioni più recenti e dettagliate sugli errori di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b41b9-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="b41b9-116">Questo metodo trasferisce automaticamente le altre informazioni richieste dalla guida Web, ad esempio la versione del sistema operativo in uso.</span><span class="sxs-lookup"><span data-stu-id="b41b9-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="b41b9-117">Per accedere direttamente alle pagine della Guida Web, usare il codice di errore e i collegamenti di Support Center seguenti:</span><span class="sxs-lookup"><span data-stu-id="b41b9-117">To access the Web Help pages directly, use the following error code and support center links:</span></span>

-   [<span data-ttu-id="b41b9-118">Informazioni sul codice di errore di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="b41b9-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="b41b9-119">Centro soluzioni Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="b41b9-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a><span data-ttu-id="b41b9-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b41b9-120">Examples</span></span>

<span data-ttu-id="b41b9-121">Nell'esempio seguente viene creato un pulsante che avvia la pagina della Guida Web di Microsoft Windows Media Player nel browser.</span><span class="sxs-lookup"><span data-stu-id="b41b9-121">The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser.</span></span> <span data-ttu-id="b41b9-122">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="b41b9-122">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b41b9-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b41b9-123">Requirements</span></span>



| <span data-ttu-id="b41b9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b41b9-124">Requirement</span></span> | <span data-ttu-id="b41b9-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b41b9-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b9-126">Versione</span><span class="sxs-lookup"><span data-stu-id="b41b9-126">Version</span></span><br/>   | <span data-ttu-id="b41b9-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b41b9-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b41b9-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b41b9-128">Namespace</span></span><br/> | <span data-ttu-id="b41b9-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b41b9-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b41b9-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="b41b9-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b41b9-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b41b9-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b41b9-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b41b9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41b9-133">**Interfaccia IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b41b9-133">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





