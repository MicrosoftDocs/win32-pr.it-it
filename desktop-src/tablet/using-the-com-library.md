---
description: Panoramica della libreria COM e note sull'utilizzo delle sezioni relative alla tecnologia Tablet PC di Windows Vista SDK.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Uso della libreria COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343281"
---
# <a name="using-the-com-library"></a><span data-ttu-id="0cf0e-103">Uso della libreria COM</span><span class="sxs-lookup"><span data-stu-id="0cf0e-103">Using the COM Library</span></span>

<span data-ttu-id="0cf0e-104">Il riferimento alla libreria gestita da Tablet PC è ora disponibile nella sezione di riferimento normale della libreria di classi di Windows Vista SDK.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-104">The Tablet PC managed library reference can now be found in the regular Windows Vista SDK Class Library reference section.</span></span> <span data-ttu-id="0cf0e-105">Fornisce un modello a oggetti per Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-105">It provides an object model for Microsoft Visual C++.</span></span> <span data-ttu-id="0cf0e-106">La maggior parte degli oggetti nella libreria COM sono identici a quelli disponibili nell'API gestita di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-106">The majority of the objects in the COM Library are identical to those found in the Tablet PC Managed API.</span></span>

<span data-ttu-id="0cf0e-107">Tuttavia, l'API COM contiene alcuni membri, oltre a quelli disponibili nell'API gestita, a causa delle differenze tra l'ambiente Microsoft Win32 standard e l'ambiente Microsoft .NET Frameworksoftware Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0cf0e-107">However, the COM API contains some members in addition to those found in the Managed API because of differences between the standard Microsoft Win32 environment and the Microsoft .NET Frameworksoftware development kit (SDK) environment.</span></span> <span data-ttu-id="0cf0e-108">Gli oggetti InkRectangle e InkTransform, ad esempio, vengono usati in COM, ma FrameworkSDK fornisce l'implementazione nativa per la [**classe InkRectangle**](inkrectangle-class.md) e la [**classe InkTransform**](inktransform-class.md) che elimina la necessità di questi oggetti nell'API gestita della piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-108">For example, the InkRectangle and InkTransform objects are used in COM, but the FrameworkSDK provides native implementation for [**InkRectangle Class**](inkrectangle-class.md) and [**InkTransform Class**](inktransform-class.md) that eliminates the need for these objects in the Tablet PC platform Managed API.</span></span>

> [!Note]  
> <span data-ttu-id="0cf0e-109">Gli oggetti nell'API COM e i controlli Ink non sono progettati per l'utilizzo in Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="0cf0e-109">The objects in the COM API and the ink controls are not designed for use in Active Server Pages (ASP).</span></span>

 

## <a name="working-with-collections"></a><span data-ttu-id="0cf0e-110">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="0cf0e-110">Working with Collections</span></span>

<span data-ttu-id="0cf0e-111">Se si passa un valore **null** come indice a uno degli oggetti della raccolta nella libreria com, si riceve il primo elemento della raccolta perché questi valori di argomento sono assegnati a 0 quando viene effettuata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-111">If you pass in a **NULL** value as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

<span data-ttu-id="0cf0e-112">La proprietà **\_ NewEnum** è contrassegnata con restrizioni nella definizione del linguaggio di definizione dell'interfaccia (IDL) per le interfacce di raccolta.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-112">The **\_NewEnum** property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.</span></span>

<span data-ttu-id="0cf0e-113">In C++ usare un `For...` ciclo per scorrere una raccolta ottenendo innanzitutto la lunghezza della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-113">In C++, use a `For...` loop to iterate through a collection by first obtaining the collection's length.</span></span> <span data-ttu-id="0cf0e-114">Nell'esempio seguente viene illustrato come scorrere i tratti di un oggetto [**InkDisp**](inkdisp-class.md) `pInk` .</span><span class="sxs-lookup"><span data-stu-id="0cf0e-114">The example below shows how to iterate through the strokes of an [**InkDisp**](inkdisp-class.md) object, `pInk`.</span></span>


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a><span data-ttu-id="0cf0e-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cf0e-115">Parameters</span></span>

<span data-ttu-id="0cf0e-116">Se si passa VT \_ Empty o VT \_ null come indice a uno degli oggetti della raccolta nella libreria com, si riceve il primo elemento della raccolta perché i valori degli argomenti vengono assegnati a 0 quando viene effettuata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-116">If you pass in VT\_EMPTY or VT\_NULL as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

## <a name="using-idispatch"></a><span data-ttu-id="0cf0e-117">Uso di IDispatch</span><span class="sxs-lookup"><span data-stu-id="0cf0e-117">Using IDispatch</span></span>

<span data-ttu-id="0cf0e-118">Per migliorare le prestazioni, il Application Programming Interface COM della piattaforma Tablet PC (API) non supporta la chiamata `IDispatchImpl::Invoke` a con una struttura DISPPARAMS con argomenti denominati.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-118">To increase performance, the Tablet PC Platform COM application programming interface (API) does not support calling `IDispatchImpl::Invoke` with a DISPPARAMS structure with named arguments.</span></span> <span data-ttu-id="0cf0e-119">`IDispatchImpl::GetIDsOfNames`Non è inoltre supportata.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-119">The `IDispatchImpl::GetIDsOfNames` is also not supported.</span></span> <span data-ttu-id="0cf0e-120">Chiamare invece `Invoke` con i DISPID forniti nelle intestazioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-120">Instead, call `Invoke` with the DISPIDs supplied in the SDK headers.</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="0cf0e-121">In attesa di eventi</span><span class="sxs-lookup"><span data-stu-id="0cf0e-121">Waiting for Events</span></span>

<span data-ttu-id="0cf0e-122">L'ambiente Tablet PC è multithreading.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-122">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="0cf0e-123">Vedere la documentazione COM per il multithreading.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-123">Refer to COM documentation for multi-threading.</span></span>

## <a name="support-for-aggregation"></a><span data-ttu-id="0cf0e-124">Supporto per l'aggregazione</span><span class="sxs-lookup"><span data-stu-id="0cf0e-124">Support for Aggregation</span></span>

<span data-ttu-id="0cf0e-125">L'aggregazione è stata testata solo per il controllo [InkEdit](inkedit-control-reference.md) , il controllo [InkPicture](inkpicture-control-reference.md) , l'oggetto [**InkDisp**](inkdisp-class.md) e l'oggetto [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="0cf0e-125">Aggregation has been tested for only the [InkEdit](inkedit-control-reference.md) control, the [InkPicture](inkpicture-control-reference.md) control, the [**InkDisp**](inkdisp-class.md) object, and the [**InkOverlay**](inkoverlay-class.md) object.</span></span> <span data-ttu-id="0cf0e-126">L'aggregazione non è stata testata per altri controlli e oggetti nella libreria.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-126">Aggregation has not been tested for other controls and objects in the library.</span></span>

## <a name="c"></a><span data-ttu-id="0cf0e-127">C++</span><span class="sxs-lookup"><span data-stu-id="0cf0e-127">C++</span></span>

<span data-ttu-id="0cf0e-128">Per utilizzare Tablet PC SDK in C++, è necessario utilizzare alcuni concetti COM, ad esempio VARIANT, SAFEARRAY e BSTR.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-128">Using the Tablet PC SDK in C++ requires the use of some COM concepts, such as VARIANT, SAFEARRAY, and BSTR.</span></span> <span data-ttu-id="0cf0e-129">Questa sezione descrive come usarli.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-129">This section describes how to use them.</span></span>

### <a name="variant-and-safearray"></a><span data-ttu-id="0cf0e-130">VARIANT e SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="0cf0e-130">VARIANT and SAFEARRAY</span></span>

<span data-ttu-id="0cf0e-131">La struttura VARIANT viene utilizzata per la comunicazione tra oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-131">The VARIANT structure is used for communication between COM objects.</span></span> <span data-ttu-id="0cf0e-132">In pratica, la struttura VARIANT è un contenitore per un'Unione di grandi dimensioni che contiene molti tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-132">Essentially, the VARIANT structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="0cf0e-133">Il valore nel primo membro della struttura, VT, descrive quale dei membri di Unione è valido.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-133">The value in the first member of the structure, vt, describes which of the union members is valid.</span></span> <span data-ttu-id="0cf0e-134">Quando si ricevono informazioni in una struttura VARIANT, controllare il membro VT per individuare il membro che contiene dati validi.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-134">When you receive information in a VARIANT structure, check the vt member to find out which member contains valid data.</span></span> <span data-ttu-id="0cf0e-135">Analogamente, quando si inviano informazioni utilizzando una struttura VARIANT, impostare sempre VT per riflettere il membro dell'Unione che contiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-135">Similarly, when you send information using a VARIANT structure, always set vt to reflect the union member that contains the information.</span></span>

<span data-ttu-id="0cf0e-136">Prima di usare la struttura, inizializzarla chiamando la funzione COM VariantInit.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-136">Before using the structure, initialize it by calling the VariantInit COM function.</span></span> <span data-ttu-id="0cf0e-137">Al termine della struttura, cancellarlo prima che la memoria che contiene la variante venga liberata chiamando VariantClear.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-137">When finished with the structure, clear it before the memory that contains the VARIANT is freed by calling VariantClear.</span></span>

<span data-ttu-id="0cf0e-138">Per ulteriori informazioni sulla struttura VARIANT, vedere [Variant e tipi di dati VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="0cf0e-138">For more information on the VARIANT structure, see [VARIANT and VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="0cf0e-139">La struttura SAFEARRAY viene fornita come metodo per lavorare in modo sicuro con le matrici in COM.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-139">The SAFEARRAY structure is provided as a way to safely work with arrays in COM.</span></span> <span data-ttu-id="0cf0e-140">Il campo pArray della variante è un puntatore a un SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-140">The VARIANT's parray field is a pointer to a SAFEARRAY.</span></span> <span data-ttu-id="0cf0e-141">Usare funzioni quali SafeArrayCreateVector, SafeArrayAccessData e SafeArrayUnaccessData per creare e riempire un SAFEARRAY in una variante.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-141">Use functions such as SafeArrayCreateVector, SafeArrayAccessData, and SafeArrayUnaccessData to create and fill a SAFEARRAY in a VARIANT.</span></span>

<span data-ttu-id="0cf0e-142">Per altre informazioni sul tipo di dati SAFEARRAY, vedere [tipo di dati SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="0cf0e-142">For more information on the SAFEARRAY data type, see [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

<span data-ttu-id="0cf0e-143">Questo esempio di C++ crea un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , in un oggetto [**InkDisp**](inkdisp-class.md) , `pInk` , da una matrice di dati punto.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-143">This C++ example creates an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp`, in an [**InkDisp**](inkdisp-class.md) object, `pInk`, from an array of point data.</span></span>


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a><span data-ttu-id="0cf0e-144">BSTR</span><span class="sxs-lookup"><span data-stu-id="0cf0e-144">BSTR</span></span>

<span data-ttu-id="0cf0e-145">Il formato di stringa supportato per COM è BSTR.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-145">The supported string format for COM is BSTR.</span></span> <span data-ttu-id="0cf0e-146">Un BSTR presenta un puntatore a una stringa con terminazione zero, ma contiene anche la lunghezza della stringa (in byte, senza contare il carattere di terminazione), che viene archiviato nei 4 byte immediatamente precedenti al primo carattere della stringa.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-146">A BSTR has a pointer to a zero-terminated string, but it also contains the length of the string (in bytes, not counting the terminator), which is stored in the 4 bytes immediately preceding the first character of the string.</span></span>

<span data-ttu-id="0cf0e-147">Per ulteriori informazioni su BSTR, vedere [tipo di dati BSTR](/previous-versions/windows/desktop/automat/bstr).</span><span class="sxs-lookup"><span data-stu-id="0cf0e-147">For more information on BSTR, see [BSTR Data Type](/previous-versions/windows/desktop/automat/bstr).</span></span>

<span data-ttu-id="0cf0e-148">In questo esempio di C++ viene illustrato come impostare il controllo del controllo in un [**InkRecognizerContext**](inkrecognizercontext-class.md) utilizzando un BSTR.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-148">This C++ sample shows how to set the factoid on an [**InkRecognizerContext**](inkrecognizercontext-class.md) using a BSTR.</span></span>


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
