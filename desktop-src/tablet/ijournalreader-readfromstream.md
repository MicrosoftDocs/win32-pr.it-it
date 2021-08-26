---
description: Accetta un flusso in un file journal note e restituisce un flusso XML che rappresenta il contenuto del documento.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: Metodo IJournalReader::ReadFromStream (Journal.h)
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
ms.openlocfilehash: 7dbe9d7929f616914d06cad237f486677cd8e5616cb04bf28a5836751ca0a3c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057851"
---
# <a name="ijournalreaderreadfromstream-method"></a>Metodo IJournalReader::ReadFromStream

Accetta un flusso in un file journal note e restituisce un flusso XML che rappresenta il contenuto del documento.

> [!Note]  
> Il componente Lettore journal non è in grado Windows file Journal creati da computer che eseguono Windows 7 o versioni successive. L'interfaccia IJournalReader deve essere considerata deprecata o obsoleta e non deve essere usata.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJournalFileStream* \[ Pollici\]
</dt> <dd>

Oggetto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che rappresenta il file Journal da leggere.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Puntatore all'indirizzo di un [**oggetto IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che riceverà il flusso XML creato leggendo il file Journal.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Flussi vengono usati per evitare l'accesso diretto al file system e per consentire la scelta del metodo di analisi XML da usare.

## <a name="examples"></a>Esempio

L'esempio seguente di un gestore per l'evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) di un pulsante crea un'istanza dell'interfaccia [**IJournalReader e**](ijournalreader.md) la usa per leggere un file Journal esistente.


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
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                         |
| Intestazione<br/>                   | <dl> <dt>Journal.h (richiede anche journal \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IJournalReader**](ijournalreader.md)
</dt> <dt>

[Informazioni di riferimento sullo schema del lettore journal](journal-reader-schema-reference.md)
</dt> </dl>

 

