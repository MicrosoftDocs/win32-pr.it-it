---
description: Libera i caricatori di classi Java che potrebbero essere stati usati durante l'esplorazione degli Apple.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327845"
---
# <a name="notifybrowsershutdown-function"></a><span data-ttu-id="db507-103">NotifyBrowserShutdown (funzione)</span><span class="sxs-lookup"><span data-stu-id="db507-103">NotifyBrowserShutdown function</span></span>

<span data-ttu-id="db507-104">Libera i caricatori di classi Java che potrebbero essere stati usati durante l'esplorazione degli Apple.</span><span class="sxs-lookup"><span data-stu-id="db507-104">Frees Java class loaders that may have been consumed while browsing the applets.</span></span>

## <a name="syntax"></a><span data-ttu-id="db507-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db507-105">Syntax</span></span>


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="db507-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db507-107">*lpvReserved*</span><span class="sxs-lookup"><span data-stu-id="db507-107">*lpvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="db507-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="db507-108">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db507-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db507-109">Return value</span></span>

<span data-ttu-id="db507-110">Se la funzione ha esito positivo, il valore restituito è **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db507-110">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="db507-111">In caso contrario, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="db507-111">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="db507-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="db507-112">Remarks</span></span>

<span data-ttu-id="db507-113">Quando il conteggio delle finestre del browser raggiunge lo zero in modalità Web integrata, questa funzione libera i caricatori di classi Java.</span><span class="sxs-lookup"><span data-stu-id="db507-113">When the count of browser windows reaches zero in integrated Web mode, this function frees the Java class loaders.</span></span> <span data-ttu-id="db507-114">Quando l'utente inizia a esplorare di nuovo gli Apple, la VM Java scaricherà i file di classe più recenti.</span><span class="sxs-lookup"><span data-stu-id="db507-114">When the user starts browsing applets again, the Java VM will download the latest class files.</span></span>

<span data-ttu-id="db507-115">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="db507-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="db507-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db507-116">Requirements</span></span>



| <span data-ttu-id="db507-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db507-117">Requirement</span></span> | <span data-ttu-id="db507-118">Valore</span><span class="sxs-lookup"><span data-stu-id="db507-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db507-119">DLL</span><span class="sxs-lookup"><span data-stu-id="db507-119">DLL</span></span><br/> | <dl> <span data-ttu-id="db507-120"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db507-120"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
