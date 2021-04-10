---
title: Funzioni helper di enumerazione
description: Sono disponibili tre funzioni di supporto enumeratore che possono essere utilizzate da C/C++ per facilitare l'esplorazione degli oggetti Active Directory. Sono ADsBuildEnumerator, ADsEnumerateNext e ADsFreeEnumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- ADsBuildEnumerator ADSI, utilizzo
- ADsEnumerateNext ADSI, utilizzo
- ADsFreeEnumerator ADSI, utilizzo
- ADSI ADSI, codice di esempio C/C++, uso di ADsBuildEnumerator ADsEnumerateNext e ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9597787202adf183435262eab9341957e19457
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118447"
---
# <a name="enumeration-helper-functions"></a>Funzioni helper di enumerazione

Sono disponibili tre funzioni di supporto enumeratore che possono essere utilizzate da C/C++ per facilitare l'esplorazione degli oggetti Active Directory. Sono [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)e [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).

## <a name="adsbuildenumerator"></a>ADsBuildEnumerator

La funzione helper [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) incapsula il codice necessario per creare un oggetto enumeratore. Chiama il metodo [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) per creare un oggetto enumeratore e quindi chiama il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per ottenere un puntatore all'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) per quell'oggetto. L'oggetto enumerazione è il meccanismo di automazione che consente di enumerare i contenitori. Utilizzare la funzione [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) per rilasciare questo oggetto enumeratore.

## <a name="adsenumeratenext"></a>ADsEnumerateNext

La funzione helper [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) compila una matrice Variant con gli elementi recuperati da un oggetto enumeratore. Il numero di elementi recuperati può essere minore di quello richiesto.

## <a name="adsfreeenumerator"></a>ADsFreeEnumerator

Libera un oggetto enumeratore creato in precedenza tramite la funzione [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .

Nell'esempio di codice seguente viene illustrata una funzione che utilizza funzioni helper enumeratore in C++.


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



 

 