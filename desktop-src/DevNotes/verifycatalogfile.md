---
description: Verifica un singolo file di catalogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324435"
---
# <a name="verifycatalogfile-function"></a><span data-ttu-id="a9ddc-103">VerifyCatalogFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="a9ddc-103">VerifyCatalogFile function</span></span>

<span data-ttu-id="a9ddc-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="a9ddc-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="a9ddc-105">Verifica un singolo file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="a9ddc-105">Verifies a single catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ddc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9ddc-106">Syntax</span></span>


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="a9ddc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9ddc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ddc-108">*CatalogFullPath*</span><span class="sxs-lookup"><span data-stu-id="a9ddc-108">*CatalogFullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ddc-109">Percorso completo del file di catalogo da verificare.</span><span class="sxs-lookup"><span data-stu-id="a9ddc-109">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ddc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9ddc-110">Return value</span></span>

<span data-ttu-id="a9ddc-111">Se la funzione ha esito positivo, viene restituito l' **errore \_ esito positivo**; in caso contrario, viene restituito l'errore da [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="a9ddc-111">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

<span data-ttu-id="a9ddc-112">Se il catalogo è un catalogo con firma Authenticode, questa funzione restituisce l' **errore di \_ \_ \_ autore attendibile Authenticode** se ha esito positivo; in caso contrario, restituisce l' **errore di \_ \_ attendibilità Authenticode \_ non \_ stabilito**.</span><span class="sxs-lookup"><span data-stu-id="a9ddc-112">If the catalog is an Authenticode-signed catalog, this function returns **ERROR\_AUTHENTICODE\_TRUSTED\_PUBLISHER** if it succeeds; otherwise, it returns **ERROR\_AUTHENTICODE\_TRUST\_NOT\_ESTABLISHED**.</span></span>

<span data-ttu-id="a9ddc-113">Se la funzione non è in grado di determinare se il server di pubblicazione è attendibile, potrebbe inoltre restituire un errore non **\_ identificato \_**.</span><span class="sxs-lookup"><span data-stu-id="a9ddc-113">If the function is unable to determine whether the publisher is trusted, it may also return **ERROR\_UNIDENTIFIED\_ERROR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9ddc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9ddc-114">Remarks</span></span>

<span data-ttu-id="a9ddc-115">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a9ddc-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ddc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9ddc-116">Requirements</span></span>



| <span data-ttu-id="a9ddc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ddc-117">Requirement</span></span> | <span data-ttu-id="a9ddc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ddc-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ddc-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a9ddc-119">DLL</span></span><br/> | <dl> <span data-ttu-id="a9ddc-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9ddc-120"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
