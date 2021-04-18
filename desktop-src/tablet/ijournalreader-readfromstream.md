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
# <a name="ijournalreaderreadfromstream-method"></a>Metodo IJournalReader:: ReadFromStream

Accetta un flusso in un file di nota Journal e restituisce un flusso XML che rappresenta il contenuto del documento.

> [!Note]  
> Il componente Reader Journal non è in grado di leggere i file journal di Windows creati da computer che eseguono Windows 7 o versioni successive. L'interfaccia IJournalReader deve essere considerata deprecata o obsoleta e non deve essere utilizzata.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJournalFileStream* \[ in\]
</dt> <dd>

Oggetto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che rappresenta il file journal da leggere.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Puntatore all'indirizzo di un oggetto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che riceverà il flusso XML creato leggendo il file journal.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

I flussi vengono usati per evitare l'accesso diretto al file system e per consentire la scelta del metodo di analisi XML da usare.

## <a name="examples"></a>Esempio

L'esempio seguente di un gestore per l'evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) di un pulsante Crea un'istanza dell'interfaccia dell' [**interfaccia IJournalReader**](ijournalreader.md) e la usa per leggere un file journal esistente.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                         |
| Intestazione<br/>                   | <dl> <dt>Journal. h (richiede anche journal \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IJournalReader**](ijournalreader.md)
</dt> <dt>

[Riferimento allo schema del lettore Journal](journal-reader-schema-reference.md)
</dt> </dl>

 

