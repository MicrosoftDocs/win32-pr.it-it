---
title: Interfaccia IADsExtension
description: Questo argomento contiene esempi di codice C++ per l'uso dell'interfaccia IADsExtension.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI, utilizzo
- ADSI ADSI, codice di esempio C/C++, uso di IADsExtension
- estensioni ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730226"
---
# <a name="iadsextension-interface"></a><span data-ttu-id="0db52-106">Interfaccia IADsExtension</span><span class="sxs-lookup"><span data-stu-id="0db52-106">IADsExtension Interface</span></span>

<span data-ttu-id="0db52-107">L'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="0db52-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



<span data-ttu-id="0db52-108">Aggregator (ADSI) chiama il metodo [**IADsExtension:: opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .</span><span class="sxs-lookup"><span data-stu-id="0db52-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="0db52-109">L'estensione deve interpretare il parametro *dwCode* e ogni parametro *vardata* , in base alla documentazione del provider.</span><span class="sxs-lookup"><span data-stu-id="0db52-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="0db52-110">Aggregator (ADSI), chiama il metodo [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="0db52-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="0db52-111">Viene chiamato dopo che ADSI determina l'estensione per la distribuzione del servizio.</span><span class="sxs-lookup"><span data-stu-id="0db52-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="0db52-112">L'estensione può usare le informazioni sul tipo per ottenere il DISPID, ovvero usando la funzione [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="0db52-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="0db52-113">ADSI chiama in genere il metodo [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) dopo aver chiamato la funzione [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="0db52-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="0db52-114">L'estensione deve chiamare il metodo effettivo che implementa.</span><span class="sxs-lookup"><span data-stu-id="0db52-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="0db52-115">In alternativa, l'estensione può usare le informazioni sul tipo e chiamare la funzione [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .</span><span class="sxs-lookup"><span data-stu-id="0db52-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="0db52-116">Tutti i parametri hanno lo stesso significato dei parametri nel metodo [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) standard.</span><span class="sxs-lookup"><span data-stu-id="0db52-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 