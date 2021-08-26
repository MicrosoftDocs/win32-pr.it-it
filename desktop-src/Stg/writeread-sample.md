---
title: Esempio di WriteRead
description: WriteRead.cpp crea un set di proprietà, scrive una proprietà, chiude e riapre il set di proprietà e legge nuovamente la proprietà.
ms.assetid: c5807dd9-2928-497b-9446-729dcaeebc8a
keywords:
- Struttura Archiviazione Strctd Stg , esempi, WriteRead
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d869076635904ab61dcf3f210cf5e3cb96308a3e6ce20090dbd227e1f4e34d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034741"
---
# <a name="writeread-sample"></a>Esempio di WriteRead

WriteRead.cpp crea un set di proprietà, scrive una proprietà, chiude e riapre il set di proprietà e legge nuovamente la proprietà. Questa applicazione di esempio crea il file "WriteRead.stg" nella directory corrente. Crea set di proprietà in un file di archiviazione della struttura, ma una modifica di una riga determina la creazione di set di file system NTFS.


```C++
//+===================================================================
//
//      To build:
//      cl /GX WriteRead.cpp
//
//+===================================================================


#define WIN32_LEAN_AND_MEAN
#define UNICODE
#define _UNICODE

#include <stdio.h>
#include <windows.h>
#include <ole2.h>

// Implicitly link ole32.dll
#pragma comment( lib, "ole32.lib" )


// From uuidgen.exe:
const FMTID fmtid = { /* d170df2e-1117-11d2-aa01-00805ffe11b8 */
    0xd170df2e,
    0x1117,
    0x11d2,
    {0xaa, 0x01, 0x00, 0x80, 0x5f, 0xfe, 0x11, 0xb8}
  };


EXTERN_C void wmain()
{
   HRESULT hr = S_OK;
   IPropertySetStorage *pPropSetStg = NULL;
   IPropertyStorage *pPropStg = NULL;
   WCHAR *pwszError = L"";
   PROPSPEC propspec; 
   PROPVARIANT propvarWrite; 
   PROPVARIANT propvarRead;

   try
   {

        // Create a file and a property set within it.

        hr = StgCreateStorageEx( L"WriteRead.stg",
                   STGM_CREATE|STGM_SHARE_EXCLUSIVE|STGM_READWRITE,
                   STGFMT_STORAGE,
                   // STGFMT_STORAGE => Structured Storage 
                                     // property sets
                   // STGFMT_FILE    => NTFS file system 
                                     // property sets
                   0, NULL, NULL,
                   IID_IPropertySetStorage,
                   reinterpret_cast<void**>(&pPropSetStg) );
        if( FAILED(hr) ) throw L"Failed StgCreateStorageEx";

        hr = pPropSetStg->Create( fmtid, NULL, PROPSETFLAG_DEFAULT, 
                    STGM_CREATE|STGM_READWRITE|STGM_SHARE_EXCLUSIVE,
                    &pPropStg );
        if( FAILED(hr) ) throw L"Failed IPropertySetStorage::Create";

        // Write a Unicode string property to the property set

        propspec.ulKind = PRSPEC_LPWSTR;
        propspec.lpwstr = L"Property Name";

        propvarWrite.vt = VT_LPWSTR;
        propvarWrite.pwszVal = L"Property Value";

        hr = pPropStg->WriteMultiple( 1, &propspec, &propvarWrite, 
                                      PID_FIRST_USABLE );
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::WriteMultiple";

        // Not required, but give the property set a friendly 
        // name.

        PROPID propidDictionary = PID_DICTIONARY;
        WCHAR *pwszFriendlyName = 
                     L"Write/Read Properties Sample Property Set";
        hr = pPropStg->WritePropertyNames( 1, &propidDictionary, 
                                           &pwszFriendlyName );
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::WritePropertyNames";

        // Commit changes to the property set.

        hr = pPropStg->Commit(STGC_DEFAULT);
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::Commit";

        // Close and reopen everything.
        // By using the STGFMT_ANY flag in the StgOpenStorageEx call,
        // it does not matter if this is a Structured Storage 
        // property set or an NTFS file system property set 
        // (for more information see the StgCreateStorageEx 
        // call above).

        pPropStg->Release(); pPropStg = NULL;
        pPropSetStg->Release(); pPropSetStg = NULL;

        hr = StgOpenStorageEx( L"WriteRead.stg",
                             STGM_READ|STGM_SHARE_DENY_WRITE,
                             STGFMT_ANY,
                             0, NULL, NULL, 
                             IID_IPropertySetStorage,
                             reinterpret_cast<void**>(&pPropSetStg) );
        if( FAILED(hr) ) 
            throw L"Failed StgOpenStorageEx";

        hr = pPropSetStg->Open( fmtid, STGM_READ|STGM_SHARE_EXCLUSIVE,
                                &pPropStg );
        if( FAILED(hr) ) 
            throw L"Failed IPropertySetStorage::Open";

        // Read the property back and validate it

        hr = pPropStg->ReadMultiple( 1, &propspec, &propvarRead );
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::ReadMultiple";

        if( S_FALSE == hr )
          throw L"Property didn't exist after reopening the 
                                                     property set";
        else if( propvarWrite.vt != propvarRead.vt )
          throw L"Property types didn't match after reopening the 
                                                     property set";
        else if( 0 != wcscmp( propvarWrite.pwszVal, 
                              propvarRead.pwszVal ))
          throw L"Property values didn't match after reopening the 
                                                     property set";
        else
           wprintf( L"Success\n" );

   }
   catch( const WCHAR *pwszError )
   {
       wprintf( L"Error:  %s (hr=%08x)\n", pwszError, hr );
   }

   PropVariantClear( &propvarRead );
            if( pPropStg ) pPropStg->Release();
   if( pPropSetStg ) pPropSetStg->Release();

}
```



 

 




