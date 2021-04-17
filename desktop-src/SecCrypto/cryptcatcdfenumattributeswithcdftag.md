---
description: Enumera gli attributi dei file membro nella sezione CatalogFiles di un file di definizione del catalogo (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525729"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a><span data-ttu-id="42104-103">CryptCATCDFEnumAttributesWithCDFTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="42104-103">CryptCATCDFEnumAttributesWithCDFTag function</span></span>

<span data-ttu-id="42104-104">\[La funzione **CryptCATCDFEnumAttributesWithCDFTag** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="42104-104">\[The **CryptCATCDFEnumAttributesWithCDFTag** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="42104-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="42104-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="42104-106">La funzione **CryptCATCDFEnumAttributesWithCDFTag** enumera gli attributi dei file membro nella sezione **CatalogFiles** di un file di definizione del catalogo (CDF).</span><span class="sxs-lookup"><span data-stu-id="42104-106">The **CryptCATCDFEnumAttributesWithCDFTag** function enumerates the attributes of member files in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="42104-107">**CryptCATCDFEnumAttributesWithCDFTag** viene chiamato da [MakeCat](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="42104-107">**CryptCATCDFEnumAttributesWithCDFTag** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="42104-108">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="42104-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="42104-109">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="42104-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="42104-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42104-110">Syntax</span></span>


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a><span data-ttu-id="42104-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="42104-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42104-112">*pCDF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42104-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42104-113">Puntatore a una struttura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="42104-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="42104-114">*pwszMemberTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42104-114">*pwszMemberTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42104-115">Puntatore a una stringa con terminazione **null** che identifica il membro del file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="42104-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="42104-116">*pMember* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42104-116">*pMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42104-117">Puntatore a una struttura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) che contiene le informazioni sui membri.</span><span class="sxs-lookup"><span data-stu-id="42104-117">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information.</span></span>

</dd> <dt>

<span data-ttu-id="42104-118">*pPrevAttr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42104-118">*pPrevAttr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42104-119">Puntatore a una struttura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) per un attributo del membro del file nel file CDF a cui punta *pCDF*.</span><span class="sxs-lookup"><span data-stu-id="42104-119">A pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure for a file member attribute in the CDF pointed to by *pCDF*.</span></span>

</dd> <dt>

<span data-ttu-id="42104-120">*pfnParseError* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42104-120">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42104-121">Puntatore a una funzione definita dall'utente per gestire gli errori di analisi del file.</span><span class="sxs-lookup"><span data-stu-id="42104-121">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42104-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42104-122">Return value</span></span>

<span data-ttu-id="42104-123">Al termine dell'operazione, questa funzione restituisce un puntatore a una struttura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) .</span><span class="sxs-lookup"><span data-stu-id="42104-123">Upon success, this function returns a pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure.</span></span> <span data-ttu-id="42104-124">Se ha esito negativo, la funzione **CryptCATCDFEnumAttributesWithCDFTag** restituisce un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="42104-124">The **CryptCATCDFEnumAttributesWithCDFTag** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="42104-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="42104-125">Remarks</span></span>

<span data-ttu-id="42104-126">Questa funzione viene in genere chiamata in un ciclo per enumerare tutti gli attributi del membro del file di catalogo in un CDF.</span><span class="sxs-lookup"><span data-stu-id="42104-126">You typically call this function in a loop to enumerate all of the catalog file member attributes in a CDF.</span></span> <span data-ttu-id="42104-127">Prima di immettere il ciclo, impostare *pPrevAttr* su **null**.</span><span class="sxs-lookup"><span data-stu-id="42104-127">Before entering the loop, set *pPrevAttr* to **NULL**.</span></span> <span data-ttu-id="42104-128">La funzione restituisce un puntatore al primo attributo.</span><span class="sxs-lookup"><span data-stu-id="42104-128">The function returns a pointer to the first attribute.</span></span> <span data-ttu-id="42104-129">Impostare *pPrevAttr* sul valore restituito della funzione per le iterazioni successive del ciclo.</span><span class="sxs-lookup"><span data-stu-id="42104-129">Set *pPrevAttr* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="42104-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="42104-130">Examples</span></span>

<span data-ttu-id="42104-131">Nell'esempio seguente viene illustrata la sequenza di assegnazioni corretta per il parametro *pPrevAttr* ( `pAttr` ).</span><span class="sxs-lookup"><span data-stu-id="42104-131">The following example shows the correct sequence of assignments for the *pPrevAttr* parameter (`pAttr`).</span></span>


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="42104-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42104-132">Requirements</span></span>



| <span data-ttu-id="42104-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="42104-133">Requirement</span></span> | <span data-ttu-id="42104-134">Valore</span><span class="sxs-lookup"><span data-stu-id="42104-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42104-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42104-135">Minimum supported client</span></span><br/> | <span data-ttu-id="42104-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="42104-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="42104-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42104-137">Minimum supported server</span></span><br/> | <span data-ttu-id="42104-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42104-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42104-139">DLL</span><span class="sxs-lookup"><span data-stu-id="42104-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42104-140"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42104-140"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42104-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42104-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42104-142">MakeCat</span><span class="sxs-lookup"><span data-stu-id="42104-142">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="42104-143">**CRYPTCATATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="42104-143">**CRYPTCATATTRIBUTE**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[<span data-ttu-id="42104-144">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="42104-144">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="42104-145">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="42104-145">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="42104-146">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="42104-146">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="42104-147">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="42104-147">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
