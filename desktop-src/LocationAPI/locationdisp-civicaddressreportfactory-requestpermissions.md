---
description: Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: LocationDisp. CivicAddressReportFactory. RequestPermissions, metodo
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
ms.openlocfilehash: 6d027687302c544974d13b1ba50194e8d6003a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349776"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a><span data-ttu-id="2f081-103">LocationDisp. CivicAddressReportFactory. RequestPermissions, metodo</span><span class="sxs-lookup"><span data-stu-id="2f081-103">LocationDisp.CivicAddressReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="2f081-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2f081-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f081-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="2f081-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2f081-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f081-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="2f081-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="2f081-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="2f081-108">Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.</span><span class="sxs-lookup"><span data-stu-id="2f081-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f081-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f081-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="2f081-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f081-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f081-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="2f081-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2f081-112">Questo parametro non viene utilizzato e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="2f081-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f081-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f081-113">Return value</span></span>

<span data-ttu-id="2f081-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2f081-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f081-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f081-115">Remarks</span></span>

<span data-ttu-id="2f081-116">La chiamata è sincrona e il chiamante attende la chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2f081-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="2f081-117">Se un'applicazione in esecuzione in modalità protetta, ad esempio un oggetto browser helper (BHO) per Internet Explorer, chiama **RequestPermissions** e l'utente sceglie l'opzione **non abilitare il sensore della posizione** nella finestra di dialogo, il provider di percorsi non verrà abilitato, ma Windows visualizzerà nuovamente la finestra di dialogo se **RequestPermissions** viene chiamato nuovamente dallo stesso utente.</span><span class="sxs-lookup"><span data-stu-id="2f081-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="2f081-118">Le applicazioni in esecuzione in modalità protetta possono scegliere di non chiamare [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) all'avvio in modo che l'utente non visualizzi una finestra di dialogo probabilmente indesiderata ogni volta che l'applicazione viene avviata.</span><span class="sxs-lookup"><span data-stu-id="2f081-118">Applications that run in protected mode may choose to not call [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2f081-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="2f081-119">Examples</span></span>

<span data-ttu-id="2f081-120">Per un esempio di come usare questo metodo, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="2f081-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f081-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f081-121">Requirements</span></span>



| <span data-ttu-id="2f081-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f081-122">Requirement</span></span> | <span data-ttu-id="2f081-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2f081-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="2f081-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f081-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2f081-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2f081-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2f081-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f081-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2f081-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2f081-127">None supported</span></span><br/>                  |



 

