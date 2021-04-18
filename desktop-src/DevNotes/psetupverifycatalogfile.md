---
description: Verifica un singolo file di catalogo usando i criteri di firma del codice del sistema operativo standard, ad esempio la firma del driver.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: pSetupVerifyCatalogFile (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325200"
---
# <a name="psetupverifycatalogfile-function"></a><span data-ttu-id="3167a-103">pSetupVerifyCatalogFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="3167a-103">pSetupVerifyCatalogFile function</span></span>

<span data-ttu-id="3167a-104">\[Questa funzione non è più supportata da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3167a-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="3167a-105">Per un file INF (installazione del dispositivo), gli sviluppatori devono usare **SetupVerifyInfFile**.</span><span class="sxs-lookup"><span data-stu-id="3167a-105">For an INF file (device install), developers should use **SetupVerifyInfFile**.</span></span> <span data-ttu-id="3167a-106">Per convalidare un catalogo non basato su INF, usare **WinVerifyTrust**.\]</span><span class="sxs-lookup"><span data-stu-id="3167a-106">To validate a non-INF based catalog, use **WinVerifyTrust**.\]</span></span>

<span data-ttu-id="3167a-107">Verifica un singolo file di catalogo usando i criteri di firma del codice del sistema operativo standard, ad esempio la firma del driver.</span><span class="sxs-lookup"><span data-stu-id="3167a-107">Verifies a single catalog file using standard operating system code signing policy, such as driver signing.</span></span>

## <a name="syntax"></a><span data-ttu-id="3167a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3167a-108">Syntax</span></span>


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="3167a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3167a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3167a-110">*CatalogFullPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3167a-110">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3167a-111">Percorso completo del file di catalogo da verificare.</span><span class="sxs-lookup"><span data-stu-id="3167a-111">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3167a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3167a-112">Return value</span></span>

<span data-ttu-id="3167a-113">Se la funzione ha esito positivo, viene restituito l' **errore \_ esito positivo**; in caso contrario, viene restituito l'errore da [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="3167a-113">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

## <a name="remarks"></a><span data-ttu-id="3167a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3167a-114">Remarks</span></span>

<span data-ttu-id="3167a-115">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3167a-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3167a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3167a-116">Requirements</span></span>



| <span data-ttu-id="3167a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3167a-117">Requirement</span></span> | <span data-ttu-id="3167a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3167a-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3167a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3167a-119">DLL</span></span><br/> | <dl> <span data-ttu-id="3167a-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3167a-120"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3167a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3167a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3167a-122">**SetupVerifyInfFile**</span><span class="sxs-lookup"><span data-stu-id="3167a-122">**SetupVerifyInfFile**</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[<span data-ttu-id="3167a-123">**WinVerifyTrust**</span><span class="sxs-lookup"><span data-stu-id="3167a-123">**WinVerifyTrust**</span></span>](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
