---
description: Fornisce l'accesso in lettura a un file journal di Windows, restituendo un flusso contenente una versione XML del contenuto del file.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Interfaccia IJournalReader (Journal. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349911"
---
# <a name="ijournalreader-interface"></a><span data-ttu-id="07f66-103">Interfaccia IJournalReader</span><span class="sxs-lookup"><span data-stu-id="07f66-103">IJournalReader interface</span></span>

<span data-ttu-id="07f66-104">Fornisce l'accesso in lettura a un file journal di Windows, restituendo un flusso contenente una versione XML del contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="07f66-104">Provides read access to a Windows Journal file, returning a stream containing an XML version of the file's contents.</span></span>

> [!Note]  
> <span data-ttu-id="07f66-105">Il componente Reader Journal non è in grado di leggere i file journal di Windows creati da computer che eseguono Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="07f66-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="07f66-106">L'interfaccia IJournalReader deve essere considerata deprecata o obsoleta e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07f66-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="members"></a><span data-ttu-id="07f66-107">Membri</span><span class="sxs-lookup"><span data-stu-id="07f66-107">Members</span></span>

<span data-ttu-id="07f66-108">L'interfaccia **IJournalReader** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="07f66-108">The **IJournalReader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="07f66-109">**IJournalReader** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07f66-109">**IJournalReader** also has these types of members:</span></span>

-   [<span data-ttu-id="07f66-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="07f66-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="07f66-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="07f66-111">Methods</span></span>

<span data-ttu-id="07f66-112">L'interfaccia **IJournalReader** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="07f66-112">The **IJournalReader** interface has these methods.</span></span>



| <span data-ttu-id="07f66-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="07f66-113">Method</span></span>                                                  | <span data-ttu-id="07f66-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07f66-114">Description</span></span>                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07f66-115">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="07f66-115">**ReadFromStream**</span></span>](ijournalreader-readfromstream.md) | <span data-ttu-id="07f66-116">Accetta un flusso in un file di nota Journal e restituisce un flusso XML che rappresenta il contenuto del documento.</span><span class="sxs-lookup"><span data-stu-id="07f66-116">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07f66-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="07f66-117">Remarks</span></span>

<span data-ttu-id="07f66-118">La classe **JournalReader** consente di caricare un flusso di documenti Journal e di ricevere un flusso XML che rappresenta il contenuto.</span><span class="sxs-lookup"><span data-stu-id="07f66-118">The **JournalReader** class enables you to load a Journal document stream and to receive an XML stream representing the contents.</span></span> <span data-ttu-id="07f66-119">È possibile ricostituire, visualizzare e modificare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="07f66-119">You can reconstitute, display, and manipulate the ink.</span></span>

## <a name="examples"></a><span data-ttu-id="07f66-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="07f66-120">Examples</span></span>

<span data-ttu-id="07f66-121">L'esempio seguente di un gestore per l'evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) di un pulsante Crea un'istanza della classe **JournalReader** e la usa per leggere un file journal esistente.</span><span class="sxs-lookup"><span data-stu-id="07f66-121">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the **JournalReader** class and uses it to read an existing Journal file.</span></span>

> [!Note]  
> <span data-ttu-id="07f66-122">Il metodo **DisplayXml** chiamato da questo esempio non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="07f66-122">The **DisplayXml** method called from this example is not shown.</span></span> <span data-ttu-id="07f66-123">L'implementazione specifica di questo metodo dipende dalle esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="07f66-123">The specific implementation of such a method is dependent on your application's needs.</span></span>

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a><span data-ttu-id="07f66-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07f66-124">Requirements</span></span>



| <span data-ttu-id="07f66-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="07f66-125">Requirement</span></span> | <span data-ttu-id="07f66-126">Valore</span><span class="sxs-lookup"><span data-stu-id="07f66-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07f66-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07f66-127">Minimum supported client</span></span><br/> | <span data-ttu-id="07f66-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="07f66-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07f66-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07f66-129">Minimum supported server</span></span><br/> | <span data-ttu-id="07f66-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07f66-130">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="07f66-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07f66-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="07f66-132"><dt>Journal. h (richiede anche journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="07f66-132"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="07f66-133">DLL</span><span class="sxs-lookup"><span data-stu-id="07f66-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07f66-134"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07f66-134"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="07f66-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07f66-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f66-136">GUID proprietà personalizzati</span><span class="sxs-lookup"><span data-stu-id="07f66-136">Custom Property GUIDs</span></span>](custom-property-guids.md)
</dt> <dt>

[<span data-ttu-id="07f66-137">**Metodo ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="07f66-137">**ReadFromStream Method**</span></span>](ijournalreader-readfromstream.md)
</dt> </dl>

 

