---
description: Accetta un flusso in un file di nota Journal e restituisce un flusso XML che rappresenta il contenuto del documento.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'Metodo IJournalReader:: ReadFromStream (Journal. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306063"
---
# <a name="ijournalreaderreadfromstream-method"></a><span data-ttu-id="1c4d5-103">Metodo IJournalReader:: ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="1c4d5-103">IJournalReader::ReadFromStream method</span></span>

<span data-ttu-id="1c4d5-104">Accetta un flusso in un file di nota Journal e restituisce un flusso XML che rappresenta il contenuto del documento.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-104">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span>

> [!Note]  
> <span data-ttu-id="1c4d5-105">Il componente Reader Journal non è in grado di leggere i file journal di Windows creati da computer che eseguono Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="1c4d5-106">L'interfaccia IJournalReader deve essere considerata deprecata o obsoleta e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1c4d5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c4d5-107">Syntax</span></span>


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a><span data-ttu-id="1c4d5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c4d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c4d5-109">*pJournalFileStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c4d5-109">*pJournalFileStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4d5-110">Oggetto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che rappresenta il file journal da leggere.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-110">An [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object representing the Journal file to read.</span></span>

</dd> <dt>

<span data-ttu-id="1c4d5-111">*ppXmlStream* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1c4d5-111">*ppXmlStream* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4d5-112">Puntatore all'indirizzo di un oggetto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che riceverà il flusso XML creato leggendo il file journal.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-112">A pointer to the address of an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object that will receive the XML stream created by reading the Journal file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c4d5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c4d5-113">Return value</span></span>

<span data-ttu-id="1c4d5-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c4d5-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c4d5-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c4d5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c4d5-116">Remarks</span></span>

<span data-ttu-id="1c4d5-117">I flussi vengono usati per evitare l'accesso diretto al file system e per consentire la scelta del metodo di analisi XML da usare.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-117">Streams are used to avoid direct access to the file system and to allow choice in which XML parsing method to use.</span></span>

## <a name="examples"></a><span data-ttu-id="1c4d5-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="1c4d5-118">Examples</span></span>

<span data-ttu-id="1c4d5-119">L'esempio seguente di un gestore per l'evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) di un pulsante Crea un'istanza dell'interfaccia dell' [**interfaccia IJournalReader**](ijournalreader.md) e la usa per leggere un file journal esistente.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-119">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the [**IJournalReader Interface**](ijournalreader.md) interface and uses it to read an existing Journal file.</span></span>


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a><span data-ttu-id="1c4d5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c4d5-120">Requirements</span></span>



| <span data-ttu-id="1c4d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4d5-121">Requirement</span></span> | <span data-ttu-id="1c4d5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1c4d5-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4d5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c4d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1c4d5-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c4d5-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1c4d5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c4d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1c4d5-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1c4d5-126">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="1c4d5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c4d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c4d5-128"><dt>Journal. h (richiede anche journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c4d5-128"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c4d5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1c4d5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c4d5-130"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c4d5-130"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="1c4d5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c4d5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4d5-132">**Interfaccia IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-132">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="1c4d5-133">Riferimento allo schema del lettore Journal</span><span class="sxs-lookup"><span data-stu-id="1c4d5-133">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

