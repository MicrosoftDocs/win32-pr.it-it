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
# <a name="ijournalreader-interface"></a>Interfaccia IJournalReader

Fornisce l'accesso in lettura a un file journal di Windows, restituendo un flusso contenente una versione XML del contenuto del file.

> [!Note]  
> Il componente Reader Journal non è in grado di leggere i file journal di Windows creati da computer che eseguono Windows 7 o versioni successive. L'interfaccia IJournalReader deve essere considerata deprecata o obsoleta e non deve essere utilizzata.

 

## <a name="members"></a>Membri

L'interfaccia **IJournalReader** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IJournalReader** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IJournalReader** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**ReadFromStream**](ijournalreader-readfromstream.md) | Accetta un flusso in un file di nota Journal e restituisce un flusso XML che rappresenta il contenuto del documento.<br/> |



 

## <a name="remarks"></a>Commenti

La classe **JournalReader** consente di caricare un flusso di documenti Journal e di ricevere un flusso XML che rappresenta il contenuto. È possibile ricostituire, visualizzare e modificare l'input penna.

## <a name="examples"></a>Esempio

L'esempio seguente di un gestore per l'evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) di un pulsante Crea un'istanza della classe **JournalReader** e la usa per leggere un file journal esistente.

> [!Note]  
> Il metodo **DisplayXml** chiamato da questo esempio non viene visualizzato. L'implementazione specifica di questo metodo dipende dalle esigenze dell'applicazione.

 


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                         |
| Intestazione<br/>                   | <dl> <dt>Journal. h (richiede anche journal \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GUID proprietà personalizzati](custom-property-guids.md)
</dt> <dt>

[**Metodo ReadFromStream**](ijournalreader-readfromstream.md)
</dt> </dl>

 

