---
title: Funzioni helper di enumerazione
description: Esistono tre funzioni helper di enumeratore che possono essere usate da C/C++ per facilitare la navigazione degli oggetti di Active Directory. Si tratta di ADsBuildEnumerator, ADsEnumerateNext e ADsFreeEnumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- ADsBuildEnumerator ADSI ,using
- ADsEnumerateNext ADSI ,using
- ADsFreeEnumerator ADSI ,using
- ADSI ADSI , codice di esempio C/C++ con ADsBuildEnumerator ADsEnumerateNext e ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c110fbc4fddd420bf8205d6c2d894c7d4f4daf8287312c2d0d86002f5520310b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082655"
---
# <a name="enumeration-helper-functions"></a>Funzioni helper di enumerazione

Esistono tre funzioni helper di enumeratore che possono essere usate da C/C++ per facilitare la navigazione degli oggetti di Active Directory. Sono [**ADsBuildEnumerator,**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)e [**ADsFreeEnumerator.**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)

## <a name="adsbuildenumerator"></a>ADsBuildEnumerator

La funzione helper [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) incapsula il codice necessario per creare un oggetto enumeratore. Chiama il [**metodo IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) per creare un oggetto enumeratore e quindi chiama il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per ottenere un puntatore all'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) per tale oggetto. L'oggetto enumerazione è il meccanismo di automazione per enumerare i contenitori. Usare la [**funzione ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) per rilasciare questo oggetto enumeratore.

## <a name="adsenumeratenext"></a>ADsEnumerateNext

La funzione helper [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) popola una matrice VARIANT con gli elementi recuperati da un oggetto enumeratore. Il numero di elementi recuperati può essere inferiore al numero richiesto.

## <a name="adsfreeenumerator"></a>ADsFreeEnumerator

Libera un oggetto enumeratore creato in precedenza tramite la [**funzione ADsBuildEnumerator.**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)

Nell'esempio di codice seguente viene illustrata una funzione che usa funzioni helper dell'enumeratore in C++.


```C++
/*****************************************************************************
  Function:    TestEnumObject
  Arguments:   pszADsPath - ADsPath of the container to be enumerated (WCHAR*).
  Return:      S_OK if successful, an error code otherwise.
  Purpose:     Example using ADsBuildEnumerator, ADsEnumerateNext and
               ADsFreeEnumerator.
******************************************************************************/
#define MAX_ENUM      100  
 
HRESULT
TestEnumObject( LPWSTR pszADsPath )
{
    ULONG cElementFetched = 0L;
    IEnumVARIANT * pEnumVariant = NULL;
    VARIANT VariantArray[MAX_ENUM];
    HRESULT hr = S_OK;
    IADsContainer * pADsContainer =  NULL;
    DWORD dwObjects = 0, dwEnumCount = 0, i = 0;
    BOOL  fContinue = TRUE;
 
 
    hr = ADsGetObject(
                pszADsPath,
                IID_IADsContainer,
                (void **)&pADsContainer
                );
 
 
    if (FAILED(hr)) {
 
        printf("\"%S\" is not a valid container object.\n", pszADsPath) ;
        goto exitpoint ;
    }
 
    hr = ADsBuildEnumerator(
            pADsContainer,
            &pEnumVariant
            );
 
    if( FAILED( hr ) )
    {
      printf("ADsBuildEnumerator failed with %lx\n", hr ) ;
      goto exitpoint ;
    }
 
    fContinue  = TRUE;
    while (fContinue) {
 
        IADs *pObject ;
 
        hr = ADsEnumerateNext(
                    pEnumVariant,
                    MAX_ENUM,
                    VariantArray,
                    &cElementFetched
                    );

        if ( FAILED( hr ) )
        {
            printf("ADsEnumerateNext failed with %lx\n",hr);
            goto exitpoint;
        }
 
        if (hr == S_FALSE) {
            fContinue = FALSE;
        }
 
        dwEnumCount++;
 
        for (i = 0; i < cElementFetched; i++ ) {
 
            IDispatch *pDispatch    = NULL;
            BSTR        bstrADsPath = NULL;
 
            pDispatch = VariantArray[i].pdispVal;
 
            hr = V_DISPATCH( VariantArray + i )->QueryInterface(IID_IADs, (void **) &pObject) ;
 
            if( SUCCEEDED( hr ) )
            {
               pObject->get_ADsPath( &bstrADsPath );
               printf( "%S\n", bstrADsPath );
            }
            pObject->Release();
            VariantClear( VariantArray + i );
            SysFreeString( bstrADsPath );
        }
 
        dwObjects += cElementFetched;
    }
 
    printf("Total Number of Objects enumerated is %d\n", dwObjects);
 
exitpoint:
    if (pEnumVariant) {
        ADsFreeEnumerator( pEnumVariant );
    }
 
    if (pADsContainer) {
        pADsContainer->Release();
    }
 
    return(hr);
}
```



 

 