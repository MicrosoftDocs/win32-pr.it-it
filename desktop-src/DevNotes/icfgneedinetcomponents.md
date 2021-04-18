---
description: Determina se i componenti contrassegnati nelle opzioni sono installati nel sistema.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330966"
---
# <a name="icfgneedinetcomponents-function"></a><span data-ttu-id="04fdb-103">IcfgNeedInetComponents (funzione)</span><span class="sxs-lookup"><span data-stu-id="04fdb-103">IcfgNeedInetComponents function</span></span>

<span data-ttu-id="04fdb-104">Determina se i componenti contrassegnati nelle opzioni sono installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="04fdb-104">Determines whether components marked in the options are installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="04fdb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04fdb-105">Syntax</span></span>


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a><span data-ttu-id="04fdb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04fdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04fdb-107">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="04fdb-107">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="04fdb-108">Combinazione dei flag seguenti che specificano i componenti da rilevare dall'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="04fdb-108">A combination of the following flags that specify which components to detect from the following list.</span></span>



| <span data-ttu-id="04fdb-109">Valore</span><span class="sxs-lookup"><span data-stu-id="04fdb-109">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="04fdb-110">Significato</span><span class="sxs-lookup"><span data-stu-id="04fdb-110">Meaning</span></span>                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="04fdb-111"><dt>**ICFG \_**</dt> <dt>0x00000004</dt> INSTALLMAIL</span><span class="sxs-lookup"><span data-stu-id="04fdb-111"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="04fdb-112">Exchange o Internet mail è necessario?</span><span class="sxs-lookup"><span data-stu-id="04fdb-112">Is Exchange or Internet mail needed?</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="04fdb-113"><dt>**ICFG \_**</dt> <dt>0x00000002</dt> INSTALLRAS</span><span class="sxs-lookup"><span data-stu-id="04fdb-113"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="04fdb-114">RAS è necessario?</span><span class="sxs-lookup"><span data-stu-id="04fdb-114">Is RAS needed?</span></span><br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="04fdb-115"><dt>**ICFG \_**</dt> <dt>0x00000001</dt> INSTALLTCP</span><span class="sxs-lookup"><span data-stu-id="04fdb-115"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="04fdb-116">TCP/IP è necessario?</span><span class="sxs-lookup"><span data-stu-id="04fdb-116">Is TCP/IP needed?</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="04fdb-117">*lpfNeedComponents*</span><span class="sxs-lookup"><span data-stu-id="04fdb-117">*lpfNeedComponents*</span></span> 
</dt> <dd>

<span data-ttu-id="04fdb-118">Se questo valore è diverso da **null**, viene restituito **true** se uno o più componenti non sono installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="04fdb-118">If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04fdb-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04fdb-119">Return value</span></span>

<span data-ttu-id="04fdb-120">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04fdb-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="04fdb-121">Se non si verificano errori, viene restituito il codice di **\_ esito positivo dell'errore** .</span><span class="sxs-lookup"><span data-stu-id="04fdb-121">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04fdb-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="04fdb-122">Remarks</span></span>

<span data-ttu-id="04fdb-123">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="04fdb-123">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="04fdb-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04fdb-124">Requirements</span></span>



| <span data-ttu-id="04fdb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="04fdb-125">Requirement</span></span> | <span data-ttu-id="04fdb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="04fdb-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04fdb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="04fdb-127">DLL</span></span><br/> | <dl> <span data-ttu-id="04fdb-128"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04fdb-128"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
