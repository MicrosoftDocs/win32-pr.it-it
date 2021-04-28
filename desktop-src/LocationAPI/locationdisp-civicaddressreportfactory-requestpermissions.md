---
description: "Metodo LocationDisp.CivicAddressReportFactory.RequestPermissions: apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione."
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: Metodo LocationDisp.CivicAddressReportFactory.RequestPermissions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: cab163585fa23839eb894f7ad83f29ed7975e589
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110909"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a><span data-ttu-id="a79f6-103">Metodo LocationDisp.CivicAddressReportFactory.RequestPermissions</span><span class="sxs-lookup"><span data-stu-id="a79f6-103">LocationDisp.CivicAddressReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="a79f6-104">\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.</span><span class="sxs-lookup"><span data-stu-id="a79f6-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a79f6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a79f6-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a79f6-106">Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a79f6-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a79f6-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]</span><span class="sxs-lookup"><span data-stu-id="a79f6-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a79f6-108">Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.</span><span class="sxs-lookup"><span data-stu-id="a79f6-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a79f6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a79f6-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="a79f6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a79f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a79f6-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="a79f6-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a79f6-112">Questo parametro non viene usato e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a79f6-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a79f6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a79f6-113">Return value</span></span>

<span data-ttu-id="a79f6-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a79f6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a79f6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a79f6-115">Remarks</span></span>

<span data-ttu-id="a79f6-116">La chiamata è sincrona e il chiamante attende la chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a79f6-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="a79f6-117">Se un'applicazione in esecuzione in modalità protetta, ad esempio un oggetto browser helper (BHO) per Internet Explorer, chiama **RequestPermissions** e **l'utente sceglie l'opzione** Non abilitare questo sensore di posizione nella finestra di dialogo, il provider di percorso non verrà abilitato, ma Windows visualizza di nuovo la finestra di dialogo se **RequestPermissions** viene chiamato di nuovo dallo stesso utente.</span><span class="sxs-lookup"><span data-stu-id="a79f6-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="a79f6-118">Le applicazioni in esecuzione in modalità protetta possono scegliere di non chiamare [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) all'avvio in modo che l'utente non veda una finestra di dialogo potenzialmente indesiderata ogni volta che l'applicazione viene avviata.</span><span class="sxs-lookup"><span data-stu-id="a79f6-118">Applications that run in protected mode may choose to not call [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a79f6-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="a79f6-119">Examples</span></span>

<span data-ttu-id="a79f6-120">Per un esempio di come usare questo metodo, vedere [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="a79f6-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="a79f6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a79f6-121">Requirements</span></span>



| <span data-ttu-id="a79f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a79f6-122">Requirement</span></span> | <span data-ttu-id="a79f6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a79f6-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a79f6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a79f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a79f6-125">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a79f6-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a79f6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a79f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a79f6-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a79f6-127">None supported</span></span><br/>                  |



 

