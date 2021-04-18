---
description: Installa i componenti di sistema specificati.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327677"
---
# <a name="icfginstallinetcomponents-function"></a><span data-ttu-id="59705-103">IcfgInstallInetComponents (funzione)</span><span class="sxs-lookup"><span data-stu-id="59705-103">IcfgInstallInetComponents function</span></span>

<span data-ttu-id="59705-104">Installa i componenti di sistema specificati.</span><span class="sxs-lookup"><span data-stu-id="59705-104">Installs the system components specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="59705-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59705-105">Syntax</span></span>


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a><span data-ttu-id="59705-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59705-107">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="59705-107">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="59705-108">Handle per la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="59705-108">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="59705-109">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="59705-109">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="59705-110">Combinazione dei flag seguenti che controllano l'installazione e la configurazione.</span><span class="sxs-lookup"><span data-stu-id="59705-110">A combination of the following flags that control the installation and configuration.</span></span>



| <span data-ttu-id="59705-111">Valore</span><span class="sxs-lookup"><span data-stu-id="59705-111">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="59705-112">Significato</span><span class="sxs-lookup"><span data-stu-id="59705-112">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="59705-113"><dt>**ICFG \_**</dt> <dt>0x00000004</dt> INSTALLMAIL</span><span class="sxs-lookup"><span data-stu-id="59705-113"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="59705-114">Installare Exchange e Internet mail.</span><span class="sxs-lookup"><span data-stu-id="59705-114">Install Exchange and Internet mail.</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="59705-115"><dt>**ICFG \_**</dt> <dt>0x00000002</dt> INSTALLRAS</span><span class="sxs-lookup"><span data-stu-id="59705-115"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="59705-116">Installare RAS (se necessario).</span><span class="sxs-lookup"><span data-stu-id="59705-116">Install RAS (if needed).</span></span><br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="59705-117"><dt>**ICFG \_**</dt> <dt>0x00000001</dt> INSTALLTCP</span><span class="sxs-lookup"><span data-stu-id="59705-117"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="59705-118">Installare TCP/IP (se necessario).</span><span class="sxs-lookup"><span data-stu-id="59705-118">Install TCP/IP (if needed).</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="59705-119">*lpfNeedsRestart*</span><span class="sxs-lookup"><span data-stu-id="59705-119">*lpfNeedsRestart*</span></span> 
</dt> <dd>

<span data-ttu-id="59705-120">Se questo valore è diverso da **null**, in caso di restituzione sarà **true** solo se è necessario riavviare Windows per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="59705-120">If this value is non-**NULL**, on return it will be **TRUE** only if Windows must be restarted to complete the installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59705-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59705-121">Return value</span></span>

<span data-ttu-id="59705-122">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59705-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="59705-123">Se non si verificano errori, viene restituito il codice di **\_ esito positivo dell'errore** .</span><span class="sxs-lookup"><span data-stu-id="59705-123">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59705-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="59705-124">Remarks</span></span>

<span data-ttu-id="59705-125">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="59705-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="59705-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59705-126">Requirements</span></span>



| <span data-ttu-id="59705-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="59705-127">Requirement</span></span> | <span data-ttu-id="59705-128">Valore</span><span class="sxs-lookup"><span data-stu-id="59705-128">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59705-129">DLL</span><span class="sxs-lookup"><span data-stu-id="59705-129">DLL</span></span><br/> | <dl> <span data-ttu-id="59705-130"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59705-130"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
