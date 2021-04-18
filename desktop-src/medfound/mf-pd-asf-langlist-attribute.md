---
description: Specifica un elenco di identificatori di lingua che specifica le lingue contenute in un file ASF (Advanced Systems Format). Questo attributo corrisponde all'oggetto elenco lingue, definito nella specifica ASF.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: Attributo MF_PD_ASF_LANGLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecac5eac178c7fb315e0ca4cfdbd540a27eeac28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315018"
---
# <a name="mf_pd_asf_langlist-attribute"></a><span data-ttu-id="4d490-104">Attributo della lingua MF \_ PD \_ ASF \_</span><span class="sxs-lookup"><span data-stu-id="4d490-104">MF\_PD\_ASF\_LANGLIST attribute</span></span>

<span data-ttu-id="4d490-105">Specifica un elenco di identificatori di lingua che specifica le lingue contenute in un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="4d490-105">Specifies a list of language identifiers which specifies the languages contained in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="4d490-106">Questo attributo corrisponde all'oggetto elenco lingue, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="4d490-106">This attribute corresponds to the Language List Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="4d490-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4d490-107">Data type</span></span>

<span data-ttu-id="4d490-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="4d490-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="4d490-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d490-109">Remarks</span></span>

<span data-ttu-id="4d490-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="4d490-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="4d490-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'intestazione dell'oggetto List della lingua.</span><span class="sxs-lookup"><span data-stu-id="4d490-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Language List Object header.</span></span> <span data-ttu-id="4d490-112">La tabella seguente illustra il formato del BLOB:</span><span class="sxs-lookup"><span data-stu-id="4d490-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="4d490-113">Campo oggetto elenco lingue</span><span class="sxs-lookup"><span data-stu-id="4d490-113">Language List Object field</span></span> | <span data-ttu-id="4d490-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4d490-114">Data type</span></span>    | <span data-ttu-id="4d490-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4d490-115">Size</span></span>    | <span data-ttu-id="4d490-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d490-116">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="4d490-117">Conteggio record ID lingua</span><span class="sxs-lookup"><span data-stu-id="4d490-117">Language ID Records Count</span></span>  | <span data-ttu-id="4d490-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4d490-118">**DWORD**</span></span>    | <span data-ttu-id="4d490-119">4 byte</span><span class="sxs-lookup"><span data-stu-id="4d490-119">4 bytes</span></span> | <span data-ttu-id="4d490-120">Numero di lingue</span><span class="sxs-lookup"><span data-stu-id="4d490-120">Number of languages</span></span>                    |
| <span data-ttu-id="4d490-121">Record ID lingua</span><span class="sxs-lookup"><span data-stu-id="4d490-121">Language ID Records</span></span>        | <span data-ttu-id="4d490-122">**BYTE**\[\]</span><span class="sxs-lookup"><span data-stu-id="4d490-122">**BYTE**\[\]</span></span> | <span data-ttu-id="4d490-123">Varia</span><span class="sxs-lookup"><span data-stu-id="4d490-123">Varies</span></span>  | <span data-ttu-id="4d490-124">Matrice di stringhe di linguaggio (vedere di seguito).</span><span class="sxs-lookup"><span data-stu-id="4d490-124">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="4d490-125">Il primo **valore DWORD** è il numero di lingue, seguito da una matrice di stringhe dell'identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="4d490-125">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="4d490-126">Ogni stringa ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="4d490-126">Each string has the following format:</span></span>



| <span data-ttu-id="4d490-127">Campo oggetto elenco lingue</span><span class="sxs-lookup"><span data-stu-id="4d490-127">Language List Object field</span></span> | <span data-ttu-id="4d490-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4d490-128">Data type</span></span>     | <span data-ttu-id="4d490-129">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4d490-129">Size</span></span>    | <span data-ttu-id="4d490-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d490-130">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d490-131">Lunghezza ID lingua</span><span class="sxs-lookup"><span data-stu-id="4d490-131">Language ID Length</span></span>         | <span data-ttu-id="4d490-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4d490-132">**DWORD**</span></span>     | <span data-ttu-id="4d490-133">4 byte</span><span class="sxs-lookup"><span data-stu-id="4d490-133">4 bytes</span></span> | <span data-ttu-id="4d490-134">Lunghezza della stringa in byte, incluse le dimensioni del carattere **null** finale.</span><span class="sxs-lookup"><span data-stu-id="4d490-134">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="4d490-135">ID lingua</span><span class="sxs-lookup"><span data-stu-id="4d490-135">Language ID</span></span>                | <span data-ttu-id="4d490-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="4d490-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="4d490-137">Varia</span><span class="sxs-lookup"><span data-stu-id="4d490-137">Varies</span></span>  | <span data-ttu-id="4d490-138">Stringa con terminazione null che contiene il nome della lingua RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="4d490-138">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="4d490-139">Ogni stringa è un tag di lingua conforme a RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="4d490-139">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="4d490-140">Per ottenere il tag di lingua per un flusso specifico nel file ASF, eseguire una query sul descrittore del flusso per l'attributo dell' [**\_ \_ \_ \_ \_ \_ indice di ID lingua MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4d490-140">To get the language tag for a particular stream in the ASF file, query the stream descriptor for the [**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="4d490-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="4d490-141">Examples</span></span>

<span data-ttu-id="4d490-142">Nell'esempio seguente viene illustrato come analizzare l'elenco di lingue.</span><span class="sxs-lookup"><span data-stu-id="4d490-142">The following example shows how to parse the language list.</span></span>


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a><span data-ttu-id="4d490-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d490-143">Requirements</span></span>



| <span data-ttu-id="4d490-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d490-144">Requirement</span></span> | <span data-ttu-id="4d490-145">Valore</span><span class="sxs-lookup"><span data-stu-id="4d490-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d490-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d490-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4d490-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d490-147">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4d490-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d490-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4d490-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d490-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4d490-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d490-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d490-151"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d490-151"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d490-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d490-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d490-153">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4d490-153">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4d490-154">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="4d490-154">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="4d490-155">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="4d490-155">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="4d490-156">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4d490-156">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4d490-157">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="4d490-157">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4d490-158">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="4d490-158">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="4d490-159">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="4d490-159">ASF Header Object</span></span>
</dt> <dt>

[<span data-ttu-id="4d490-160">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="4d490-160">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




