---
description: Panoramica della libreria COM e note sull'uso della tecnologia Tablet PC di Windows Vista SDK.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Uso della libreria COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf986d79011301abe6a9f279a83278fda5dd9e33e3a79335d7d94e6081fb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819141"
---
# <a name="using-the-com-library"></a>Uso della libreria COM

Le informazioni di riferimento sulla libreria gestita per Tablet PC sono ora disponibili nella sezione di riferimento Windows riferimento alla libreria di classi di Vista SDK. Fornisce un modello a oggetti per Microsoft Visual C++. La maggior parte degli oggetti nella libreria COM è identica a quella presente nell'API gestita di Tablet PC.

Tuttavia, l'API COM contiene alcuni membri oltre a quelli presenti nell'API gestita a causa delle differenze tra l'ambiente Microsoft Win32 standard e l'ambiente Microsoft .NET Frameworksoftware Development Kit (SDK). Ad esempio, gli oggetti InkRectangle e InkTransform vengono usati in COM, ma FrameworkSDK fornisce l'implementazione nativa per la classe [**InkRectangle**](inkrectangle-class.md) e la classe [**InkTransform**](inktransform-class.md) che elimina la necessità di questi oggetti nell'API gestita della piattaforma Tablet PC.

> [!Note]  
> Gli oggetti nell'API COM e i controlli input penna non sono progettati per l'uso in asp (Active Server asp).

 

## <a name="working-with-collections"></a>Uso delle raccolte

Se si passa un valore **NULL** come indice a uno degli oggetti raccolta nella libreria COM, si riceve il primo elemento nella raccolta perché questi valori di argomento vengono forzati a 0 quando viene effettuata la chiamata.

La **\_ proprietà NewEnum** è contrassegnata come limitata nella definizione IDL (Interface Definition Language) per le interfacce di raccolta.

In C++ usare un ciclo per scorrere una raccolta ottenendo prima la `For...` lunghezza della raccolta. L'esempio seguente illustra come scorrere i tratti di un [**oggetto InkDisp,**](inkdisp-class.md) `pInk` .


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



## <a name="parameters"></a>Parametri

Se si passa VT EMPTY o VT NULL come indice a uno degli oggetti raccolta nella libreria COM, si riceve il primo elemento della raccolta perché questi valori di argomento vengono forzati a 0 quando viene effettuata \_ \_ la chiamata.

## <a name="using-idispatch"></a>Uso di IDispatch

Per migliorare le prestazioni, l'API (Application Programming Interface) COM della piattaforma Tablet PC non supporta la chiamata con una `IDispatchImpl::Invoke` struttura DISPPARAMS con argomenti denominati. Anche `IDispatchImpl::GetIDsOfNames` l'oggetto non è supportato. Chiamare invece `Invoke` con i DISPID specificati nelle intestazioni dell'SDK.

## <a name="waiting-for-events"></a>In attesa di eventi

L'ambiente Tablet PC è multithreading. Per il multithreading, vedere la documentazione COM.

## <a name="support-for-aggregation"></a>Supporto per l'aggregazione

L'aggregazione è stata testata solo per il controllo [InkEdit,](inkedit-control-reference.md) il [controllo InkPicture,](inkpicture-control-reference.md) l'oggetto [**InkDisp**](inkdisp-class.md) e [**l'oggetto InkOverlay.**](inkoverlay-class.md) L'aggregazione non è stata testata per altri controlli e oggetti nella libreria.

## <a name="c"></a>C++

L'uso di Tablet PC SDK in C++ richiede l'uso di alcuni concetti COM, ad esempio VARIANT, SAFEARRAY e BSTR. In questa sezione viene descritto come usarli.

### <a name="variant-and-safearray"></a>VARIANT e SAFEARRAY

La struttura VARIANT viene utilizzata per la comunicazione tra oggetti COM. In sostanza, la struttura VARIANT è un contenitore per un'unione di grandi dimensioni che contiene molti tipi di dati.

Il valore nel primo membro della struttura, vt, descrive quale dei membri di unione è valido. Quando si ricevono informazioni in una struttura VARIANT, controllare il membro vt per scoprire quale membro contiene dati validi. Analogamente, quando si inviano informazioni usando una struttura VARIANT, impostare sempre vt in modo che rifletta il membro di unione che contiene le informazioni.

Prima di usare la struttura , inizializzarla chiamando la funzione COM VariantInit. Al termine della struttura , cancellarla prima che la memoria che contiene VARIANT venga liberata chiamando VariantClear.

Per altre informazioni sulla struttura VARIANT, vedere [Tipi di dati VARIANT e VARIANTARG.](/windows/win32/api/oaidl/ns-oaidl-variant)

La struttura SAFEARRAY viene fornita come modo per lavorare in modo sicuro con le matrici in COM. Il campo parray di VARIANT è un puntatore a safeARRAY. Usare funzioni come SafeArrayCreateVector, SafeArrayAccessData e SafeArrayUnaccessData per creare e compilare un SAFEARRAY in variant.

Per altre informazioni sul tipo di dati SAFEARRAY, vedere [Tipo di dati SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray).

Questo esempio di C++ crea un [**oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , , in un `pInkStrokeDisp` oggetto [**InkDisp,**](inkdisp-class.md) `pInk` , da una matrice di dati punto.


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



### <a name="bstr"></a>BSTR

Il formato di stringa supportato per COM è BSTR. Un BSTR ha un puntatore a una stringa con terminazione zero, ma contiene anche la lunghezza della stringa (in byte, senza contare il carattere di terminazione), archiviata nei 4 byte immediatamente precedenti al primo carattere della stringa.

Per altre informazioni su BSTR, vedere [Tipo di dati BSTR.](/previous-versions/windows/desktop/automat/bstr)

Questo esempio di C++ illustra come impostare il factoid in [**inkRecognizerContext**](inkrecognizercontext-class.md) usando un oggetto BSTR.


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



 

 
