---
description: Questa sezione illustra come recuperare il markup MathML dal controllo di input matematico usando il Active Template Library (ATL) e il Component Object Model (COM).
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Ricezione di input dal controllo Math input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317915"
---
# <a name="receiving-input-from-the-math-input-control"></a><span data-ttu-id="7f90d-103">Ricezione di input dal controllo Math input</span><span class="sxs-lookup"><span data-stu-id="7f90d-103">Receiving Input from the Math Input Control</span></span>

<span data-ttu-id="7f90d-104">Questa sezione illustra come recuperare il markup MathML dal controllo di input matematico usando il Active Template Library (ATL) e il Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="7f90d-104">This section explains how to retrieve the MathML markup from the math input control using the Active Template Library (ATL) and the Component Object Model (COM).</span></span>

<span data-ttu-id="7f90d-105">Per recuperare l'equazione matematica riconosciuta dal controllo di input matematico, è possibile eseguire l'override del comportamento che si verifica quando viene premuto il pulsante di inserimento.</span><span class="sxs-lookup"><span data-stu-id="7f90d-105">To retrieve the recognized math equation from the math input control, you can override the behavior that happens when the insert button is pressed.</span></span> <span data-ttu-id="7f90d-106">A tale scopo, sarà necessario configurare un gestore eventi che implementi i vari eventi supportati dall'interfaccia [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) .</span><span class="sxs-lookup"><span data-stu-id="7f90d-106">To do this, you will need to set up an event handler that implements the various events that are supported by the [**\_IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) interface.</span></span> <span data-ttu-id="7f90d-107">La configurazione del gestore eventi prevede l'esecuzione dei passaggi seguenti per gli eventi che si desidera supportare (inserire in questo caso).</span><span class="sxs-lookup"><span data-stu-id="7f90d-107">Setting up the events handler involves the performing the following steps for the events you want to support (insert in this case).</span></span>

-   [<span data-ttu-id="7f90d-108">Creare una classe modello che contiene sink di evento</span><span class="sxs-lookup"><span data-stu-id="7f90d-108">Create a template class that contains event sinks</span></span>](#create-a-template-class-that-contains-event-sinks)
-   [<span data-ttu-id="7f90d-109">Configurare i gestori eventi</span><span class="sxs-lookup"><span data-stu-id="7f90d-109">Set up the event handlers</span></span>](#set-up-the-event-handlers)
-   [<span data-ttu-id="7f90d-110">Ereditare la classe del gestore eventi nella classe principale</span><span class="sxs-lookup"><span data-stu-id="7f90d-110">Inherit the event handler class in your main class</span></span>](#inherit-the-event-handler-class-in-your-main-class)
-   [<span data-ttu-id="7f90d-111">Inizializzare la classe per ereditare i sink di evento</span><span class="sxs-lookup"><span data-stu-id="7f90d-111">Initialize your class to inherit the event sink(s)</span></span>](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a><span data-ttu-id="7f90d-112">Creare una classe modello che contiene sink di evento</span><span class="sxs-lookup"><span data-stu-id="7f90d-112">Create a template class that contains event sinks</span></span>

<span data-ttu-id="7f90d-113">Quando si implementa un sink di evento che utilizza il controllo di input matematico, è necessario innanzitutto specificare un ID sink. È quindi necessario creare una classe modello che erediti dall'evento, dal gestore del controllo eventi e dalle interfacce eventi del controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="7f90d-113">When you are implementing an event sink that uses the math input control, you must first specify a sink id. You must then create a template class that inherits from the event, event control handler, and math input control event interfaces.</span></span> <span data-ttu-id="7f90d-114">Il codice seguente illustra come impostare un ID sink e creare una classe modello, CMathInputControlEventHandler, che eredita dalle interfacce necessarie.</span><span class="sxs-lookup"><span data-stu-id="7f90d-114">The following code shows how to set a sink id and create such a template class, CMathInputControlEventHandler, that inherits from the requisite interfaces.</span></span> <span data-ttu-id="7f90d-115">Questa classe modello viene anche configurata in modo da avere un puntatore a interfaccia sconosciuto privato che verrà usato per passare il controllo di input matematico all'inizializzazione e il \_ membro ulAdviseCount di m per conteggiare il numero di chiamate a advise/Unadvise.</span><span class="sxs-lookup"><span data-stu-id="7f90d-115">This template class also is set up to have a private unknown interface pointer that will be used to pass the math input control to it on initialization and the m\_ulAdviseCount member to count the number of calls to advise / unadvise.</span></span>


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> <span data-ttu-id="7f90d-116">Se non si usa una finestra di dialogo, il membro **m \_ pMain** dovrebbe essere diverso nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7f90d-116">The member **m\_pMain** should be different in your implementation if you are not using a dialog.</span></span>

 

<span data-ttu-id="7f90d-117">Ora che si dispone della classe modello di base, è necessario fornire una dichiarazione con i gestori di eventi di cui verrà eseguito l'override, quindi impostare una mappa di sink per gli eventi da gestire.</span><span class="sxs-lookup"><span data-stu-id="7f90d-117">Now that you have the basic template class, you must give a forward declaration for the event handlers that you will be overriding and must then set up a sink map for the events you will be handling.</span></span> <span data-ttu-id="7f90d-118">Nel codice seguente viene illustrato come impostare i gestori eventi per il metodo [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , chiamati quando un utente fa clic sul pulsante di inserimento nel controllo di input matematico e il metodo [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , chiamato quando un utente fa clic sul pulsante Annulla nel controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="7f90d-118">The following code shows how to set up event handlers for the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) method, called when a user clicks the insert button on the math input control, and the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) method, called when a user clicks the cancel button on the math input control.</span></span>


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



<span data-ttu-id="7f90d-119">Poiché si lavorerà con il controllo di input matematico, sarà utile impostare un riferimento interno all'interfaccia pertinente.</span><span class="sxs-lookup"><span data-stu-id="7f90d-119">Since you will be working with the math input control, it will be useful to set an internal reference to the relevant interface.</span></span> <span data-ttu-id="7f90d-120">Nella classe di esempio viene creata la funzione di utilità seguente per impostare il riferimento.</span><span class="sxs-lookup"><span data-stu-id="7f90d-120">The following utility function is created in the example class to set this reference.</span></span>


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a><span data-ttu-id="7f90d-121">Configurare i gestori eventi</span><span class="sxs-lookup"><span data-stu-id="7f90d-121">Set up the event handlers</span></span>

<span data-ttu-id="7f90d-122">Dopo aver configurato i sink di evento, sarà necessario creare le implementazioni dei sink di evento.</span><span class="sxs-lookup"><span data-stu-id="7f90d-122">Once you have set up the event sinks, you will need to create your implementations of the event sinks.</span></span> <span data-ttu-id="7f90d-123">In entrambi i metodi nell'esempio di codice seguente, i sink di evento recuperano un handle per l'interfaccia di controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="7f90d-123">In both of the methods in the following code example, the event sinks retrieve a handle to the math input control interface.</span></span> <span data-ttu-id="7f90d-124">Nella funzione [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) il risultato del riconoscimento viene visualizzato come MathML e il controllo è nascosto.</span><span class="sxs-lookup"><span data-stu-id="7f90d-124">In the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) function, the recognition result is displayed as MathML and the control is hidden.</span></span> <span data-ttu-id="7f90d-125">Nella funzione [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) il controllo di input matematico è nascosto.</span><span class="sxs-lookup"><span data-stu-id="7f90d-125">In the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) function, the math input control is hidden.</span></span>


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a><span data-ttu-id="7f90d-126">Ereditare la classe del gestore eventi nella classe principale</span><span class="sxs-lookup"><span data-stu-id="7f90d-126">Inherit the event handler class in your main class</span></span>

<span data-ttu-id="7f90d-127">Dopo che la classe modello è stata implementata, sarà necessario ereditarla nella classe in cui verrà configurato il controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="7f90d-127">After you have your template class implemented, you will need to inherit it into the class that you will be setting up your math input control in.</span></span> <span data-ttu-id="7f90d-128">Ai fini di questa guida, questa classe è una finestra di dialogo, CMIC \_ test \_ EVENTSDlg.</span><span class="sxs-lookup"><span data-stu-id="7f90d-128">For the purposes of this guide, this class is a dialog, CMIC\_TEST\_EVENTSDlg.</span></span> <span data-ttu-id="7f90d-129">Nell'intestazione della finestra di dialogo è necessario includere le intestazioni necessarie e la classe modello creata deve essere ereditata.</span><span class="sxs-lookup"><span data-stu-id="7f90d-129">In the dialog header, the requisite headers must be included and the template class you created must be inherited.</span></span> <span data-ttu-id="7f90d-130">La classe in cui si sta ereditando e i gestori di eventi devono avere dichiarazioni con esecuzione in modo che il modello possa essere implementato.</span><span class="sxs-lookup"><span data-stu-id="7f90d-130">The class you're inheriting within and the event handlers must have forward declarations so that the template can be implemented.</span></span> <span data-ttu-id="7f90d-131">Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7f90d-131">The following code example shows how this is done.</span></span>


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> <span data-ttu-id="7f90d-132">Il tipo di modello, **CMIC \_ test \_ EventsDlg**, sarà diverso a meno che non sia stata denominata la classe uguale a quella dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="7f90d-132">The template type, **CMIC\_TEST\_EventsDlg**, will be different unless you have named your class the same as the example.</span></span>

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a><span data-ttu-id="7f90d-133">Inizializzare la classe per ereditare i sink di evento</span><span class="sxs-lookup"><span data-stu-id="7f90d-133">Initialize your class to inherit the event sink(s)</span></span>

<span data-ttu-id="7f90d-134">Dopo aver configurato la classe in modo che erediti dalla classe modello, è possibile configurarla per la gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="7f90d-134">Once you have set up your class to inherit from the template class, you are ready to set it up to handle events.</span></span> <span data-ttu-id="7f90d-135">Questa operazione consiste nell'inizializzazione della classe in modo che disponga di un handle per il controllo di input matematico e della classe chiamante.</span><span class="sxs-lookup"><span data-stu-id="7f90d-135">This will consist of initializing the class to have a handle to the math input control and the calling class.</span></span> <span data-ttu-id="7f90d-136">Inoltre, il controllo di input matematico per la gestione degli eventi da deve essere inviato al metodo DispEventAdvise ereditato dalla classe di esempio CMathInputControlEventHandler.</span><span class="sxs-lookup"><span data-stu-id="7f90d-136">Additionally, the math input control to handle events from must be sent to the DispEventAdvise method that the CMathInputControlEventHandler example class inherits.</span></span> <span data-ttu-id="7f90d-137">Il codice seguente viene chiamato dal metodo OnInitDialog nella classe Example per eseguire queste azioni.</span><span class="sxs-lookup"><span data-stu-id="7f90d-137">The following code is called from the OnInitDialog method in the example class to perform these actions.</span></span>


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> <span data-ttu-id="7f90d-138">Il tipo di modello, CMIC \_ test \_ EventsDlg in questo esempio, sarà diverso a meno che la classe non sia stata denominata come l'esempio.</span><span class="sxs-lookup"><span data-stu-id="7f90d-138">The template type, CMIC\_TEST\_EventsDlg in this example, will be different unless you have named your class the same as the example.</span></span>

 

 

 
