---
description: Enumera i singoli membri di file nella sezione CatalogFiles di un file di definizione del catalogo (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525734"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a><span data-ttu-id="a0615-103">CryptCATCDFEnumMembersByCDFTagEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="a0615-103">CryptCATCDFEnumMembersByCDFTagEx function</span></span>

<span data-ttu-id="a0615-104">\[La funzione **CryptCATCDFEnumMembersByCDFTagEx** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a0615-104">\[The **CryptCATCDFEnumMembersByCDFTagEx** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a0615-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="a0615-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="a0615-106">La funzione **CryptCATCDFEnumMembersByCDFTagEx** enumera i singoli membri di file nella sezione **CatalogFiles** di un file di definizione del catalogo (CDF).</span><span class="sxs-lookup"><span data-stu-id="a0615-106">The **CryptCATCDFEnumMembersByCDFTagEx** function enumerates the individual file members in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="a0615-107">**CryptCATCDFEnumMembersByCDFTagEx** viene chiamato da [MakeCat](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="a0615-107">**CryptCATCDFEnumMembersByCDFTagEx** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0615-108">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="a0615-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="a0615-109">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="a0615-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a0615-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0615-110">Syntax</span></span>


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="a0615-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0615-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0615-112">*pCDF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0615-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0615-113">Puntatore a una struttura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="a0615-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0615-114">*pwszPrevCDFTag* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a0615-114">*pwszPrevCDFTag* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0615-115">Puntatore a una stringa con terminazione **null** che identifica il membro del file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="a0615-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="a0615-116">*pfnParseError* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0615-116">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0615-117">Puntatore a una funzione definita dall'utente per gestire gli errori di analisi del file.</span><span class="sxs-lookup"><span data-stu-id="a0615-117">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> <dt>

<span data-ttu-id="a0615-118">*ppMember* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0615-118">*ppMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0615-119">Puntatore a una struttura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) che contiene le informazioni sui membri del file.</span><span class="sxs-lookup"><span data-stu-id="a0615-119">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the file member information.</span></span>

</dd> <dt>

<span data-ttu-id="a0615-120">*fContinueOnError* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0615-120">*fContinueOnError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0615-121">Valore che specifica se rimanere in memoria un riferimento all'ultimo membro enumerato.</span><span class="sxs-lookup"><span data-stu-id="a0615-121">A value that specifies whether to keep in memory a reference to the last enumerated member.</span></span>

</dd> <dt>

<span data-ttu-id="a0615-122">*pvReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0615-122">*pvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0615-123">Questo parametro è riservato; non usarlo.</span><span class="sxs-lookup"><span data-stu-id="a0615-123">This parameter is reserved; do not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0615-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0615-124">Return value</span></span>

<span data-ttu-id="a0615-125">Al termine dell'operazione, questa funzione restituisce un puntatore a una stringa con terminazione **null** che identifica un membro del file nella sezione **CATALOGFILES** di un CDF.</span><span class="sxs-lookup"><span data-stu-id="a0615-125">Upon success, this function returns a pointer to a **null**-terminated string that identifies a file member in the **CatalogFiles** section of a CDF.</span></span> <span data-ttu-id="a0615-126">Se ha esito negativo, la funzione **CryptCATCDFEnumMembersByCDFTagEx** restituisce un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="a0615-126">The **CryptCATCDFEnumMembersByCDFTagEx** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0615-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0615-127">Remarks</span></span>

<span data-ttu-id="a0615-128">Questa funzione viene in genere chiamata in un ciclo per enumerare tutti i membri del file di catalogo in un CDF.</span><span class="sxs-lookup"><span data-stu-id="a0615-128">You typically call this function in a loop to enumerate all of the catalog file members in a CDF.</span></span> <span data-ttu-id="a0615-129">Prima di immettere il ciclo, impostare *pwszPrevCDFTag* su **null**.</span><span class="sxs-lookup"><span data-stu-id="a0615-129">Before entering the loop, set *pwszPrevCDFTag* to **NULL**.</span></span> <span data-ttu-id="a0615-130">La funzione restituisce un puntatore al primo membro.</span><span class="sxs-lookup"><span data-stu-id="a0615-130">The function returns a pointer to the first member.</span></span> <span data-ttu-id="a0615-131">Impostare *pwszPrevCDFTag* sul valore restituito della funzione per le iterazioni successive del ciclo.</span><span class="sxs-lookup"><span data-stu-id="a0615-131">Set *pwszPrevCDFTag* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="a0615-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="a0615-132">Examples</span></span>

<span data-ttu-id="a0615-133">Nell'esempio seguente viene illustrata la sequenza di assegnazioni corretta per il parametro *pwszPrevCDFTag* ( `pwszMemberTag` ).</span><span class="sxs-lookup"><span data-stu-id="a0615-133">The following example shows the correct sequence of assignments for the *pwszPrevCDFTag* parameter (`pwszMemberTag`).</span></span>


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="a0615-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0615-134">Requirements</span></span>



| <span data-ttu-id="a0615-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0615-135">Requirement</span></span> | <span data-ttu-id="a0615-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a0615-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0615-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0615-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a0615-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0615-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0615-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0615-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a0615-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0615-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0615-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a0615-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0615-142"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0615-142"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0615-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0615-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0615-144">MakeCat</span><span class="sxs-lookup"><span data-stu-id="a0615-144">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="a0615-145">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="a0615-145">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="a0615-146">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="a0615-146">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="a0615-147">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="a0615-147">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="a0615-148">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="a0615-148">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
