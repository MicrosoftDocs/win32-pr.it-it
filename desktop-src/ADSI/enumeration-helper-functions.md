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
# <a name="enumeration-helper-functions"></a><span data-ttu-id="23c46-108">Funzioni helper di enumerazione</span><span class="sxs-lookup"><span data-stu-id="23c46-108">Enumeration Helper Functions</span></span>

<span data-ttu-id="23c46-109">Sono disponibili tre funzioni di supporto enumeratore che possono essere utilizzate da C/C++ per facilitare l'esplorazione degli oggetti Active Directory.</span><span class="sxs-lookup"><span data-stu-id="23c46-109">There are three enumerator helper functions that can be used from C/C++ to aid in the navigation of Active Directory objects.</span></span> <span data-ttu-id="23c46-110">Sono [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)e [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span><span class="sxs-lookup"><span data-stu-id="23c46-110">They are [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext), and [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span></span>

## <a name="adsbuildenumerator"></a><span data-ttu-id="23c46-111">ADsBuildEnumerator</span><span class="sxs-lookup"><span data-stu-id="23c46-111">ADsBuildEnumerator</span></span>

<span data-ttu-id="23c46-112">La funzione helper [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) incapsula il codice necessario per creare un oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="23c46-112">The [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) helper function encapsulates the code required to create an enumerator object.</span></span> <span data-ttu-id="23c46-113">Chiama il metodo [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) per creare un oggetto enumeratore e quindi chiama il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per ottenere un puntatore all'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) per quell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23c46-113">It calls the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) method to create an enumerator object and then calls the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to get a pointer to the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface for that object.</span></span> <span data-ttu-id="23c46-114">L'oggetto enumerazione è il meccanismo di automazione che consente di enumerare i contenitori.</span><span class="sxs-lookup"><span data-stu-id="23c46-114">The enumeration object is the Automation mechanism to enumerate over containers.</span></span> <span data-ttu-id="23c46-115">Utilizzare la funzione [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) per rilasciare questo oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="23c46-115">Use the [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) function to release this enumerator object.</span></span>

## <a name="adsenumeratenext"></a><span data-ttu-id="23c46-116">ADsEnumerateNext</span><span class="sxs-lookup"><span data-stu-id="23c46-116">ADsEnumerateNext</span></span>

<span data-ttu-id="23c46-117">La funzione helper [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) compila una matrice Variant con gli elementi recuperati da un oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="23c46-117">The [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) helper function populates a VARIANT array with elements fetched from an enumerator object.</span></span> <span data-ttu-id="23c46-118">Il numero di elementi recuperati può essere minore di quello richiesto.</span><span class="sxs-lookup"><span data-stu-id="23c46-118">The number of elements retrieved can be smaller than the number requested.</span></span>

## <a name="adsfreeenumerator"></a><span data-ttu-id="23c46-119">ADsFreeEnumerator</span><span class="sxs-lookup"><span data-stu-id="23c46-119">ADsFreeEnumerator</span></span>

<span data-ttu-id="23c46-120">Libera un oggetto enumeratore creato in precedenza tramite la funzione [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .</span><span class="sxs-lookup"><span data-stu-id="23c46-120">Frees an enumerator object previously created through the [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) function.</span></span>

<span data-ttu-id="23c46-121">Nell'esempio di codice seguente viene illustrata una funzione che utilizza funzioni helper enumeratore in C++.</span><span class="sxs-lookup"><span data-stu-id="23c46-121">The following code example shows a function that uses enumerator helper functions in C++.</span></span>


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



 

 