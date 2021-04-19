---
description: Ricarica una configurazione IME dal registro di sistema HKCU, solo nell'IME giapponese.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: funzione reload_config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332655"
---
# <a name="reload_config-function"></a><span data-ttu-id="9d40e-103">ricarica \_ funzione di configurazione</span><span class="sxs-lookup"><span data-stu-id="9d40e-103">reload\_config function</span></span>

<span data-ttu-id="9d40e-104">Ricarica una configurazione IME dal registro di sistema HKCU, solo nell'IME giapponese.</span><span class="sxs-lookup"><span data-stu-id="9d40e-104">Reloads an IME configuration from the HKCU registry, in Japanese IME only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d40e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d40e-105">Syntax</span></span>


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a><span data-ttu-id="9d40e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d40e-106">Parameters</span></span>

<span data-ttu-id="9d40e-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="9d40e-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d40e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d40e-108">Return value</span></span>

<span data-ttu-id="9d40e-109">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="9d40e-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d40e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d40e-110">Remarks</span></span>

<span data-ttu-id="9d40e-111">Se non è presente alcun valore del registro di sistema in HKCU, la funzione di **ricaricamento della \_ configurazione** scrive i dati iniziali nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9d40e-111">If no registry value is present in HKCU, the **reload\_config** function writes initial data to the registry.</span></span>

<span data-ttu-id="9d40e-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9d40e-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d40e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d40e-113">Requirements</span></span>



| <span data-ttu-id="9d40e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d40e-114">Requirement</span></span> | <span data-ttu-id="9d40e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9d40e-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d40e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9d40e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="9d40e-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d40e-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span></span> </dl> |



 

 
