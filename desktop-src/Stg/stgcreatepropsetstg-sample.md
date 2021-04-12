---
title: Esempio StgCreatePropSetStg
description: Mostra come è possibile usare la funzione StgCreatePropSetStg per creare un'interfaccia IPropertySetStorage su una determinata interfaccia IStorage.
ms.assetid: f0d0664a-2cfd-4eb0-b1d5-47d1545394fd
keywords:
- Archiviazione strutturata Strctd STG, esempi, StgCreatePropSetStg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5633089e10f5f98a6acd8cd75b5f8bc6e4a97e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396606"
---
# <a name="stgcreatepropsetstg-sample"></a>Esempio StgCreatePropSetStg

L'esempio StgCreatePropSetStg. cpp Mostra come è possibile usare la funzione [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) per creare un'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) su qualsiasi interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) specificata.


```C++
//+===================================================================
//
// To Build:   cl /GX StgCreatePropSetStg.cpp
//
//+===================================================================

#define UNICODE
#define _UNICODE
#define WIN32_LEAN_AND_MEAN

#include <stdio.h>
#include <windows.h>
#include <ole2.h>

#pragma comment( lib, "ole32.lib" )

IPropertyStorage*
CreatePropertySetInStorage( IStorage *pStg, const FMTID &fmtid )
{
    HRESULT hr = S_OK;
    IPropertySetStorage *pPropSetStg = NULL;
    IPropertyStorage *pPropStg = NULL;

    try
    {
        hr = StgCreatePropSetStg( pStg, 0 /*reserved*/, 
                                  &pPropSetStg );
        if( FAILED(hr) ) 
            throw L"Failed StgCreatePropSetStg (%08x)";

        hr = pPropSetStg->Create( fmtid, NULL,
            PROPSETFLAG_DEFAULT,
            STGM_CREATE | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
            &pPropStg );
        if( FAILED(hr) ) 
            throw L"Failed IPropertySetStorage::Create (%08x)";

        // Success. The caller must now call Release on both
        // pPropSetStg and pStg.

    }
    catch( const WCHAR *pwszError )
    {
        wprintf( L"Error: %s (%08x)\n", pwszError, hr );
    }

    if( NULL != pPropSetStg )
        pPropSetStg->Release();

    return( pPropStg );
}


extern "C" void wmain()
{
    HRESULT hr = S_OK;
    IStorage *pStg = NULL;
    IPropertyStorage *pPropStg = NULL;

    try
    {
        // Create an object with an IStorage interface. It is not 
        // necessary that it be a system-provided storage, such as 
        // that obtained by this call.  Any object that implements 
        // IStorage can be used.

        hr = StgCreateStorageEx( NULL,  // Create a temporary storage.
                                 STGM_CREATE
                                    | STGM_READWRITE
                                    | STGM_SHARE_EXCLUSIVE,
                                 STGFMT_STORAGE,
                                 0, NULL, NULL,
                                 IID_IStorage,
                                 reinterpret_cast<void**>(&pStg) );
        if( FAILED(hr) ) throw L"Failed StgCreateStorageEx";

        // Get and use an IPropertySetStorage that represents this 
        // IStorage.

        pPropStg = CreatePropertySetInStorage( pStg, 
                                        FMTID_SummaryInformation );
        if( NULL == pPropStg ) 
           throw L"Failed CreatePropertySetInStorage";

        // Here you could call IPropertyStorage methods, such as 
        // WriteMultiple andReadMultiple, using the pPropStg pointer.

        printf( "Success\n" );
    }
    catch( const WCHAR *pwszError )
    {
        wprintf( L"Error: %s (%08x)\n", pwszError, hr );
    }

    if( NULL != pPropStg )
        pPropStg->Release();
    if( NULL != pStg )
        pStg->Release();

}
```



 

 




