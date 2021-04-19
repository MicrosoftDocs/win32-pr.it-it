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
# <a name="receiving-input-from-the-math-input-control"></a>Ricezione di input dal controllo Math input

Questa sezione illustra come recuperare il markup MathML dal controllo di input matematico usando il Active Template Library (ATL) e il Component Object Model (COM).

Per recuperare l'equazione matematica riconosciuta dal controllo di input matematico, è possibile eseguire l'override del comportamento che si verifica quando viene premuto il pulsante di inserimento. A tale scopo, sarà necessario configurare un gestore eventi che implementi i vari eventi supportati dall'interfaccia [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) . La configurazione del gestore eventi prevede l'esecuzione dei passaggi seguenti per gli eventi che si desidera supportare (inserire in questo caso).

-   [Creare una classe modello che contiene sink di evento](#create-a-template-class-that-contains-event-sinks)
-   [Configurare i gestori eventi](#set-up-the-event-handlers)
-   [Ereditare la classe del gestore eventi nella classe principale](#inherit-the-event-handler-class-in-your-main-class)
-   [Inizializzare la classe per ereditare i sink di evento](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Creare una classe modello che contiene sink di evento

Quando si implementa un sink di evento che utilizza il controllo di input matematico, è necessario innanzitutto specificare un ID sink. È quindi necessario creare una classe modello che erediti dall'evento, dal gestore del controllo eventi e dalle interfacce eventi del controllo di input matematico. Il codice seguente illustra come impostare un ID sink e creare una classe modello, CMathInputControlEventHandler, che eredita dalle interfacce necessarie. Questa classe modello viene anche configurata in modo da avere un puntatore a interfaccia sconosciuto privato che verrà usato per passare il controllo di input matematico all'inizializzazione e il \_ membro ulAdviseCount di m per conteggiare il numero di chiamate a advise/Unadvise.


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
> Se non si usa una finestra di dialogo, il membro **m \_ pMain** dovrebbe essere diverso nell'implementazione.

 

Ora che si dispone della classe modello di base, è necessario fornire una dichiarazione con i gestori di eventi di cui verrà eseguito l'override, quindi impostare una mappa di sink per gli eventi da gestire. Nel codice seguente viene illustrato come impostare i gestori eventi per il metodo [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , chiamati quando un utente fa clic sul pulsante di inserimento nel controllo di input matematico e il metodo [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , chiamato quando un utente fa clic sul pulsante Annulla nel controllo di input matematico.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Poiché si lavorerà con il controllo di input matematico, sarà utile impostare un riferimento interno all'interfaccia pertinente. Nella classe di esempio viene creata la funzione di utilità seguente per impostare il riferimento.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Configurare i gestori eventi

Dopo aver configurato i sink di evento, sarà necessario creare le implementazioni dei sink di evento. In entrambi i metodi nell'esempio di codice seguente, i sink di evento recuperano un handle per l'interfaccia di controllo di input matematico. Nella funzione [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) il risultato del riconoscimento viene visualizzato come MathML e il controllo è nascosto. Nella funzione [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) il controllo di input matematico è nascosto.


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



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>Ereditare la classe del gestore eventi nella classe principale

Dopo che la classe modello è stata implementata, sarà necessario ereditarla nella classe in cui verrà configurato il controllo di input matematico. Ai fini di questa guida, questa classe è una finestra di dialogo, CMIC \_ test \_ EVENTSDlg. Nell'intestazione della finestra di dialogo è necessario includere le intestazioni necessarie e la classe modello creata deve essere ereditata. La classe in cui si sta ereditando e i gestori di eventi devono avere dichiarazioni con esecuzione in modo che il modello possa essere implementato. Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.


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
> Il tipo di modello, **CMIC \_ test \_ EventsDlg**, sarà diverso a meno che non sia stata denominata la classe uguale a quella dell'esempio.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Inizializzare la classe per ereditare i sink di evento

Dopo aver configurato la classe in modo che erediti dalla classe modello, è possibile configurarla per la gestione degli eventi. Questa operazione consiste nell'inizializzazione della classe in modo che disponga di un handle per il controllo di input matematico e della classe chiamante. Inoltre, il controllo di input matematico per la gestione degli eventi da deve essere inviato al metodo DispEventAdvise ereditato dalla classe di esempio CMathInputControlEventHandler. Il codice seguente viene chiamato dal metodo OnInitDialog nella classe Example per eseguire queste azioni.


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
> Il tipo di modello, CMIC \_ test \_ EventsDlg in questo esempio, sarà diverso a meno che la classe non sia stata denominata come l'esempio.

 

 

 
