---
title: Esempio di manipolazione e inerzia
description: L'esempio Manipulation and Inertia illustra come aggiungere il supporto Windows Touch alle applicazioni native basate su Windows che usano l'API Windows Touch.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows Tocco, esempi di codice
- Windows Tocco, codice di esempio
- Windows Tocco, manipolazioni
- Windows Tocco, inerzia
- Windows Esempio di tocco, manipolazione e inerzia
- Esempio di manipolazione e inerzia
- Windows Interfaccia touch,_IManipulationEventSink
- Windows Interfaccia Touch,IManipulationProcessor
- Windows Interfaccia Touch,IInertiaProcessor
- manipolazioni, codice di esempio
- manipolazioni, esempi di codice
- manipolazioni, _IManipulationEventSink interfaccia
- manipolazioni, interfaccia IManipulationProcessor
- inerzia, codice di esempio
- inerzia, esempi di codice
- inerzia, interfaccia IInertiaProcessor
- _IManipulationEventSink interfaccia
- Interfaccia IManipulationProcessor, esempi di codice
- Interfaccia IManipulationProcessor, codice di esempio
- Interfaccia IInertiaProcessor, esempi di codice
- Interfaccia IInertiaProcessor, codice di esempio
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 8b6471362d30b6efc9dfa0c4f07df70f014c8cb72866c92bbb04c9eb33463410
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840596"
---
# <a name="manipulation-and-inertia-sample"></a>Esempio di manipolazione e inerzia

L'esempio Manipulation and Inertia illustra come aggiungere il supporto Windows Touch alle applicazioni native basate su Windows che usano l'API Windows Touch. L'esempio implementa le funzionalità di base dell'API per abilitare la conversione, la rotazione e il ridimensionamento per gli oggetti e l'applicazione di proprietà di inerzia. L'esempio illustra anche come fornire alle applicazioni touch Windows supporto del mouse di base. L'immagine seguente mostra l'aspetto dell'esempio durante l'esecuzione.

![Screenshot che mostra due caselle con sfumature nell'esempio di manipolazione e inerzia](images/manip-inertia-sample.png)

Le caselle con sfumature possono essere manipolate in modo indipendente da un utente quando eseguono l'applicazione da un computer che supporta Windows Touch.

## <a name="register-the-touch-window"></a>Registrare la finestra touch

Prima di poter ricevere l'input tocco, è necessario notificare al sistema che l'applicazione è un'applicazione Windows Touch chiamando la funzione seguente:

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a>Implementare l'interfaccia _IManipulationEventSink

[**L_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink contiene tre funzioni: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted). Queste funzioni di callback vengono usate [**dall'interfaccia IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e [**dall'interfaccia IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) per restituire i valori calcolati dai processori dopo aver richiamato le funzioni [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)e [**ProcessMoveWithTime.**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) Nell'esempio di codice seguente viene illustrata un'implementazione di esempio **di un_IManipulationEvents** interface.

```C++
#include "cmanipulationeventsink.h"
#include <math.h>

CManipulationEventSink::CManipulationEventSink(HWND hWnd, CDrawingObject *dObj, int iTimerId, BOOL inertia) {
    // Manipulation & Inertia Processors
    m_manip = NULL;
    m_inert = NULL;

    // Connection points for COM.
    m_pConPointContainer = NULL;
    m_pConnPoint = NULL;

    // Reference to an object associated with this event sink.
    m_dObj = dObj;

    // Handle to the window used for computing boundaries.
    m_hWnd = hWnd;

    // The unique timer id for this manipulation event sink.
    m_iTimerId = iTimerId;

    m_bInertia = inertia;

    m_cRefCount = 1;
}


CManipulationEventSink::~CManipulationEventSink()
{

}


HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted(
    FLOAT x,
    FLOAT y)
{
    KillTimer(m_hWnd, m_iTimerId);

    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    FLOAT x,
    FLOAT y,
    FLOAT translationDeltaX,
    FLOAT translationDeltaY,
    FLOAT scaleDelta,
    FLOAT expansionDelta,
    FLOAT rotationDelta,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    FLOAT pivot = 0.0f;

    // Apply transformation based on rotationDelta (in radians).
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta.
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta.
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    if(!m_bInertia)
    {
        // Set values for one-finger rotations.
        FLOAT fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->GetWidth()/2, 2)
                           + pow(m_dObj->GetHeight()/2, 2)))*0.4f;
        FLOAT fPivotPtX    = m_dObj->GetCenterX();
        FLOAT fPivotPtY    = m_dObj->GetCenterY();

        m_manip->put_PivotPointX(fPivotPtX);
        m_manip->put_PivotPointY(fPivotPtY);
        m_manip->put_PivotRadius(fPivotRadius);
    }
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted(
    FLOAT x,
    FLOAT y,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    if(!m_bInertia)
    {
        SetupInertia();

        // Kick off timer that handles inertia.
        SetTimer(m_hWnd, m_iTimerId, DESIRED_MILLISECONDS, NULL);
    }
    else
    {
        // Stop timer that handles inertia.
        KillTimer(m_hWnd, m_iTimerId);
    }

    return S_OK;
}
```

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a>Creare oggetti COM e configurare le interfacce IManipulationProcessor e IInertiaProcessor

L'API fornisce un'implementazione [**delle interfacce IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) È necessario creare un'istanza di e fare riferimento agli oggetti COM dal sink di evento [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) implementato in precedenza.

## <a name="handle-wm_touch-messages"></a>Gestire WM_TOUCH messaggi

I dati di input devono [](wm-touchdown.md) essere estratti dai messaggi WM_TOUCH e successivamente devono essere elaborati per alimentare il processore di manipolazione corretto.

```C++
switch (msg)
{
    case WM_TOUCH:

      iNumContacts = LOWORD(wParam);
      hInput       = (HTOUCHINPUT)lParam;
      pInputs      = new TOUCHINPUT[iNumContacts];

      // Get each touch input info and feed each
      // tagTOUCHINPUT into the process input handler.

      if(pInputs != NULL)
      {
          if(GetTouchInputInfo(hInput, iNumContacts,
               pInputs, sizeof(TOUCHINPUT)))
          {
              for(int i = 0; i < iNumContacts; i++)
              {
                  // Bring touch input info into client coordinates.
                  ptInputs.x = pInputs[i].x/100;
                  ptInputs.y = pInputs[i].y/100;
                  ScreenToClient(g_hWnd, &ptInputs);

                  pInputs[i].x = ptInputs.x;
                  pInputs[i].y = ptInputs.y;

                  g_ctDriver->ProcessInputEvent(pInputs[i]);
              }
          }
      }

      delete [] pInputs;
      break;
}
```

> [!Note]  
> Per usare la funzione [**ScreenToClient,**](/windows/desktop/api/winuser/nf-winuser-screentoclient) è necessario avere un supporto DPI elevato nell'applicazione. Per altre informazioni sul supporto di valori DPI elevati, vedere la [sezione High DPI (DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) elevato) di MSDN.

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a>Passare strutture TOUCHINPUT al processore appropriato

Dopo aver estratto i dati dai messaggi [**WM_TOUCH**](wm-touchdown.md) usando la funzione [**GetTouchInputInfo,**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) inviare i dati al processore di manipolazione richiamando le funzioni [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)o [**ProcessMoveWithTime,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) a seconda del **set dwFlag** nella struttura [**TOUCHINPUT.**](/windows/win32/api/winuser/ns-winuser-touchinput)

> [!Note]  
> Quando si supportano più manipolazioni, è necessario creare un nuovo processore di manipolazione se è necessario usare **il dwID** definito nella struttura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) per inviare i dati all'oggetto [**IManipulationProcessor corretto.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)

```C++
CoreObject* coCurrent = m_coHead;

while(coCurrent!=NULL && !bFoundObj)
{
    if(dwEvent & TOUCHEVENTF_DOWN)
    {
        DownEvent(coCurrent, inData, &bFoundObj);
    }
    else if(dwEvent & TOUCHEVENTF_MOVE)
    {
        MoveEvent(coCurrent, inData);
    }
    else if(dwEvent & TOUCHEVENTF_UP)
    {
        UpEvent(coCurrent, inData);
    }
    coCurrent = coCurrent->coNext;
}

VOID CComTouchDriver::DownEvent(CoreObject* coRef, tagTOUCHINPUT inData, BOOL* bFound) {
    DWORD dwPCursor = inData.dwID;
    DWORD dwPTime   = inData.dwTime;
    int x           = inData.x;
    int y           = inData.y;

    // Check that the user has touched within an object's region and fed to the object's manipulation processor.

    if(coRef->doDrawing->InRegion(x, y) &&
        !HasCursor(coRef, dwPCursor))
    {
        ...

        // Feed values to the Manipulation Processor.
        coRef->manipulationProc->ProcessDownWithTime(dwPCursor, (FLOAT)x, (FLOAT)y, dwPTime);

        ...
    }
}
```

## <a name="set-up-inertia-within-manipulationcompleted"></a>Configurare l'inerzia all'interno di ManipulationCompleted

Dopo aver richiamato il metodo [**ManipulationCompleted,**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) l'oggetto [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) deve impostare i valori per l'oggetto [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) collegato a **IManipulationProcessor** per richiamare l'inerzia. Nell'esempio di codice seguente viene illustrato come configurare l'oggetto **IInertiaProcessor** dal metodo **IManipulationProcessor** **ManipulationCompleted**.

```C++
    int iVWidth       = GetSystemMetrics(SM_CXVIRTUALSCREEN);
    int iVHeight      = GetSystemMetrics(SM_CYVIRTUALSCREEN);

    RECT rc;
    GetClientRect(m_hWnd, &rc);
    FLOAT lCWidth     = (FLOAT)rc.right;
    FLOAT lCHeight    = (FLOAT)rc.bottom;

    // Set properties for inertia events.

    // Deceleration for tranlations in pixel / msec^2.
    m_inert->put_DesiredDeceleration(0.001f);

    // Deceleration for rotations in radians / msec^2.
    m_inert->put_DesiredAngularDeceleration(0.00001f);

    // Calculate borders and elastic margin to be set.
    // They are relative to the width and height of the object.

    FLOAT fHOffset = m_dObj->GetWidth()  * 0.5f;
    FLOAT fVOffset = m_dObj->GetHeight() * 0.5f;

    // Elastic margin is in pixels - note that it offsets the boundary.

    FLOAT fHElasticMargin = 25.0f;
    FLOAT fVElasticMargin = 25.0f;

    FLOAT fBoundaryLeft   = fHOffset + fHElasticMargin;
    FLOAT fBoundaryTop    = fVOffset + fVElasticMargin;
    FLOAT fBoundaryRight  = lCWidth - fHOffset - fHElasticMargin;
    FLOAT fBoundaryBottom = lCHeight - fVOffset - fVElasticMargin;

    // Set borders and elastic margin.

    m_inert->put_BoundaryLeft(fBoundaryLeft);
    m_inert->put_BoundaryTop(fBoundaryTop);
    m_inert->put_BoundaryRight(fBoundaryRight);
    m_inert->put_BoundaryBottom(fBoundaryBottom);

    m_inert->put_ElasticMarginLeft(fHElasticMargin);
    m_inert->put_ElasticMarginTop(fVElasticMargin);
    m_inert->put_ElasticMarginRight(fHElasticMargin);
    m_inert->put_ElasticMarginBottom(fVElasticMargin);

    // Set initial origins.

    m_inert->put_InitialOriginX(m_dObj->GetCenterX());
    m_inert->put_InitialOriginY(m_dObj->GetCenterY());

    FLOAT fVX;
    FLOAT fVY;
    FLOAT fVR;

    m_manip->GetVelocityX(&fVX);
    m_manip->GetVelocityY(&fVY);
    m_manip->GetAngularVelocity(&fVR);

    // Set initial velocities for inertia processor.

    m_inert->put_InitialVelocityX(fVX);
    m_inert->put_InitialVelocityY(fVY);
    m_inert->put_InitialAngularVelocity(fVR);
```

## <a name="clean-up-your-com-objects"></a>Pulire gli oggetti COM

Quando l'applicazione viene chiusa, è necessario pulire gli oggetti COM. Il codice seguente illustra come liberare le risorse allocate nell'esempio.

```C++
CComTouchDriver::~CComTouchDriver(VOID) {
    CoreObject* coCurrent = m_coHead;

    // Clean up COM objects.

    while(coCurrent!=NULL)
    {
        coCurrent->inertiaEventSink->Release();
        coCurrent->manipulationEventSink->Release();
        coCurrent->inertiaProc->Release();
        coCurrent->manipulationProc->Release();
        coCurrent = coCurrent->coNext;
    }
}
```

## <a name="related-topics"></a>Argomenti correlati

[Esempio di applicazione di manipolazione multitocchetto,](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp)manipolazione e [inerzia](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp) [Windows touch](windows-touch-samples.md)