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
# <a name="using-the-com-library"></a>Uso della libreria COM

Il riferimento alla libreria gestita da Tablet PC è ora disponibile nella sezione di riferimento normale della libreria di classi di Windows Vista SDK. Fornisce un modello a oggetti per Microsoft Visual C++. La maggior parte degli oggetti nella libreria COM sono identici a quelli disponibili nell'API gestita di Tablet PC.

Tuttavia, l'API COM contiene alcuni membri, oltre a quelli disponibili nell'API gestita, a causa delle differenze tra l'ambiente Microsoft Win32 standard e l'ambiente Microsoft .NET Frameworksoftware Development Kit (SDK). Gli oggetti InkRectangle e InkTransform, ad esempio, vengono usati in COM, ma FrameworkSDK fornisce l'implementazione nativa per la [**classe InkRectangle**](inkrectangle-class.md) e la [**classe InkTransform**](inktransform-class.md) che elimina la necessità di questi oggetti nell'API gestita della piattaforma Tablet PC.

> [!Note]  
> Gli oggetti nell'API COM e i controlli Ink non sono progettati per l'utilizzo in Active Server Pages (ASP).

 

## <a name="working-with-collections"></a>Uso delle raccolte

Se si passa un valore **null** come indice a uno degli oggetti della raccolta nella libreria com, si riceve il primo elemento della raccolta perché questi valori di argomento sono assegnati a 0 quando viene effettuata la chiamata.

La proprietà **\_ NewEnum** è contrassegnata con restrizioni nella definizione del linguaggio di definizione dell'interfaccia (IDL) per le interfacce di raccolta.

In C++ usare un `For...` ciclo per scorrere una raccolta ottenendo innanzitutto la lunghezza della raccolta. Nell'esempio seguente viene illustrato come scorrere i tratti di un oggetto [**InkDisp**](inkdisp-class.md) `pInk` .


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

Se si passa VT \_ Empty o VT \_ null come indice a uno degli oggetti della raccolta nella libreria com, si riceve il primo elemento della raccolta perché i valori degli argomenti vengono assegnati a 0 quando viene effettuata la chiamata.

## <a name="using-idispatch"></a>Uso di IDispatch

Per migliorare le prestazioni, il Application Programming Interface COM della piattaforma Tablet PC (API) non supporta la chiamata `IDispatchImpl::Invoke` a con una struttura DISPPARAMS con argomenti denominati. `IDispatchImpl::GetIDsOfNames`Non è inoltre supportata. Chiamare invece `Invoke` con i DISPID forniti nelle intestazioni dell'SDK.

## <a name="waiting-for-events"></a>In attesa di eventi

L'ambiente Tablet PC è multithreading. Vedere la documentazione COM per il multithreading.

## <a name="support-for-aggregation"></a>Supporto per l'aggregazione

L'aggregazione è stata testata solo per il controllo [InkEdit](inkedit-control-reference.md) , il controllo [InkPicture](inkpicture-control-reference.md) , l'oggetto [**InkDisp**](inkdisp-class.md) e l'oggetto [**InkOverlay**](inkoverlay-class.md) . L'aggregazione non è stata testata per altri controlli e oggetti nella libreria.

## <a name="c"></a>C++

Per utilizzare Tablet PC SDK in C++, è necessario utilizzare alcuni concetti COM, ad esempio VARIANT, SAFEARRAY e BSTR. Questa sezione descrive come usarli.

### <a name="variant-and-safearray"></a>VARIANT e SAFEARRAY

La struttura VARIANT viene utilizzata per la comunicazione tra oggetti COM. In pratica, la struttura VARIANT è un contenitore per un'Unione di grandi dimensioni che contiene molti tipi di dati.

Il valore nel primo membro della struttura, VT, descrive quale dei membri di Unione è valido. Quando si ricevono informazioni in una struttura VARIANT, controllare il membro VT per individuare il membro che contiene dati validi. Analogamente, quando si inviano informazioni utilizzando una struttura VARIANT, impostare sempre VT per riflettere il membro dell'Unione che contiene le informazioni.

Prima di usare la struttura, inizializzarla chiamando la funzione COM VariantInit. Al termine della struttura, cancellarlo prima che la memoria che contiene la variante venga liberata chiamando VariantClear.

Per ulteriori informazioni sulla struttura VARIANT, vedere [Variant e tipi di dati VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

La struttura SAFEARRAY viene fornita come metodo per lavorare in modo sicuro con le matrici in COM. Il campo pArray della variante è un puntatore a un SAFEARRAY. Usare funzioni quali SafeArrayCreateVector, SafeArrayAccessData e SafeArrayUnaccessData per creare e riempire un SAFEARRAY in una variante.

Per altre informazioni sul tipo di dati SAFEARRAY, vedere [tipo di dati SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray).

Questo esempio di C++ crea un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , in un oggetto [**InkDisp**](inkdisp-class.md) , `pInk` , da una matrice di dati punto.


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

Il formato di stringa supportato per COM è BSTR. Un BSTR presenta un puntatore a una stringa con terminazione zero, ma contiene anche la lunghezza della stringa (in byte, senza contare il carattere di terminazione), che viene archiviato nei 4 byte immediatamente precedenti al primo carattere della stringa.

Per ulteriori informazioni su BSTR, vedere [tipo di dati BSTR](/previous-versions/windows/desktop/automat/bstr).

In questo esempio di C++ viene illustrato come impostare il controllo del controllo in un [**InkRecognizerContext**](inkrecognizercontext-class.md) utilizzando un BSTR.


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



 

 
