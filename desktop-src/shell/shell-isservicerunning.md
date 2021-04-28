---
description: 'Metodo Shell.IsServiceRunning: restituisce un valore che indica se un determinato servizio è in esecuzione.'
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Metodo Shell.IsServiceRunning (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 01af900bb7930ec7b6dde0b0700c83f211733dc3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083719"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="8ea08-103">Metodo Shell.IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="8ea08-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="8ea08-104">Restituisce un valore che indica se un determinato servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8ea08-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea08-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ea08-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="8ea08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ea08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea08-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8ea08-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea08-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="8ea08-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="8ea08-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="8ea08-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea08-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ea08-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8ea08-111">JScript</span><span class="sxs-lookup"><span data-stu-id="8ea08-111">JScript</span></span>

<span data-ttu-id="8ea08-112">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="8ea08-112">Type: **Variant\***</span></span>

<span data-ttu-id="8ea08-113">Restituisce **true** se il servizio specificato da *sServiceName è* in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8ea08-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="8ea08-114">VB</span><span class="sxs-lookup"><span data-stu-id="8ea08-114">VB</span></span>

<span data-ttu-id="8ea08-115">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="8ea08-115">Type: **Variant\***</span></span>

<span data-ttu-id="8ea08-116">Restituisce **true** se il servizio specificato da *sServiceName è* in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8ea08-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea08-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ea08-117">Remarks</span></span>

<span data-ttu-id="8ea08-118">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8ea08-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="8ea08-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="8ea08-119">Examples</span></span>

<span data-ttu-id="8ea08-120">Gli esempi seguenti illustrano l'uso di **IsServiceRunning** per determinare se il servizio Temi è in esecuzione per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8ea08-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="8ea08-121">L'utilizzo è illustrato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="8ea08-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="8ea08-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="8ea08-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="8ea08-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="8ea08-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="8ea08-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ea08-124">Requirements</span></span>



| <span data-ttu-id="8ea08-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea08-125">Requirement</span></span> | <span data-ttu-id="8ea08-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8ea08-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea08-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ea08-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea08-128">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8ea08-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ea08-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ea08-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea08-130">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ea08-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8ea08-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ea08-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ea08-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ea08-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8ea08-133">Idl</span><span class="sxs-lookup"><span data-stu-id="8ea08-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ea08-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ea08-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8ea08-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea08-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ea08-136"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea08-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
