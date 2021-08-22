---
description: Un provider WMI crea un gruppo di classi, istanze ed eventi supportati per passare dati a WMI. A sua volta, un'applicazione di gestione o uno script può chiamare i metodi del provider per modificare i dati forniti dal provider.
ms.assetid: 919dfa7c-4a36-4e59-8377-72cf9735eaec
ms.tgt_platform: multiple
title: Fornire dati a WMI scrivendo un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9410fd26a830df1846dd62434dc85ffc9cb033c524c7b4e76ff6db93d64dd95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050144"
---
# <a name="supplying-data-to-wmi-by-writing-a-provider"></a>Fornire dati a WMI scrivendo un provider

Un provider WMI crea un gruppo di classi, istanze ed eventi supportati per passare dati a WMI. A sua volta, un'applicazione di gestione o uno script può chiamare [*i metodi del provider*](gloss-p.md) per modificare i dati forniti dal provider.

Il diagramma seguente illustra la relazione tra un provider abbinato a WMI e all'applicazione.

![relazione tra WMI, provider accoppiato e applicazione](images/coupledprov.png)

Nella procedura seguente viene descritto come creare un provider semplice che supporta un set di istanze di . Il provider descritto qui è registrato per l'esecuzione all'interno del processo WMI. In alcuni casi, usare un [*provider disaccoccodato*](gloss-d.md) che viene eseguito in un processo diverso. Per altre informazioni sui modelli di hosting del provider, vedere [Provider Hosting and Security](provider-hosting-and-security.md). I passaggi 1 e 2 della procedura seguente differiscono per i provider disaccoccodati, ma per altri aspetti usano le stesse interfacce dei provider in-process. Per altre informazioni, vedere [Incorporamento di un provider in un'applicazione.](incorporating-a-provider-in-an-application.md)

**Per creare un provider di istanze**

1.  Creare un'istanza di [**\_ \_ una classe Win32Provider**](--win32provider.md) [con Managed Object Format (MOF),](managed-object-format--mof-.md) specificando il nome e **il CLSID** del provider. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

    Nell'esempio di codice seguente viene illustrato come creare un'istanza di [**\_ \_ una classe Win32Provider.**](--win32provider.md)

    ``` syntax
    Instance of __Win32Provider as $P   // $P is an alias
    {
      // Name that describes your provider
      Name        = "InstProvSamp" ;   
      ClsId   = "{22CB8761-914A-11cf-B705-00AA0062CBB7}" ;
    } ;   
    ```

    > [!Note]  
    > Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti siano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e si riavvia, usare l'istruzione del preprocessore [**\# pragma autorecover**](pragma-autorecover.md) nel file MOF.

     

    Per altre informazioni, vedere [Creazione di un'istanza e](creating-an-instance.md) Registrazione di un provider di [istanze.](registering-an-instance-provider.md)

2.  Creare un'istanza della [**\_ \_ classe InstanceProviderRegistration**](--instanceproviderregistration.md) che descrive le funzionalità del provider di istanze.

    L'esempio di codice seguente illustra come creare un'istanza della [**\_ \_ classe InstanceProviderRegistration.**](--instanceproviderregistration.md)

    ``` syntax
    instance of __InstanceProviderRegistration
    {
      Provider = $P;                // Alias to the __Win32Provider
      SupportsPut = FALSE;          // Does not support the Put method
      SupportsGet = TRUE;           // Supports the Get method
      SupportsDelete = FALSE;       // Does not support the Delete method
      SupportsEnumeration = TRUE;   // Supports enumeration.
    };
    ```

    Per altre informazioni sulle proprietà in questa sezione del codice MOF, vedere [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) [**\_ \_ e ObjectProviderRegistration.**](--objectproviderregistration.md)

    Per altre informazioni, vedere [Registrazione di un provider di istanze.](registering-an-instance-provider.md)

3.  Usare il codice MOF per creare la classe dinamica per la quale il provider fornisce istanze di .

    Una classe dinamica è una classe le cui istanze ricevono aggiornamenti da un provider. Questi aggiornamenti possono essere regolari o collegati a modifiche sporadiche negli oggetti che le istanze rappresentano. È possibile visualizzare le modifiche apportate alle istanze di classe dinamica tramite la propria applicazione di gestione o il [Visualizzatore oggetti WMI.](further-information.md)

    Nell'esempio di codice seguente viene descritta una classe dinamica supportata dal provider "InstProvSamp".

    ``` syntax
    [dynamic, provider("InstProvSamp"), // uses the InstProvSamp Provider
    ClassContext("whatever!")]          // information is dynamically
                                        // supported by the provider
    class InstProvSamp
    {
      [key]
      // MyKey uniquely identifies this class
      String MyKey="HELLO";   

      // InstProvSamp dynamically updates MyValue
      [PropertyContext("Name")] 
      uint32 MyValue;
    };
    ```

4.  Registrare le classi con WMI tramite il compilatore MOF.

    Dal prompt dei comandi nella directory del provider digitare quanto segue per registrare il codice MOF di esempio con WMI.

    **mofcomp** *instprov.mof*

    Per altre informazioni, vedere [Compilazione di file MOF.](compiling-mof-files.md)

5.  Definire un oggetto COM per contenere il provider. Il codice di esempio per questo passaggio è disponibile in un esempio completo alla fine di questo argomento.

    1.  Come per qualsiasi oggetto COM, è necessario implementare un costruttore e un decostruttore, nonché i [**metodi QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) [**e Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)

    2.  Implementare [**il metodo IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) nell'oggetto COM.

        Lo scopo principale di [**Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) in questo esempio è impostare il membro **m \_ pNamespace** nello spazio dei nomi corrente. Per altre informazioni sugli spazi dei nomi, vedere [Creazione di gerarchie all'interno di WMI.](creating-hierarchies-within-wmi.md)

        Un sink viene passato tramite il *parametro pInitSink* nel metodo [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) per indica che il provider è stato inizializzato correttamente. Per altre informazioni sui sink, vedere [**IWbemObjectSink**](iwbemobjectsink.md) e [Chiamata di un metodo](calling-a-method.md).

    3.  Implementare il metodo [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) all'interno dell'oggetto COM (anche se è possibile implementare un'ampia gamma di interfacce [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) l'esempio alla fine di questo argomento implementa solo **CreateInstanceEnumAsync).** In particolare, **CreateInstanceEnumAsync** restituisce istanze di oggetti specificati a WMI.

    4.  Implementare il [**metodo GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) all'interno dell'oggetto COM.

        Nell'esempio alla fine di questo argomento [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) controlla i parametri nell'oggetto gestito, recupera l'oggetto specificato, esegue il controllo degli errori e restituisce i codici appropriati al sink.

6.  Registrare il provider come oggetto COM usando RegSvr32.

    Dal prompt dei comandi nella directory del provider digitare quanto segue:

    **regsvr32** *InstProv.dll*

Il provider è ora completo. A questo punto, dovrebbe essere possibile accedere alle istanze della **classe InstProvSamp** dall'interno di WMI.

Nell'esempio di codice seguente viene creato un oggetto COM per contenere il provider, come descritto nel passaggio 5 precedente. L'esempio completo contiene il codice del file di intestazione Sample.h e dei file di origine intitolati Instprov.cpp, Utils.cpp, Classfac.cpp e Maindll.cpp.


```C++
//*******************************************************************
//  sample.h
//  WMI Instance provider sample code
//
// Copyright (C) Microsoft. All Rights Reserved.
//
//*******************************************************************

#ifndef _sample_H_
#define _sample_H_

#include <wbemprov.h>
#pragma comment(lib, "wbemuuid.lib")

typedef LPVOID * PPVOID;

// Provider interfaces are provided by objects of this class
 
class CInstPro : public IWbemServices, public IWbemProviderInit
    {
    protected:
        ULONG m_cRef;         //Object reference count
        IWbemServices* m_pNamespace;
     public:
        CInstPro(BSTR ObjectPath = NULL, BSTR User = NULL, BSTR Password = NULL, IWbemContext * pCtx=NULL);
        ~CInstPro(void);

        //Non-delegating object IUnknown

        STDMETHODIMP QueryInterface(REFIID, PPVOID);
        STDMETHODIMP_(ULONG) AddRef(void);
        STDMETHODIMP_(ULONG) Release(void);

        //IWbemProviderInit

        HRESULT STDMETHODCALLTYPE Initialize(
             /* [in] */ LPWSTR pszUser,
             /* [in] */ LONG lFlags,
             /* [in] */ LPWSTR pszNamespace,
             /* [in] */ LPWSTR pszLocale,
             /* [in] */ IWbemServices *pNamespace,
             /* [in] */ IWbemContext *pCtx,
             /* [in] */ IWbemProviderInitSink *pInitSink
                        );

        SCODE GetByPath( BSTR             Path,
                         IWbemClassObject FAR* FAR* pObj,
                         IWbemContext     *pCtx);

        //IWbemServices  

        HRESULT STDMETHODCALLTYPE OpenNamespace( 
            /* [in] */ const BSTR Namespace,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [unique][in][out] */ IWbemServices __RPC_FAR *__RPC_FAR *ppWorkingNamespace,
            /* [unique][in][out] */ IWbemCallResult __RPC_FAR *__RPC_FAR *ppResult) 
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE CancelAsyncCall( 
            /* [in] */ IWbemObjectSink __RPC_FAR *pSink)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE QueryObjectSink( 
            /* [in] */ long lFlags,
            /* [out] */ IWbemObjectSink __RPC_FAR *__RPC_FAR *ppResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE GetObject( 
            /* [in] */ const BSTR ObjectPath,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [unique][in][out] */ IWbemClassObject __RPC_FAR *__RPC_FAR *ppObject,
            /* [unique][in][out] */ IWbemCallResult __RPC_FAR *__RPC_FAR *ppCallResult)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE GetObjectAsync( 
            /* [in] */ const BSTR ObjectPath,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler);
        
        HRESULT STDMETHODCALLTYPE PutClass( 
            /* [in] */ IWbemClassObject __RPC_FAR *pObject,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [unique][in][out] */ IWbemCallResult __RPC_FAR *__RPC_FAR *ppCallResult) 
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE PutClassAsync( 
            /* [in] */ IWbemClassObject __RPC_FAR *pObject,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE DeleteClass( 
            /* [in] */ const BSTR Class,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [unique][in][out] */ IWbemCallResult __RPC_FAR *__RPC_FAR *ppCallResult)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE DeleteClassAsync( 
            /* [in] */ const BSTR Class,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE CreateClassEnum( 
            /* [in] */ const BSTR Superclass,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [out] */ 
            IEnumWbemClassObject __RPC_FAR *__RPC_FAR *ppEnum)
            {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE CreateClassEnumAsync( 
            /* [in] */ const BSTR Superclass,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE PutInstance( 
            /* [in] */ IWbemClassObject __RPC_FAR *pInst,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [unique][in][out] */ IWbemCallResult __RPC_FAR *__RPC_FAR *ppCallResult)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE PutInstanceAsync( 
            /* [in] */ IWbemClassObject __RPC_FAR *pInst,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE DeleteInstance( 
            /* [in] */ const BSTR ObjectPath,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [unique][in][out] */ IWbemCallResult __RPC_FAR *__RPC_FAR *ppCallResult)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE DeleteInstanceAsync( 
            /* [in] */ const BSTR ObjectPath,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE CreateInstanceEnum( 
            /* [in] */ const BSTR Class,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [out] */ IEnumWbemClassObject __RPC_FAR *__RPC_FAR *ppEnum)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE CreateInstanceEnumAsync( 
            /* [in] */ const BSTR Class,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler);
        
        HRESULT STDMETHODCALLTYPE ExecQuery( 
            /* [in] */ const BSTR QueryLanguage,
            /* [in] */ const BSTR Query,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [out] */ IEnumWbemClassObject __RPC_FAR *__RPC_FAR *ppEnum)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE ExecQueryAsync( 
            /* [in] */ const BSTR QueryLanguage,
            /* [in] */ const BSTR Query,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE ExecNotificationQuery( 
            /* [in] */ const BSTR QueryLanguage,
            /* [in] */ const BSTR Query,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [out] */ IEnumWbemClassObject __RPC_FAR *__RPC_FAR *ppEnum)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE ExecNotificationQueryAsync( 
            /* [in] */ const BSTR QueryLanguage,
            /* [in] */ const BSTR Query,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler)
        {return WBEM_E_NOT_SUPPORTED;};
        
        HRESULT STDMETHODCALLTYPE ExecMethod( const BSTR,
                                              const BSTR,
                                              long,
                                              IWbemContext*,
                                              IWbemClassObject*,
                                              IWbemClassObject**,
                                              IWbemCallResult**)
        {return WBEM_E_NOT_SUPPORTED;}

        HRESULT STDMETHODCALLTYPE ExecMethodAsync( const BSTR,
                                                   const BSTR,
                                                   long, 
                                                   IWbemContext*,
                                                   IWbemClassObject*,
                                                   IWbemObjectSink*)
        {return WBEM_E_NOT_SUPPORTED;}

};

typedef CInstPro *PCInstPro;

// This class is the class factory for CInstPro objects.

class CProvFactory : public IClassFactory
    {
    protected:
        ULONG m_cRef;

    public:
        CProvFactory(void);
        ~CProvFactory(void);

        //IUnknown members
        STDMETHODIMP QueryInterface(REFIID, PPVOID);
        STDMETHODIMP_(ULONG) AddRef(void);
        STDMETHODIMP_(ULONG) Release(void);

        //IClassFactory members
        STDMETHODIMP CreateInstance(LPUNKNOWN, REFIID, PPVOID);
        STDMETHODIMP LockServer(BOOL);
    };

typedef CProvFactory *PCProvFactory;



// These variables keep track of
// when the module can be unloaded

extern long g_cObj;
extern long g_cLock;

// General purpose utilities.  

DWORD GetCurrentImpersonationLevel ();

             
SCODE CreateInst( IWbemServices * pNamespace,
                  LPWSTR pKey, long lVal,
                  IWbemClassObject ** pNewInst,
                  WCHAR * pwcClassName,
                  IWbemContext  *pCtx); 

typedef struct {
   WCHAR * pwcKey;
   long lValue;
   } InstDef;

extern InstDef MyDefs[];
extern long glNumInst;


#endif
```



Il file di origine Instpro.cpp contiene il codice che implementa le funzioni per il provider dichiarato nel file di intestazione Sample.h.


```C++
//*******************************************************************
//  INSTPRO.CPP
//
//  Module: WMI Instance provider sample code
//
//  Purpose: Defines the CInstPro class.  An object of this class is
//           created by the class factory for each connection.
// Copyright (C) Microsoft. All Rights Reserved.
//
//*******************************************************************
#define _WIN32_WINNT 0x0500


#include <objbase.h>
#include "sample.h"
#include <process.h>
#include <strsafe.h>
#include <sddl.h>

InstDef MyDefs[] = {{L"a", 1}, {L"b", 2}, {L"c", 3}};

long glNumInst = sizeof(MyDefs)/sizeof(InstDef);

//*******************************************************************
//
// CInstPro::CInstPro
// CInstPro::~CInstPro
//
//*******************************************************************

CInstPro::CInstPro(BSTR ObjectPath,
                   BSTR User,
                   BSTR Password,
                   IWbemContext * pCtx)
{
    m_pNamespace = NULL;
    m_cRef=0;
    InterlockedIncrement(&g_cObj);
    return;
}

CInstPro::~CInstPro(void)
{
    if(m_pNamespace)
        m_pNamespace->Release();
    InterlockedDecrement(&g_cObj);
    return;
}

//*******************************************************************
//
// CInstPro::QueryInterface
// CInstPro::AddRef
// CInstPro::Release
//
// Purpose: IUnknown members for CInstPro object.
//*******************************************************************


STDMETHODIMP CInstPro::QueryInterface(REFIID riid, PPVOID ppv)
{
    *ppv=NULL;

    // Because you have dual inheritance,
    // it is necessary to cast the return type

    if(riid== IID_IWbemServices)
       *ppv=(IWbemServices*)this;

    if(IID_IUnknown==riid || riid== IID_IWbemProviderInit)
       *ppv=(IWbemProviderInit*)this;
    

    if (NULL!=*ppv) 
    {
        AddRef();
        return NOERROR;
    }
    else
        return E_NOINTERFACE;
  
}


STDMETHODIMP_(ULONG) CInstPro::AddRef(void)
{
    return ++m_cRef;
}

STDMETHODIMP_(ULONG) CInstPro::Release(void)
{
    ULONG nNewCount = InterlockedDecrement((long *)&m_cRef);
    if (0L == nNewCount)
        delete this;
    
    return nNewCount;
}

/********************************************************************
*         
*   CInstPro::Initialize     
*                                                                    
*   Purpose: This is the implementation of IWbemProviderInit. 
*            The method is required to initialize with CIMOM.
*   
********************************************************************/

STDMETHODIMP CInstPro::Initialize(LPWSTR pszUser, 
                                  LONG lFlags,
                                  LPWSTR pszNamespace, 
                                  LPWSTR pszLocale,
                                  IWbemServices *pNamespace, 
                                  IWbemContext *pCtx,
                                  IWbemProviderInitSink *pInitSink)
{
    if(! pNamespace)
    {
        pInitSink->SetStatus(WBEM_E_FAILED , 0);
    }
    else
    {
        m_pNamespace = pNamespace;
        m_pNamespace->AddRef();
        pInitSink->SetStatus(WBEM_S_INITIALIZED, 0);
    }

    
    return WBEM_S_NO_ERROR;
}

//*******************************************************************
//
// CInstPro::CreateInstanceEnumAsync
//
// Purpose: Asynchronously enumerates the instances.  
//
//*******************************************************************

SCODE CInstPro::CreateInstanceEnumAsync( const BSTR RefStr,
                                         long lFlags,
                                         IWbemContext *pCtx,
                                         IWbemObjectSink FAR* pHandler)
{

    //Impersonate the client
    HRESULT hr = CoImpersonateClient () ;

    if ( FAILED ( hr ) )
    {
        pHandler->SetStatus ( 0 , hr , NULL , NULL ) ;
        return hr ;
    }

    // Check to see if call is at lower than 
    // RPC_C_IMP_LEVEL_IMPERSONATE level. If that is the case,
    // the provider will not be able to impersonate
    // the client to access the protected resources. 

    DWORD t_CurrentImpersonationLevel = 
        GetCurrentImpersonationLevel () ;
    if ( t_CurrentImpersonationLevel < RPC_C_IMP_LEVEL_IMPERSONATE )
    {
        // Revert before you perform any operations 
        CoRevertToSelf () ;

        hr = WBEM_E_ACCESS_DENIED;
        pHandler->SetStatus ( 0 , hr , NULL , NULL ) ;
        return hr ;
    }

    SCODE sc;
    int iCnt;
    IWbemClassObject FAR* pNewInst;
  
    // Do a check of arguments and ensure
    // you have a pointer to Namespace

    if(pHandler == NULL || m_pNamespace == NULL)
        return WBEM_E_INVALID_PARAMETER;

    for(iCnt=0; iCnt < glNumInst; iCnt++)
    {
        sc = CreateInst(m_pNamespace,MyDefs[iCnt].pwcKey, MyDefs[iCnt].lValue, &pNewInst, RefStr, pCtx);
 
        if(sc != S_OK)
            break;

        // Send the object to the caller

        pHandler->Indicate(1,&pNewInst);
        pNewInst->Release();
    }

    // Set status

    pHandler->SetStatus(0,sc,NULL, NULL);

    return sc;
}


//*******************************************************************
//
// CInstPro::GetObjectByPath
// CInstPro::GetObjectByPathAsync
//
// Purpose: Creates an instance given a particular path value.
//
//*******************************************************************



SCODE CInstPro::GetObjectAsync(const BSTR      ObjectPath,
                               long            lFlags,
                               IWbemContext    *pCtx,
                               IWbemObjectSink FAR* pHandler)
{

    //Impersonate the client
    HRESULT hr = CoImpersonateClient () ;

    if ( FAILED ( hr ) )
    {
        pHandler->SetStatus ( 0 , hr , NULL , NULL ) ;
        return hr ;
    } 

    // Check to see if call is at the 
    // RPC_C_IMP_LEVEL_IDENTIFY level. If that is the case,
    // the provider will not be able to impersonate
    // the client to access the protected resources.
    if (GetCurrentImpersonationLevel () == RPC_C_IMP_LEVEL_IDENTIFY)
    {
        hr = WBEM_E_ACCESS_DENIED;
        pHandler->SetStatus ( 0 , hr , NULL , NULL ) ;
        return hr ;
    }

    SCODE sc;
    IWbemClassObject FAR* pObj;
    BOOL bOK = FALSE;

    // Do a check of arguments and ensure
    // you have a pointer to Namespace

    if(ObjectPath == NULL || 
        pHandler == NULL || 
        m_pNamespace == NULL)
        return WBEM_E_INVALID_PARAMETER;

    // do the get, pass the object on to the notify
    
    sc = GetByPath(ObjectPath,&pObj, pCtx);
    if(sc == S_OK) 
    {
        pHandler->Indicate(1,&pObj);
        pObj->Release();
        bOK = TRUE;
    }

    sc = (bOK) ? S_OK : WBEM_E_NOT_FOUND;

    // Set Status

    pHandler->SetStatus(0,sc, NULL, NULL);

    return sc;
}
 
//*******************************************************************
//
// CInstPro::GetByPath
//
// Purpose: Creates an instance given a particular Path value.
//
//*******************************************************************

SCODE CInstPro::GetByPath(BSTR ObjectPath,
                          IWbemClassObject FAR* FAR* ppObj,
                          IWbemContext  *pCtx)
{
    SCODE sc = S_OK;
    
    int iCnt;

    // Do a simple path parse.  The path looks like
    // InstProvSamp.MyKey="a"
    // Create a test string with just the part between quotes.

    WCHAR wcTest[MAX_PATH+1];
    memset(wcTest, NULL, sizeof(wcTest));
    StringCbCopyW(wcTest, sizeof(wcTest), ObjectPath);

    WCHAR * pwcTest, * pwcCompare = NULL;
    int iNumQuotes = 0;
    for(pwcTest = wcTest; *pwcTest; pwcTest++)
        if(*pwcTest == L'\"')
        {
            iNumQuotes++;
            if(iNumQuotes == 1)
            {
                pwcCompare = pwcTest+1;
            }
            else if(iNumQuotes == 2)
            {
                *pwcTest = NULL;
                break;
            }
        }
        else if(*pwcTest == L'.')
            *pwcTest = NULL;    // isolate the class name.
    if(iNumQuotes != 2)
        return WBEM_E_FAILED;

    // check the instance list for a match.

    for(iCnt = 0; iCnt < glNumInst; iCnt++)
    {
        if(!_wcsicmp(MyDefs[iCnt].pwcKey, pwcCompare))
        {
            sc = CreateInst(m_pNamespace,MyDefs[iCnt].pwcKey, MyDefs[iCnt].lValue, ppObj, wcTest, pCtx);
            return sc;
        }
    }

    return WBEM_E_NOT_FOUND;
}
```



Il file di origine Utils.cpp contiene il codice che implementa le funzioni di utilità per il provider dichiarato nel file di intestazione Sample.h.


```C++
//*******************************************************************
//  UTILS.CPP
//  Module: WMI Instance provider sample code
//  Purpose: General purpose utilities.  
// (c) Microsoft. All rights reserved.
//
//*******************************************************************

#include <objbase.h>
#include "sample.h"

//*******************************************************************
//
// CreateInst
//
// Purpose: Creates a new instance and sets
//          the initial values of the properties.
//
// Return:   S_OK if all is well, otherwise an error code is returned
//
//*******************************************************************

SCODE CreateInst(IWbemServices * pNamespace, 
                 LPWSTR pKey, 
                 long lVal, 
                 IWbemClassObject ** pNewInst,
                 WCHAR * pwcClassName,
                 IWbemContext  *pCtx)
{
    SCODE sc;
    IWbemClassObject * pClass = NULL;
    sc = pNamespace->GetObject(pwcClassName, 0, pCtx, &pClass, NULL);
    if(sc != S_OK)
        return WBEM_E_FAILED;
    sc = pClass->SpawnInstance(0, pNewInst);
    pClass->Release();
    if(FAILED(sc))
        return sc;
    VARIANT v;

    // Set the key property value.

    v.vt = VT_BSTR;
    v.bstrVal = SysAllocString(pKey);
    if (!v.bstrVal)
        return WBEM_E_OUT_OF_MEMORY;

    sc = (*pNewInst)->Put(L"MyKey", 0, &v, 0);
    VariantClear(&v);
    if(FAILED(sc))
        return sc;

    // Set the number property value.

    v.vt = VT_I4;
    v.lVal = lVal;
    sc = (*pNewInst)->Put(L"MyValue", 0, &v, 0);
    return sc;
}


/********************************************************************
 *
 * Name: GetCurrentImpersonationLevel
 * Description: Get COM impersonation level of caller. 
 *
 *******************************************************************/

DWORD GetCurrentImpersonationLevel ()
{
    DWORD t_ImpersonationLevel = RPC_C_IMP_LEVEL_ANONYMOUS ;
    HANDLE t_ThreadToken = NULL ;
    BOOL t_Status = OpenThreadToken(GetCurrentThread(),TOKEN_QUERY,TRUE,&t_ThreadToken);

    if ( t_Status )
    {
        SECURITY_IMPERSONATION_LEVEL t_Level = SecurityAnonymous ;
        DWORD t_Returned = 0 ;

        t_Status = GetTokenInformation( t_ThreadToken, 
                                        TokenImpersonationLevel, 
                                        &t_Level, 
                                        sizeof(SECURITY_IMPERSONATION_LEVEL),
                                        &t_Returned);

        CloseHandle ( t_ThreadToken ) ;

        if ( t_Status == FALSE )
        {
            t_ImpersonationLevel = RPC_C_IMP_LEVEL_ANONYMOUS ;
        }
        else
        {
            switch ( t_Level )
            {
                case SecurityAnonymous:
                {
                    t_ImpersonationLevel = RPC_C_IMP_LEVEL_ANONYMOUS;
                }
                break;

                case SecurityIdentification:
                {
                    t_ImpersonationLevel = RPC_C_IMP_LEVEL_IDENTIFY;
                }
                break ;

                case SecurityImpersonation:
                {
                    t_ImpersonationLevel = RPC_C_IMP_LEVEL_IMPERSONATE;
                }
                break ;

                case SecurityDelegation:
                {
                    t_ImpersonationLevel = RPC_C_IMP_LEVEL_DELEGATE ;
                }
                break ;

                default:
                {
                    t_ImpersonationLevel = RPC_C_IMP_LEVEL_ANONYMOUS ;
                }
                break ;
            }
        }
    }
    else
    {
        ULONG t_LastError = GetLastError () ;

        if ( t_LastError == ERROR_NO_IMPERSONATION_TOKEN ||
            t_LastError == ERROR_NO_TOKEN )
        {
            t_ImpersonationLevel = RPC_C_IMP_LEVEL_DELEGATE ;
        }
        else 
        {
            if ( t_LastError == ERROR_CANT_OPEN_ANONYMOUS )
            {
                t_ImpersonationLevel = RPC_C_IMP_LEVEL_ANONYMOUS ;
            }
            else
            {
                t_ImpersonationLevel = RPC_C_IMP_LEVEL_ANONYMOUS ;
            }
        }
    }

    return t_ImpersonationLevel ;
}

```



Il file di origine Classfac.cpp contiene il codice che crea oggetti quando vengono richieste le connessioni.


```C++
//*******************************************************************
//
//  CLASSFAC.CPP
//  Module: WMI Instance provider sample code
//  Purpose: Contains the class factory.  This creates objects when
//           connections are requested.
// Copyright (C) Microsoft. All Rights Reserved.
//
//*******************************************************************

#include <objbase.h>
#include "sample.h"

//*******************************************************************
//
// CProvFactory::CProvFactory
// CProvFactory::~CProvFactory
//
// Constructor Parameters:
//  None
//*******************************************************************

CProvFactory::CProvFactory()
{
    m_cRef=0L;
    return;
}

CProvFactory::~CProvFactory(void)
{
    return;
}

//*******************************************************************
//
// CProvFactory::QueryInterface
// CProvFactory::AddRef
// CProvFactory::Release
//
// Purpose: Standard Ole routines needed for all interfaces
//
//*******************************************************************


STDMETHODIMP CProvFactory::QueryInterface(REFIID riid, PPVOID ppv)
{
    *ppv=NULL;

    if (IID_IUnknown==riid || IID_IClassFactory==riid)
        *ppv=this;

    if (NULL!=*ppv)
        {
        ((LPUNKNOWN)*ppv)->AddRef();
        return NOERROR;
        }

    return E_NOINTERFACE;
}

STDMETHODIMP_(ULONG) CProvFactory::AddRef(void)
{
    return ++m_cRef;
}

STDMETHODIMP_(ULONG) CProvFactory::Release(void)
{
    ULONG nNewCount = InterlockedDecrement((long *)&m_cRef);
    if (0L == nNewCount)
        delete this;
    
    return nNewCount;
}

//*******************************************************************
//
// CProvFactory::CreateInstance
//
// Purpose: Instantiates a Locator object
// and returns an interface pointer.
//
// Parameters:
//  pUnkOuter       LPUNKNOWN to the controlling IUnknown if 
//                  being used in an aggregation.
//  riid            REFIID identifies the interface the caller
//                  desires to have for the new object.
//  ppvObj          PPVOID in which to store the desired
//                  interface pointer for the new object.
//
// Return Value:
//  HRESULT         NOERROR if successful, otherwise E_NOINTERFACE
//                  if you cannot support the requested interface.
//*******************************************************************

STDMETHODIMP CProvFactory::CreateInstance(LPUNKNOWN pUnkOuter, REFIID riid, PPVOID ppvObj)
{
    CInstPro *   pObj;
    HRESULT hr;

    *ppvObj=NULL;

    // This object does not support aggregation.

    if (NULL!=pUnkOuter)
        return CLASS_E_NOAGGREGATION;

    // Create the locator object.
    
    pObj=new CInstPro();
    if (NULL==pObj)
        return E_OUTOFMEMORY;

    hr=pObj->QueryInterface(riid, ppvObj);

    //Kill the object if initial creation or Init failed.

    if (FAILED(hr))
        delete pObj;
    return hr;
}

//*******************************************************************
//
// CProvFactory::LockServer
//
// Purpose:
//  Increments or decrements the lock count of the DLL.  If the
//  lock count goes to zero and there are no objects, the DLL
//  is allowed to unload.  See DllCanUnloadNow.
//
// Parameters:
//  fLock           BOOL specifying whether to increment or
//                  decrement the lock count.
//
// Return Value:
//  HRESULT         NOERROR always.
//*******************************************************************


STDMETHODIMP CProvFactory::LockServer(BOOL fLock)
{
    if (fLock)
        InterlockedIncrement(&g_cLock);
    else
        InterlockedDecrement(&g_cLock);
    return NOERROR;
}
```



Il file di origine Maindll.cpp contiene codice che controlla quando la DLL può essere scaricata verificando il numero di oggetti e blocchi, nonché le routine che supportano la registrazione automatica.


```C++
//*******************************************************************
//  MAINDLL.CPP
//  Module: WMI Instance provider sample code
//  Purpose: Contains DLL entry points.  Also has code that controls
//           when the DLL can be unloaded by tracking the number of
//           objects and locks as well as routines that support
//           self registration.
//
// Copyright (C) Microsoft. All Rights Reserved.
//
//*******************************************************************

#include <objbase.h>
#include <initguid.h>
#include <strsafe.h>

#include "sample.h"

HMODULE ghModule;

// TODO, GuidGen should be used to generate a unique number for any 
// providers that are going to be used for anything more extensive 
// than just testing.

DEFINE_GUID(CLSID_instprovider, 0x22cb8761, 0x914a, 0x11cf, 0xb7, 0x5, 0x0, 0xaa, 0x0, 0x62, 0xcb, 0xb7);
// {22CB8761-914A-11cf-B705-00AA0062CBB7}

//Count number of objects and number of locks.

long       g_cObj=0;
long       g_cLock=0;

//*******************************************************************
//
// LibMain32
//
// Purpose: Entry point for DLL.
//
// Return: TRUE if OK.
//
//*******************************************************************


BOOL WINAPI LibMain32(HINSTANCE hInstance, ULONG ulReason, LPVOID pvReserved)
{
    if (DLL_PROCESS_ATTACH==ulReason)
        ghModule = hInstance;
    return TRUE;
}

//*******************************************************************
//
//  DllGetClassObject
//
//  Purpose: Called by Ole when some client wants a class factory.
//           Return one only if it is the sort of
//           class this DLL supports.
//
//*******************************************************************


STDAPI DllGetClassObject(REFCLSID rclsid, REFIID riid, PPVOID ppv)
{
    HRESULT hr;
    CProvFactory *pObj;

    if (CLSID_instprovider!=rclsid)
        return E_FAIL;

    pObj=new CProvFactory();

    if (NULL==pObj)
        return E_OUTOFMEMORY;

    hr=pObj->QueryInterface(riid, ppv);

    if (FAILED(hr))
        delete pObj;

    return hr;
}

//*******************************************************************
//
// DllCanUnloadNow
//
// Purpose: Called periodically by Ole to determine if the
//          DLL can be freed.
//
// Return:  S_OK if there are no objects in use and the class factory 
//          is not locked.
//
//*******************************************************************

STDAPI DllCanUnloadNow(void)
{
    SCODE   sc;

    //It is OK to unload if there are no objects or locks on the 
    // class factory.
    
    sc=(0L==g_cObj && 0L==g_cLock) ? S_OK : S_FALSE;
    return sc;
}

//*******************************************************************
//
// DllRegisterServer
//
// Purpose: Called during setup or by regsvr32.
//
// Return:  NOERROR if registration successful, error otherwise.
//*******************************************************************

STDAPI DllRegisterServer(void)
{   
    char       szID[128];
    WCHAR      wcID[128];
    char       szCLSID[128];
    TCHAR       szModule[MAX_PATH + 1];
    const char * pName = "WMI Sample Instance Provider";
    const char * pModel = "Both";
    HKEY hKey1, hKey2;


    // Create the path.

    memset(wcID, NULL, sizeof(wcID));
    memset(szID, NULL, sizeof(szID)); 
    StringFromGUID2(CLSID_instprovider, wcID, sizeof(wcID)/sizeof(WCHAR));
    wcstombs(szID, wcID, sizeof(szID)); 
    StringCbCopy(szCLSID, sizeof(szCLSID), "Software\\classes\\CLSID\\");
    StringCbCat(szCLSID, sizeof(szCLSID), (LPCTSTR)szID);

    // Create entries under CLSID

    LONG lRet = RegCreateKeyEx( HKEY_LOCAL_MACHINE, 
                                szCLSID, 
                                0, 
                                NULL,
                                REG_OPTION_NON_VOLATILE, 
                                KEY_WRITE, 
                                NULL, 
                                &hKey1, 
                                NULL );
    if (lRet != ERROR_SUCCESS)
    {
        return E_FAIL;
    }

    lRet = RegSetValueEx(hKey1, NULL, 0, REG_SZ, (BYTE *)pName, strlen(pName)+1);
    if (lRet != ERROR_SUCCESS)
    {
        RegCloseKey(hKey1);
        return E_FAIL;
    }

    lRet = RegCreateKeyEx( hKey1, "InprocServer32", 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey2, NULL );
    if (lRet != ERROR_SUCCESS)
    {
        RegCloseKey(hKey1);
        return E_FAIL;
    }

    memset(&szModule, NULL, sizeof(szModule));
    GetModuleFileName(ghModule, szModule, sizeof(szModule)/sizeof(TCHAR) - 1);

    lRet = RegSetValueEx(hKey2, NULL, 0, REG_SZ, (BYTE *)szModule, strlen(szModule)+1);
    if (lRet != ERROR_SUCCESS)
    {
        RegCloseKey(hKey2);
        RegCloseKey(hKey1);
        return E_FAIL;
    }
    
    lRet = RegSetValueEx(hKey2, "ThreadingModel", 0, REG_SZ, (BYTE *)pModel, strlen(pModel)+1);
    if (lRet != ERROR_SUCCESS)
    {
        RegCloseKey(hKey2);
        RegCloseKey(hKey1);
        return E_FAIL;
    }
    RegCloseKey(hKey1);
    RegCloseKey(hKey2);
    return NOERROR;
}

//*******************************************************************
//
// DllUnregisterServer
//
// Purpose: Called when it is time to remove the registry entries.
//
// Return:  NOERROR if registration successful, error otherwise.
//*******************************************************************

STDAPI DllUnregisterServer(void)
{
    TCHAR szID[128];
    WCHAR wcID[128];
    TCHAR szCLSID[128];
    HKEY hKey;

    // Create the path using the CLSID

    memset(wcID, NULL, sizeof(wcID));
    memset(szID, NULL, sizeof(szID)); 
    StringFromGUID2(CLSID_instprovider, wcID, sizeof(wcID)/sizeof(WCHAR));
    wcstombs(szID, wcID, sizeof(szID)); 
    StringCbCopy(szCLSID, sizeof(szCLSID), "Software\\classes\\CLSID\\");
    StringCbCat(szCLSID, sizeof(szCLSID), (LPCTSTR)szID);


    // First delete the InProcServer subkey.

    DWORD dwRet = RegOpenKeyEx(HKEY_LOCAL_MACHINE, szCLSID, 0, KEY_WRITE, &hKey);
    if(dwRet == NO_ERROR)
    {
        RegDeleteKey(hKey, "InProcServer32");
        RegCloseKey(hKey);
    }

    dwRet = RegOpenKeyEx(HKEY_LOCAL_MACHINE, "Software\\classes\\CLSID", 0, KEY_WRITE, &hKey);
    if(dwRet == NO_ERROR)
    {
        RegDeleteKey(hKey,szID);
        RegCloseKey(hKey);
    }

    return NOERROR;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dei descrittori di sicurezza namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
