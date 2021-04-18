---
description: Questo argomento illustra il codice di esempio per gestire la ricerca e la frequenza delle modifiche, quando si usa la sessione multimediale per la riproduzione.
ms.assetid: 50bf4c05-99c0-4cf0-aaca-8ee717cafd12
title: Ricerca, avanzamento rapido e riproduzione inversa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c42e4ab2bbf5bd3ac1057ce4bb0e09fceddc44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309009"
---
# <a name="seeking-fast-forward-and-reverse-play"></a>Ricerca, avanzamento rapido e riproduzione inversa

Questo argomento illustra il codice di esempio per gestire la ricerca e la frequenza delle modifiche, quando si usa la [sessione multimediale](media-session.md) per la riproduzione.

Quando si usa la sessione multimediale per la riproduzione, un'applicazione può cercare e modificare la velocità di riproduzione come indicato di seguito:

-   Per eseguire la ricerca, chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) e specificare la posizione di ricerca.
-   Per modificare la velocità di riproduzione, usare l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) , come descritto in [controllo della frequenza](rate-control.md).
-   Per ottenere i frame video aggiornati durante la ricerca, impostare la velocità di riproduzione su zero prima di chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). Questa operazione è denominata *pulitura*. (Vedere [come eseguire lo scrubbing](how-to-perform-scrubbing.md)).

Per creare la migliore esperienza utente, tuttavia, è necessario tenere conto dei comportamenti seguenti:

-   La ricerca è asincrona e la sessione multimediale Accoda tutte le richieste di ricerca su una coda FIFO. Se si inviano più richieste di ricerca, è possibile che l'interfaccia utente venga eseguita in anticipo rispetto allo stato di riproduzione effettivo. Si supponga, ad esempio, che l'applicazione implementi una barra di ricerca. Se l'utente trascina la barra di ricerca in avanti e indietro, potrebbe essersi verificato un ritardo durante l'esecuzione delle ricerche in avanti. Mentre è in corso una ricerca, è necessario memorizzare nella cache le richieste di ricerca dell'utente. Al termine dell'operazione di ricerca corrente, inviare la richiesta di ricerca più recente dell'utente e rimuovere gli altri.
-   Alcune transizioni di frequenza non sono consentite in alcuni Stati di trasporto. Ad esempio, il cambio dalla riproduzione in diretta alla riproduzione inversa non è consentito durante la riproduzione. Le transizioni supportate sono descritte in [**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate). Anche le modifiche di frequenza sono asincrone.

La classe helper seguente può essere utilizzata per gestire le richieste di ricerca e la frequenza delle modifiche. Mentre un'operazione asincrona è in sospeso, la classe memorizza nella cache qualsiasi richiesta di ricerca o di modifica della frequenza. Al termine dell'operazione corrente, la classe Invia la richiesta più recente, se disponibile. La classe gestisce anche lo stato del trasporto per evitare modifiche di frequenza non valide.

Di seguito è illustrata la dichiarazione della classe PlayerSeeking.


```C++
// Implements seeking and rate control functionality.

/*
    Usage:

    - Call SetTopology when you get the MF_TOPOSTATUS_READY session event.
    - Call SessionEvent for each session event.
    - Call Clear before closing the Media Session.
    - To coordinate rate-change requests with transport state, delegate all 
      stop, pause, and play commands to the PlayerSeeking class.

*/

class PlayerSeeking 
{
    class CritSec
    {
    private:
        CRITICAL_SECTION m_criticalSection;
    public:
        CritSec()
        {
            InitializeCriticalSection(&m_criticalSection);
        }
        ~CritSec()
        {
            DeleteCriticalSection(&m_criticalSection);
        }
        void Lock()
        {
            EnterCriticalSection(&m_criticalSection);
        }
        void Unlock()
        {
            LeaveCriticalSection(&m_criticalSection);
        }
    };

    class AutoLock
    {
    private:
        CritSec *m_pCriticalSection;
    public:
        AutoLock(CritSec& crit)
        {
            m_pCriticalSection = &crit;
            m_pCriticalSection->Lock();
        }
        ~AutoLock()
        {
            m_pCriticalSection->Unlock();
        }
    };

public:

    PlayerSeeking();
    virtual ~PlayerSeeking();

    HRESULT SetTopology(IMFMediaSession *pSession, IMFTopology *pTopology);
    HRESULT Clear();
    HRESULT SessionEvent(MediaEventType type, HRESULT hrStatus, IMFMediaEvent *pEvent);

    HRESULT CanSeek(BOOL *pbCanSeek);
    HRESULT GetDuration(MFTIME *phnsDuration);
    HRESULT GetCurrentPosition(MFTIME *phnsPosition);
    HRESULT SetPosition(MFTIME hnsPosition);

    HRESULT CanScrub(BOOL *pbCanScrub);
    HRESULT Scrub(BOOL bScrub);

    HRESULT CanFastForward(BOOL *pbCanFF);
    HRESULT CanRewind(BOOL *pbCanRewind);
    HRESULT SetRate(float fRate);
    HRESULT FastForward();
    HRESULT Rewind();

    HRESULT Start();
    HRESULT Pause();
    HRESULT Stop();

private:

    enum Command
    {
        CmdNone = 0,
        CmdStop,
        CmdStart,
        CmdPause,
        CmdSeek,
    };

    HRESULT SetPositionInternal(const MFTIME &hnsPosition);
    HRESULT CommitRateChange(float fRate, BOOL bThin);
    float   GetNominalRate();

    HRESULT OnSessionStart(HRESULT hr);
    HRESULT OnSessionStop(HRESULT hr);
    HRESULT OnSessionPause(HRESULT hr);
    HRESULT OnSessionEnded(HRESULT hr);

    HRESULT UpdatePendingCommands(Command cmd);

private:

    // Describes the current or requested state, with respect to seeking and 
    // playback rate.
    struct SeekState
    {
        Command command;
        float   fRate;      // Playback rate
        BOOL    bThin;      // Thinned playback?
        MFTIME  hnsStart;   // Start position
    };

    BOOL        m_bPending;     // Is a request pending?

    SeekState   m_state;        // Current nominal state.
    SeekState   m_request;      // Pending request.

    CritSec     m_critsec;      // Protects the seeking and rate-change states.

    DWORD       m_caps;         // Session caps.
    BOOL        m_bCanScrub;    // Does the current session support rate = 0.

    MFTIME      m_hnsDuration;  // Duration of the current presentation.
    float       m_fPrevRate;

    IMFMediaSession         *m_pSession;
    IMFRateControl          *m_pRate;
    IMFRateSupport          *m_pRateSupport;
    IMFPresentationClock    *m_pClock;
};
```



Di seguito è illustrata l'implementazione della classe PlayerSeeking.


```C++
#include <assert.h>
#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mferror.h>
#include "seeking.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

#define CMD_PENDING      0x01
#define CMD_PENDING_SEEK 0x02
#define CMD_PENDING_RATE 0x04

// Given a topology, returns a pointer to the presentation descriptor.

HRESULT GetPresentationDescriptorFromTopology(
    IMFTopology *pTopology,
    IMFPresentationDescriptor **ppPD
    )
{
    HRESULT hr = S_OK;

    IMFCollection *pCollection = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;
    IMFPresentationDescriptor *pPD = NULL;

    // Get the collection of source nodes from the topology.
    hr = pTopology->GetSourceNodeCollection(&pCollection);
    if (FAILED(hr))
    {
        goto done;
    }

    // Any of the source nodes should have the PD, so take the first
    // object in the collection.

    hr = pCollection->GetElement(0, &pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pUnk->QueryInterface(IID_PPV_ARGS(&pNode));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the PD, which is stored as an attribute.
    hr = pNode->GetUnknown(
        MF_TOPONODE_PRESENTATION_DESCRIPTOR, IID_PPV_ARGS(&pPD));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppPD = pPD;
    (*ppPD)->AddRef();

done:
    SafeRelease(&pCollection);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    SafeRelease(&pPD);
    return hr;
}


PlayerSeeking::PlayerSeeking()
    : m_pClock(NULL),
      m_pSession(NULL),
      m_pRate(NULL),
      m_pRateSupport(NULL),
      m_bPending(FALSE)
{
    Clear();
}

PlayerSeeking::~PlayerSeeking()
{
    SafeRelease(&m_pClock);
    SafeRelease(&m_pSession);
    SafeRelease(&m_pRate);
    SafeRelease(&m_pRateSupport);
}

// Clears any resources for the current topology.

HRESULT PlayerSeeking::Clear()
{
    m_caps = 0;
    m_bCanScrub = FALSE;

    m_hnsDuration = 0;
    m_fPrevRate = 1.0f;

    m_bPending = FALSE;

    SafeRelease(&m_pClock);
    SafeRelease(&m_pSession);
    SafeRelease(&m_pRate);
    SafeRelease(&m_pRateSupport);

    ZeroMemory(&m_state, sizeof(m_state));
    m_state.command = CmdStop;
    m_state.fRate = 1.0f;

    ZeroMemory(&m_request, sizeof(m_request));
    m_request.command = CmdNone;
    m_request.fRate = 1.0f;

    return S_OK;
}


// Call when the full playback topology is ready.

HRESULT PlayerSeeking::SetTopology(IMFMediaSession *pSession, IMFTopology *pTopology)
{
    HRESULT hr = S_OK;
    HRESULT hrTmp = S_OK;   // For non-critical failures.

    IMFClock *pClock = NULL;
    IMFPresentationDescriptor *pPD = NULL;

    Clear();

    // Get the session capabilities.
    hr = pSession->GetSessionCapabilities(&m_caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the presentation descriptor from the topology.
    hr = GetPresentationDescriptorFromTopology(pTopology, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the duration from the presentation descriptor (optional)
    (void)pPD->GetUINT64(MF_PD_DURATION, (UINT64*)&m_hnsDuration);

    // Get the presentation clock (optional)
    hrTmp = pSession->GetClock(&pClock);
    if (SUCCEEDED(hrTmp))
    {
        hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the rate control interface (optional)
    hrTmp = MFGetService(
        pSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&m_pRate));

    // Get the rate support interface (optional)
    if (SUCCEEDED(hrTmp))
    {
        hrTmp = MFGetService(
            pSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&m_pRateSupport));
    }
    if (SUCCEEDED(hrTmp))
    {
        // Check if rate 0 (scrubbing) is supported.
        hrTmp = m_pRateSupport->IsRateSupported(TRUE, 0, NULL);
    }
    if (SUCCEEDED(hrTmp))
    {
        m_bCanScrub = TRUE;
    }

    // if m_pRate is NULL, m_bCanScrub must be FALSE.
    assert(m_pRate || !m_bCanScrub); 

    // Cache a pointer to the session.
    m_pSession = pSession;
    m_pSession->AddRef();

done:
    SafeRelease(&pPD);
    SafeRelease(&pClock);
    return hr;
}

// Call when media session fires an event.

HRESULT PlayerSeeking::SessionEvent(
    MediaEventType type, 
    HRESULT hrStatus, 
    IMFMediaEvent *pEvent
    )
{
    PROPVARIANT var;
    HRESULT hr = S_OK;

    switch (type)
    {
    case MESessionStarted:
        OnSessionStart(hrStatus);
        break;

    case MESessionStopped:
        OnSessionStop(hrStatus);
        break;

    case MESessionPaused:
        OnSessionPause(hrStatus);
        break;

    case MESessionRateChanged:
        // If the rate change succeeded, we've already got the rate
        // cached. If it failed, try to get the actual rate.
        if (FAILED(hrStatus))
        {
            PropVariantInit(&var);

            hr = pEvent->GetValue(&var);

            if (SUCCEEDED(hr) && (var.vt == VT_R4))
            {
                m_state.fRate = var.fltVal;
            }
        }
        break;

    case MESessionEnded:
        OnSessionEnded(hrStatus);
        break;

    case MESessionCapabilitiesChanged:
        // The session capabilities changed. Get the updated capabilities.
        m_caps = MFGetAttributeUINT32(pEvent, MF_EVENT_SESSIONCAPS, m_caps);
        break;
    }
    return S_OK;
}


// Starts playback.

HRESULT PlayerSeeking::Start()
{
    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    // If another operation is pending, cache the request.
    // Otherwise, start the media session.
    if (m_bPending)
    {
       m_request.command = CmdStart;
    }
    else
    {
        PROPVARIANT varStart;
        PropVariantInit(&varStart);

        hr =  m_pSession->Start(NULL, &varStart);

        m_state.command = CmdStart;
        m_bPending = CMD_PENDING;
    }
    return hr;
}


// Pauses playback.

HRESULT PlayerSeeking::Pause()
{
    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    // If another operation is pending, cache the request.
    // Otherwise, pause the media session.
    if (m_bPending)
    {
        m_request.command = CmdPause;
    }
    else
    {
        hr =  m_pSession->Pause();

        m_state.command = CmdPause;
        m_bPending = CMD_PENDING;
    }
    return hr;
}


// Stops playback.

HRESULT PlayerSeeking::Stop()
{
    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    // If another operation is pending, cache the request.
    // Otherwise, stop the media session.
    if (m_bPending)
    {
        m_request.command = CmdStop;
    }
    else
    {
        hr =  m_pSession->Stop();

        m_state.command = CmdStop;
        m_bPending = CMD_PENDING;
    }
    return hr;
}

// Queries whether the current session supports seeking.

HRESULT PlayerSeeking::CanSeek(BOOL *pbCanSeek)
{
    if (pbCanSeek == NULL)
    {
        return E_POINTER;
    }

    // Note: The MFSESSIONCAP_SEEK flag is sufficient for seeking. However, to
    // implement a seek bar, an application also needs the duration (to get 
    // the valid range) and a presentation clock (to get the current position).

    *pbCanSeek = (
        ((m_caps & MFSESSIONCAP_SEEK) == MFSESSIONCAP_SEEK) &&
        (m_hnsDuration > 0) &&
        (m_pClock != NULL)
        );

    return S_OK;
}


// Gets the duration of the current presentation.

HRESULT PlayerSeeking::GetDuration(MFTIME *phnsDuration)
{
    if (phnsDuration == NULL)
    {
        return E_POINTER;
    }

    *phnsDuration = m_hnsDuration;

    if (m_hnsDuration == 0)
    {
        return MF_E_NO_DURATION;
    }
    else
    {
        return S_OK;
    }
}

// Gets the current playback position.

HRESULT PlayerSeeking::GetCurrentPosition(MFTIME *phnsPosition)
{
    if (phnsPosition == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    if (m_pClock == NULL)
    {
        return MF_E_NO_CLOCK;
    }

    // Return, in order:
    // 1. Cached seek request (nominal position).
    // 2. Pending seek operation (nominal position).
    // 3. Presentation time (actual position).

    if (m_request.command == CmdSeek)
    {
        *phnsPosition = m_request.hnsStart;
    }
    else if (m_bPending & CMD_PENDING_SEEK)
    {
        *phnsPosition = m_state.hnsStart;
    }
    else
    {
        hr = m_pClock->GetTime(phnsPosition);
    }

    return hr;
}


// Sets the current playback position.

HRESULT PlayerSeeking::SetPosition(MFTIME hnsPosition)
{
    AutoLock lock(m_critsec);

    HRESULT hr = S_OK;

    if (m_bPending)
    {
        // Currently seeking or changing rates, so cache this request.
        m_request.command = CmdSeek;
        m_request.hnsStart = hnsPosition;
    }
    else
    {
        hr = SetPositionInternal(hnsPosition);
    }

    return hr;
}


// Queries whether the current session supports scrubbing.

HRESULT PlayerSeeking::CanScrub(BOOL *pbCanScrub)
{
    if (pbCanScrub == NULL)
    {
        return E_POINTER;
    }

    *pbCanScrub = m_bCanScrub;
    return S_OK;
}


// Enables or disables scrubbing.

HRESULT PlayerSeeking::Scrub(BOOL bScrub)
{
    // Scrubbing is implemented as rate = 0.

    AutoLock lock(m_critsec);

    if (!m_pRate)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (!m_bCanScrub)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;

    if (bScrub)
    {
        // Enter scrubbing mode. Cache the current rate.

        if (GetNominalRate() != 0)
        {
            m_fPrevRate = m_state.fRate;
        }

        hr = SetRate(0.0f);
    }
    else
    {
        // Leaving scrubbing mode. Restore the old rate.

        if (GetNominalRate() == 0)
        {
            hr = SetRate(m_fPrevRate);
        }
    }

    return hr;
}


// Queries whether the current session supports fast-forward.

HRESULT PlayerSeeking::CanFastForward(BOOL *pbCanFF)
{
    if (pbCanFF == NULL)
    {
        return E_POINTER;
    }

    *pbCanFF = 
        ((m_caps & MFSESSIONCAP_RATE_FORWARD) == MFSESSIONCAP_RATE_FORWARD);
    return S_OK;
}


// Queries whether the current session supports rewind (reverse play).

HRESULT PlayerSeeking::CanRewind(BOOL *pbCanRewind)
{
    if (pbCanRewind == NULL)
    {
        return E_POINTER;
    }

    *pbCanRewind = 
        ((m_caps & MFSESSIONCAP_RATE_REVERSE) == MFSESSIONCAP_RATE_REVERSE);
    return S_OK;
}


// Switches to fast-forward playback, as follows:
// - If the current rate is < 0 (reverse play), switch to 1x speed.
// - Otherwise, double the current playback rate.
//
// Note: This method is for convenience; the application can also call SetRate.

HRESULT PlayerSeeking::FastForward()
{
    if (!m_pRate)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;
    float   fTarget = GetNominalRate() * 2;

    if (fTarget <= 0.0f)
    {
        fTarget = 1.0f;
    }

    hr = SetRate(fTarget);

    return hr;
}


// Switches to reverse playback, as follows:
// - If the current rate is > 0 (forward playback), switch to -1x speed.
// - Otherwise, double the current (reverse) playback rate.
//
// Note: This method is for convenience; the application can also call SetRate.

HRESULT PlayerSeeking::Rewind()
{
    if (!m_pRate)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;
    float   fTarget = GetNominalRate() * 2;

    if (fTarget >= 0.0f)
    {
        fTarget = -1.0f;
    }

    hr = SetRate(fTarget);

    return hr;
}


// Sets the playback rate.

HRESULT PlayerSeeking::SetRate(float fRate)
{
    HRESULT hr = S_OK;
    BOOL bThin = FALSE;

    AutoLock lock(m_critsec);

    if (fRate == GetNominalRate())
    {
        return S_OK; // no-op
    }

    if (m_pRateSupport == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Check if this rate is supported. Try non-thinned playback first,
    // then fall back to thinned playback.

    hr = m_pRateSupport->IsRateSupported(FALSE, fRate, NULL);

    if (FAILED(hr))
    {
        bThin = TRUE;
        hr = m_pRateSupport->IsRateSupported(TRUE, fRate, NULL);
    }

    if (FAILED(hr))
    {
        // Unsupported rate.
        return hr;
    }

    // If there is an operation pending, cache the request.
    if (m_bPending)
    {
        m_request.fRate = fRate;
        m_request.bThin = bThin;

        // Remember the current transport state (play, paused, etc), so that we
        // can restore it after the rate change, if necessary. However, if 
        // anothercommand is already pending, that one takes precedent.

        if (m_request.command == CmdNone)
        {
            m_request.command = m_state.command;
        }

    }
    else
    {
        // No pending operation. Commit the new rate.
        hr  = CommitRateChange(fRate, bThin);
    }

    return hr;

}

// Sets the playback position.

HRESULT PlayerSeeking::SetPositionInternal(const MFTIME &hnsPosition)
{
    assert (!m_bPending);

    if (m_pSession == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;

    PROPVARIANT varStart;
    varStart.vt = VT_I8;
    varStart.hVal.QuadPart = hnsPosition;

    hr =  m_pSession->Start(NULL, &varStart);

    if (SUCCEEDED(hr))
    {
        // Store the pending state.
        m_state.command = CmdStart;
        m_state.hnsStart = hnsPosition;
        m_bPending = CMD_PENDING_SEEK;
    }
    return hr;
}




// Sets the playback rate.

HRESULT PlayerSeeking::CommitRateChange(float fRate, BOOL bThin)
{
    assert (!m_bPending);

    // Caller holds the lock.

    HRESULT hr = S_OK;
    MFTIME  hnsSystemTime = 0;
    MFTIME  hnsClockTime = 0;

    Command cmdNow = m_state.command;

    IMFClock *pClock = NULL;

    // Allowed rate transitions:

    // Positive <-> negative:   Stopped
    // Negative <-> zero:       Stopped
    // Postive <-> zero:        Paused or stopped

    if ((fRate > 0 && m_state.fRate <= 0) || (fRate < 0 && m_state.fRate >= 0))
    {
        // Transition to stopped.
        if (cmdNow == CmdStart)
        {
            // Get the current clock position. This will be the restart time.
            hr = m_pSession->GetClock(&pClock);
            if (FAILED(hr))
            {
                goto done;
            }

            (void)pClock->GetCorrelatedTime(0, &hnsClockTime, &hnsSystemTime);

            assert(hnsSystemTime != 0);

            // Stop and set the rate
            hr = Stop();
            if (FAILED(hr))
            {
                goto done;
            }

            // Cache Request: Restart from stop.
            m_request.command = CmdSeek;
            m_request.hnsStart = hnsClockTime;
        }
        else if (cmdNow == CmdPause)
        {
            // The current state is paused.

            // For this rate change, the session must be stopped. However, the 
            // session cannot transition back from stopped to paused. 
            // Therefore, this rate transition is not supported while paused.

            hr = MF_E_UNSUPPORTED_STATE_TRANSITION;
            goto done;
        }
    }
    else if (fRate == 0 && m_state.fRate != 0)
    {
        if (cmdNow != CmdPause)
        {
           // Transition to paused.

            // This transisition requires the paused state.

            // Pause and set the rate.
            hr = Pause();
            if (FAILED(hr))
            {
                goto done;
            }

            // Request: Switch back to current state.
            m_request.command = cmdNow;
        }
    }

    // Set the rate.
    hr = m_pRate->SetRate(bThin, fRate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Adjust our current rate and requested rate.
    m_request.fRate = m_state.fRate = fRate;

done:
    SafeRelease(&pClock);
    return hr;
}


float PlayerSeeking::GetNominalRate()
{
    return m_request.fRate;
}


// Called when playback starts or restarts.

HRESULT PlayerSeeking::OnSessionStart(HRESULT hrStatus)
{
    HRESULT hr = S_OK;

    if (FAILED(hrStatus))
    {
        return hrStatus;
    }

    // The Media Session completed a start/seek operation. Check if there
    // is another seek request pending.
    UpdatePendingCommands(CmdStart);

    return hr;
}


// Called when playback stops.

HRESULT PlayerSeeking::OnSessionStop(HRESULT hrStatus)
{
    HRESULT hr = S_OK;

    if (FAILED(hrStatus))
    {
        return hrStatus;
    }

    // The Media Session completed a transition to stopped. This might occur
    // because we are changing playback direction (forward/rewind). Check if
    // there is a pending rate-change request.

    UpdatePendingCommands(CmdStop);

    return hr;
}


// Called when playback pauses.

HRESULT PlayerSeeking::OnSessionPause(HRESULT hrStatus)
{
    HRESULT hr = S_OK;

    if (FAILED(hrStatus))
    {
        return hrStatus;
    }

    hr = UpdatePendingCommands(CmdPause);

    return hr;
}



// Called when the session ends.

HRESULT PlayerSeeking::OnSessionEnded(HRESULT hr)
{
    // After the session ends, playback starts from position zero. But if the
    // current playback rate is reversed, playback would end immediately 
    // (reversing from position 0). Therefore, reset the rate to 1x.

    if (GetNominalRate() < 0.0f)
    {
        m_state.command = CmdStop;

        hr = CommitRateChange(1.0f, FALSE);
    }

    return hr;
}


// Called after an operation completes.
// This method executes any cached requests.

HRESULT PlayerSeeking::UpdatePendingCommands(Command cmd)
{
    HRESULT hr = S_OK;

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    AutoLock lock(m_critsec);

    if (m_bPending && m_state.command == cmd)
    {
        m_bPending = FALSE;

        // The current pending command has completed.

        // First look for rate changes.
        if (m_request.fRate != m_state.fRate)
        {
            hr = CommitRateChange(m_request.fRate, m_request.bThin);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Now look for seek requests.
        if (!m_bPending)
        {
            switch (m_request.command)
            {
            case CmdNone:
                // Nothing to do.
                break;

            case CmdStart:
                Start();
                break;

            case CmdPause:
                Pause();
                break;

            case CmdStop:
                Stop();
                break;

            case CmdSeek:
                SetPositionInternal(m_request.hnsStart);
                break;
            }
            m_request.command = CmdNone;
        }
    }

done:
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 



