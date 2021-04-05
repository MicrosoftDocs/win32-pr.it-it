---
title: Introduzione con XInput
description: XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows. Sono supportati gli effetti Rumble del controller e l'input vocale e l'output.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727658"
---
# <a name="getting-started-with-xinput"></a><span data-ttu-id="7d4ef-104">Introduzione con XInput</span><span class="sxs-lookup"><span data-stu-id="7d4ef-104">Getting Started With XInput</span></span>

<span data-ttu-id="7d4ef-105">XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-105">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="7d4ef-106">Sono supportati gli effetti Rumble del controller e l'input vocale e l'output.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-106">Controller rumble effects and voice input and output are supported.</span></span>

<span data-ttu-id="7d4ef-107">Questo argomento fornisce una breve panoramica delle funzionalità di XInput e di come configurarlo in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-107">This topic provides a brief overview of the capabilities of XInput and how to set it up in an application.</span></span> <span data-ttu-id="7d4ef-108">Include quanto segue:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-108">It includes the following:</span></span>

-   [<span data-ttu-id="7d4ef-109">Introduzione a XInput</span><span class="sxs-lookup"><span data-stu-id="7d4ef-109">Introduction to XInput</span></span>](#introduction-to-xinput)
    -   [<span data-ttu-id="7d4ef-110">Controller Xbox</span><span class="sxs-lookup"><span data-stu-id="7d4ef-110">The Xbox Controller</span></span>](#the-xbox-controller)
-   [<span data-ttu-id="7d4ef-111">Uso di XInput</span><span class="sxs-lookup"><span data-stu-id="7d4ef-111">Using XInput</span></span>](#using-xinput)
    -   [<span data-ttu-id="7d4ef-112">Più controller</span><span class="sxs-lookup"><span data-stu-id="7d4ef-112">Multiple Controllers</span></span>](#multiple-controllers)
    -   [<span data-ttu-id="7d4ef-113">Recupero dello stato del controller</span><span class="sxs-lookup"><span data-stu-id="7d4ef-113">Getting Controller State</span></span>](#getting-controller-state)
    -   [<span data-ttu-id="7d4ef-114">Zona non recapitata</span><span class="sxs-lookup"><span data-stu-id="7d4ef-114">Dead Zone</span></span>](#dead-zone)
    -   [<span data-ttu-id="7d4ef-115">Impostazione degli effetti di vibrazione</span><span class="sxs-lookup"><span data-stu-id="7d4ef-115">Setting Vibration Effects</span></span>](#setting-vibration-effects)
    -   [<span data-ttu-id="7d4ef-116">Recupero degli identificatori di dispositivo audio</span><span class="sxs-lookup"><span data-stu-id="7d4ef-116">Getting Audio Device Identifiers</span></span>](#getting-audio-device-identifiers)
    -   [<span data-ttu-id="7d4ef-117">Recupero di GUID DirectSound (solo legacy DirectX SDK)</span><span class="sxs-lookup"><span data-stu-id="7d4ef-117">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>](#getting-directsound-guids-legacy-directx-sdk-only)
-   [<span data-ttu-id="7d4ef-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d4ef-118">Related topics</span></span>](#related-topics)

## <a name="introduction-to-xinput"></a><span data-ttu-id="7d4ef-119">Introduzione a XInput</span><span class="sxs-lookup"><span data-stu-id="7d4ef-119">Introduction to XInput</span></span>

<span data-ttu-id="7d4ef-120">La console Xbox usa un controller di gioco compatibile con Windows.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-120">The Xbox console uses a gaming controller that is compatible with Windows.</span></span> <span data-ttu-id="7d4ef-121">Le applicazioni possono usare l'API XInput per comunicare con questi controller quando sono collegati a un PC Windows (fino a quattro controller univoci possono essere collegati alla volta).</span><span class="sxs-lookup"><span data-stu-id="7d4ef-121">Applications can use the XInput API to communicate with these controllers when they are plugged into a Windows PC (up to four unique controllers can be plugged in at a time).</span></span>

<span data-ttu-id="7d4ef-122">Utilizzando questa API, è possibile eseguire query su qualsiasi controller Xbox connesso per lo stato e impostare gli effetti di vibrazione.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-122">Using this API, any connected Xbox Controller can be queried for its state, and vibration effects can be set.</span></span> <span data-ttu-id="7d4ef-123">È anche possibile eseguire query sui controller con l'auricolare collegato per i dispositivi di input e output audio che possono essere usati con la cuffia per l'elaborazione vocale.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-123">Controllers that have the headset attached can also be queried for sound input and output devices that can be used with the headset for voice processing.</span></span>

### <a name="the-xbox-controller"></a><span data-ttu-id="7d4ef-124">Controller Xbox</span><span class="sxs-lookup"><span data-stu-id="7d4ef-124">The Xbox Controller</span></span>

<span data-ttu-id="7d4ef-125">Il controller Xbox ha due stick direzionali analoghi, ognuno con un pulsante digitale, due trigger analoghi, un pad direzionale digitale con quattro direzioni e otto pulsanti digitali.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-125">The Xbox Controller has two analog directional sticks, each with a digital button, two analog triggers, a digital directional pad with four directions, and eight digital buttons.</span></span> <span data-ttu-id="7d4ef-126">Gli Stati di ognuno di questi input vengono restituiti nella struttura [**del \_ Gamepad XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) quando viene chiamata la funzione [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) .</span><span class="sxs-lookup"><span data-stu-id="7d4ef-126">The states of each of these inputs are returned in the [**XINPUT\_GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) structure when the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function is called.</span></span>

<span data-ttu-id="7d4ef-127">Il controller ha anche due motori di vibrazione per fornire agli utenti effetti sul feedback forzato.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-127">The controller also has two vibration motors to supply force feedback effects to the user.</span></span> <span data-ttu-id="7d4ef-128">Le velocità di questi motori vengono specificate nella struttura [**di \_ vibrazione XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) che viene passata alla funzione [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) per impostare gli effetti di vibrazione.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-128">The speeds of these motors are specified in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function to set vibration effects.</span></span>

<span data-ttu-id="7d4ef-129">Facoltativamente, una cuffia può essere connessa al controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-129">Optionally, a headset can be connected to the controller.</span></span> <span data-ttu-id="7d4ef-130">La cuffia ha un microfono per l'input vocale e una cuffia per l'output audio.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-130">The headset has a microphone for voice input, and a headphone for sound output.</span></span> <span data-ttu-id="7d4ef-131">È possibile chiamare la funzione [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) o legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) per ottenere gli identificatori del dispositivo che corrispondono ai dispositivi per il microfono e la cuffia.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-131">You can call the [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) or legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) function to obtain the device identifiers that correspond to the devices for the microphone and headphone.</span></span> <span data-ttu-id="7d4ef-132">È quindi possibile usare le [API audio principali](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) per ricevere l'input vocale e inviare l'output audio.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-132">You can then use the [Core Audio APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) to receive voice input and send sound output.</span></span>

## <a name="using-xinput"></a><span data-ttu-id="7d4ef-133">Uso di XInput</span><span class="sxs-lookup"><span data-stu-id="7d4ef-133">Using XInput</span></span>

<span data-ttu-id="7d4ef-134">L'uso di XInput è semplice come chiamare le funzioni XInput in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-134">Using XInput is as simple as calling the XInput functions as required.</span></span> <span data-ttu-id="7d4ef-135">Usando le funzioni XInput, è possibile recuperare lo stato del controller, ottenere gli ID audio della cuffia e impostare gli effetti Rumble del controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-135">Using the XInput functions, you can retrieve controller state, get headset audio IDs, and set controller rumble effects.</span></span>

### <a name="multiple-controllers"></a><span data-ttu-id="7d4ef-136">Più controller</span><span class="sxs-lookup"><span data-stu-id="7d4ef-136">Multiple Controllers</span></span>

<span data-ttu-id="7d4ef-137">L'API XInput supporta fino a quattro controller connessi in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-137">The XInput API supports up to four controllers connected at any time.</span></span> <span data-ttu-id="7d4ef-138">Per tutte le funzioni XInput è necessario un parametro *dwUserIndex* passato per identificare il controller impostato o sottoposto a query.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-138">The XInput functions all require a *dwUserIndex* parameter that is passed in to identify the controller being set or queried.</span></span> <span data-ttu-id="7d4ef-139">Questo ID sarà compreso nell'intervallo 0-3 e verrà impostato automaticamente da XInput.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-139">This ID will be in the range of 0-3 and is set automatically by XInput.</span></span> <span data-ttu-id="7d4ef-140">Il numero corrisponde alla porta a cui il controller è collegato e non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-140">The number corresponds to the port that the controller is plugged into, and is not modifiable.</span></span>

<span data-ttu-id="7d4ef-141">Ogni controller Visualizza l'ID che sta usando illuminando un quadrante sull'"anello di luce" al centro del controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-141">Each controller displays which ID it is using by lighting up a quadrant on the "ring of light" in the center of the controller.</span></span> <span data-ttu-id="7d4ef-142">Un valore *dwUserIndex* pari a 0 corrisponde al quadrante superiore sinistro; la numerazione continua intorno all'anello in ordine orario.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-142">A *dwUserIndex* value of 0 corresponds to the top-left quadrant; the numbering proceeds around the ring in clockwise order.</span></span>

<span data-ttu-id="7d4ef-143">Le applicazioni devono supportare più controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-143">Applications should support multiple controllers.</span></span>

### <a name="getting-controller-state"></a><span data-ttu-id="7d4ef-144">Recupero dello stato del controller</span><span class="sxs-lookup"><span data-stu-id="7d4ef-144">Getting Controller State</span></span>

<span data-ttu-id="7d4ef-145">Per tutta la durata di un'applicazione, è probabile che il recupero dello stato da un controller venga eseguito più spesso.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-145">Throughout the duration of an application, getting state from a controller will probably be done most often.</span></span> <span data-ttu-id="7d4ef-146">Dal frame al frame in un'applicazione di gioco, è necessario recuperare lo stato e aggiornare le informazioni sul gioco in modo da riflettere le modifiche del controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-146">From frame to frame in a game application, state should be retrieved and game information updated to reflect the controller changes.</span></span>

<span data-ttu-id="7d4ef-147">Per recuperare lo stato, usare la funzione [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :</span><span class="sxs-lookup"><span data-stu-id="7d4ef-147">To retrieve state, use the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function:</span></span>

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

<span data-ttu-id="7d4ef-148">Si noti che il valore restituito di [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) può essere usato per determinare se il controller è connesso.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-148">Note that the return value of [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) can be used to determine if the controller is connected.</span></span> <span data-ttu-id="7d4ef-149">Le applicazioni devono definire una struttura per conservare informazioni interne sul controller; Queste informazioni devono essere confrontate con i risultati di **XInputGetState** per determinare quali modifiche sono state apportate, ad esempio le pressioni dei pulsanti o i delta dei controller analoghi.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-149">Applications should define a structure to hold internal controller information; this information should be compared against the results of **XInputGetState** to determine what changes, such as button presses or analog controller deltas, were made that frame.</span></span> <span data-ttu-id="7d4ef-150">Nell'esempio precedente, i *\_ controller g* rappresentano una struttura di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-150">In the above example, *g\_Controllers* represents such a structure.</span></span>

<span data-ttu-id="7d4ef-151">Una volta recuperato lo stato in una struttura [**di \_ stato XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , è possibile verificarne le modifiche e ottenere informazioni specifiche sullo stato del controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-151">Once the state has been retrieved in a [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure, you can check it for changes and get specific information about controller state.</span></span>

<span data-ttu-id="7d4ef-152">Il membro *dwPacketNumber* della struttura [**di \_ stato XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_state) può essere usato per verificare se lo stato del controller è stato modificato dall'ultima chiamata a [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span><span class="sxs-lookup"><span data-stu-id="7d4ef-152">The *dwPacketNumber* member of the [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure can be used to check if the state of the controller has changed since the last call to [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span></span> <span data-ttu-id="7d4ef-153">Se *dwPacketNumber* non viene modificato tra due chiamate sequenziali a **XInputGetState**, non sono state apportate modifiche allo stato.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-153">If *dwPacketNumber* does not change between two sequential calls to **XInputGetState**, then there has been no change in state.</span></span> <span data-ttu-id="7d4ef-154">Se è diverso, l'applicazione deve controllare il membro del *Gamepad* della struttura di **\_ stato XINPUT** per ottenere informazioni più dettagliate sullo stato.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-154">If it differs, then the application should check the *Gamepad* member of the **XINPUT\_STATE** structure to get more detailed state information.</span></span>

<span data-ttu-id="7d4ef-155">Per motivi di prestazioni, non chiamare [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) per uno slot utente ' Empty ' ogni frame.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-155">For performance reasons, don't call [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) for an 'empty' user slot every frame.</span></span> <span data-ttu-id="7d4ef-156">Si consiglia di verificare la presenza di nuovi controller a intervalli di pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-156">We recommend that you space out checks for new controllers every few seconds instead.</span></span>

### <a name="dead-zone"></a><span data-ttu-id="7d4ef-157">Zona non recapitata</span><span class="sxs-lookup"><span data-stu-id="7d4ef-157">Dead Zone</span></span>

<span data-ttu-id="7d4ef-158">Per consentire agli utenti di avere un'esperienza di gioco coerente, il gioco deve implementare correttamente l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-158">In order for users to have a consistent gameplay experience, your game must implement dead zone correctly.</span></span> <span data-ttu-id="7d4ef-159">L'area inattiva è rappresentata dai valori di "movimento" segnalati dal controller anche quando i ThumbSticks analoghi non vengono modificati e centrati.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-159">The dead zone is "movement" values reported by the controller even when the analog thumbsticks are untouched and centered.</span></span> <span data-ttu-id="7d4ef-160">Esiste anche un'area inattiva per i 2 trigger analoghi.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-160">There is also a dead zone for the 2 analog triggers.</span></span>

> [!Note]  
> <span data-ttu-id="7d4ef-161">I giochi che usano XInput che non filtrano l'area insufficiente comportano una scarsa giocabilità.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-161">Games that use XInput that do not filter dead zone at all will experience poor gameplay.</span></span> <span data-ttu-id="7d4ef-162">Si noti che alcuni controller sono più sensibili di altri, pertanto l'area inattiva può variare da unità a unità.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-162">Please note that some controllers are more sensitive than others, thus the dead zone may vary from unit to unit.</span></span> <span data-ttu-id="7d4ef-163">Si consiglia di testare i giochi con diversi controller Xbox su sistemi diversi.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-163">It is recommended that you test your games with several Xbox controllers on different systems.</span></span>

<span data-ttu-id="7d4ef-164">Le applicazioni devono usare "zone inattive" sugli input analoghi (trigger, stick) per indicare quando uno spostamento è stato sufficientemente appropriato per essere considerato valido.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-164">Applications should use "dead zones" on analog inputs (triggers, sticks) to indicate when a movement has been made sufficiently on the stick or trigger to be considered valid.</span></span>

<span data-ttu-id="7d4ef-165">L'applicazione deve controllare le zone non recapitabili e rispondere a appopriately, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-165">Your application should check for dead zones and respond appopriately, as in this example:</span></span>

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

<span data-ttu-id="7d4ef-166">Questo esempio calcola il vettore di direzione del controller e la distanza del vettore con cui è stato effettuato il push del controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-166">This example calculates the controller's direction vector and how far along the vector the controller has been pushed.</span></span> <span data-ttu-id="7d4ef-167">In questo modo è possibile applicare un DeadZone circolare semplicemente controllando se la grandezza del controller è maggiore del valore di DeadZone.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-167">This allows enforcement of a circular deadzone by simply checking whether the controller's magnitude is greater than the deadzone value.</span></span> <span data-ttu-id="7d4ef-168">Inoltre, il codice normalizza la Magnitude del controller che può quindi essere moltiplicato per un fattore specifico del gioco per convertire la posizione del controller in unità rilevanti per il gioco.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-168">In addition the code normalizes the controller's magnitude which can then be multiplied by a game specific factor to convert the controller's position to units relevant to the game.</span></span>

<span data-ttu-id="7d4ef-169">Si noti che è possibile definire zone inattive per i bastoni e i trigger (ovunque si trovino da 0-65534) oppure usare il zone morte fornito definito come XINPUT \_ Gamepad \_ Left \_ Thumb \_ DEADZONE, XINPUT \_ Gamepad \_ right \_ Thumb \_ DEADZONE e XINPUT \_ Gamepad \_ trigger \_ Threshold in XINPUT. h:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-169">Note that you may define your own dead zones for the sticks and triggers (anywhere from 0-65534), or you may use the provided deadzones defined as XINPUT\_GAMEPAD\_LEFT\_THUMB\_DEADZONE, XINPUT\_GAMEPAD\_RIGHT\_THUMB\_DEADZONE, and XINPUT\_GAMEPAD\_TRIGGER\_THRESHOLD in XInput.h:</span></span>

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

<span data-ttu-id="7d4ef-170">Una volta applicato il DeadZone, può risultare utile ridimensionare l'intervallo risultante \[ 0.0.. 1.0 a \] virgola mobile (come nell'esempio precedente) e, facoltativamente, applicare una trasformazione non lineare.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-170">Once the deadzone is enforced, you may find it useful to scale the resulting range \[0.0..1.0\] floating point (as in the example above), and optionally apply a non-linear transform.</span></span>

<span data-ttu-id="7d4ef-171">Ad esempio, con la guida ai giochi, può essere utile creare un cubo per il risultato in modo da ottenere una migliore sensazione di guidare le auto usando un gamepad, in quanto cubi il risultato offre una maggiore precisione negli intervalli inferiori, che è auspicabile, perché i giocatori in genere applicano la forza morbida per ottenere un leggero movimento o applicare una forzatura totale in una direzione per ottenere la risposta Rd</span><span class="sxs-lookup"><span data-stu-id="7d4ef-171">For example, with driving games, it may be helpful to cube the result to provide a better feel to driving the cars using a gamepad, as cubing the result gives you more precision in the lower ranges, which is desirable, since gamers typically either apply soft force to get subtle movement or apply hard force all the way in one direction to get rd response.</span></span>

### <a name="setting-vibration-effects"></a><span data-ttu-id="7d4ef-172">Impostazione degli effetti di vibrazione</span><span class="sxs-lookup"><span data-stu-id="7d4ef-172">Setting Vibration Effects</span></span>

<span data-ttu-id="7d4ef-173">Oltre a ottenere lo stato del controller, è anche possibile inviare dati di vibrazione al controller per modificare il feedback fornito all'utente del controller.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-173">In addition to getting the state of the controller, you may also send vibration data to the controller to alter the feedback provided to the user of the controller.</span></span> <span data-ttu-id="7d4ef-174">Il controller contiene due motori Rumble che possono essere controllati in modo indipendente passando i valori alla funzione [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .</span><span class="sxs-lookup"><span data-stu-id="7d4ef-174">The controller contains two rumble motors that can be independently controlled by passing values to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function.</span></span>

<span data-ttu-id="7d4ef-175">La velocità di ogni motore può essere specificata usando un valore di parola nella struttura di [**\_ vibrazione XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) che viene passata alla funzione [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-175">The speed of each motor can be specified using a WORD value in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function as follows:</span></span>

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

<span data-ttu-id="7d4ef-176">Si noti che il motore a destra è il motore ad alta frequenza, il motore di sinistra è il motore a bassa frequenza.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-176">Note that the right motor is the high-frequency motor, the left motor is the low-frequency motor.</span></span> <span data-ttu-id="7d4ef-177">Non è sempre necessario impostare la stessa quantità, perché forniscono effetti diversi.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-177">They do not always need to be set to the same amount, as they provide different effects.</span></span>

### <a name="getting-audio-device-identifiers"></a><span data-ttu-id="7d4ef-178">Recupero degli identificatori di dispositivo audio</span><span class="sxs-lookup"><span data-stu-id="7d4ef-178">Getting Audio Device Identifiers</span></span>

<span data-ttu-id="7d4ef-179">La cuffia per un controller Xbox dispone di queste funzioni:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-179">The headset for an Xbox Controller has these functions:</span></span>

-   <span data-ttu-id="7d4ef-180">Registrare un suono usando un microfono</span><span class="sxs-lookup"><span data-stu-id="7d4ef-180">Record sound using a microphone</span></span>
-   <span data-ttu-id="7d4ef-181">Riprodurre un suono con una cuffia</span><span class="sxs-lookup"><span data-stu-id="7d4ef-181">Play back sound using a headphone</span></span>

<span data-ttu-id="7d4ef-182">Usare questo codice per ottenere gli identificatori del dispositivo per la cuffia:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-182">Use this code to obtain the device identifiers for the headset:</span></span>

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

<span data-ttu-id="7d4ef-183">Una volta ottenuti gli identificatori del dispositivo, è possibile creare le interfacce appropriate.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-183">After you obtain the device identifiers, you can create the appropriate interfaces.</span></span> <span data-ttu-id="7d4ef-184">Se ad esempio si usa XAudio 2,8, usare questo codice per creare una voce di mastering per questo dispositivo:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-184">For example, if you use XAudio 2.8, use this code to create a mastering voice for this device:</span></span>

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

<span data-ttu-id="7d4ef-185">Per informazioni su come usare l'identificatore del dispositivo captureId, vedere [acquisizione di un flusso](/windows/desktop/CoreAudio/capturing-a-stream).</span><span class="sxs-lookup"><span data-stu-id="7d4ef-185">For info about how to use the captureId device identifier, see [Capturing a Stream](/windows/desktop/CoreAudio/capturing-a-stream).</span></span>

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a><span data-ttu-id="7d4ef-186">Recupero di GUID DirectSound (solo legacy DirectX SDK)</span><span class="sxs-lookup"><span data-stu-id="7d4ef-186">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>

<span data-ttu-id="7d4ef-187">L'auricolare che può essere connesso a un controller Xbox ha due funzioni: può registrare un suono usando un microfono ed è in grado di riprodurre il suono con una cuffia.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-187">The headset that can be connected to an Xbox Controller has two functions: it can record sound using a microphone, and it can play back sound using a headphone.</span></span> <span data-ttu-id="7d4ef-188">Nell'API XInput queste funzioni vengono eseguite tramite [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), usando le interfacce **IDirectSound8** e **IDirectSoundCapture8** .</span><span class="sxs-lookup"><span data-stu-id="7d4ef-188">In the XInput API, these functions are accomplished through [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), using the **IDirectSound8** and **IDirectSoundCapture8** interfaces.</span></span>

<span data-ttu-id="7d4ef-189">Per associare il microfono e la cuffia auricolare alle interfacce [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) appropriate, è necessario ottenere il DirectSoundGUIDs per i dispositivi di acquisizione e rendering chiamando [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span><span class="sxs-lookup"><span data-stu-id="7d4ef-189">To associate the headset microphone and headphone with their appropriate [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) interfaces, you must get the DirectSoundGUIDs for the capture and render devices by calling [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span></span>

> [!Note]  
> <span data-ttu-id="7d4ef-190">L'uso di [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) legacy non è consigliato e non è disponibile nelle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7d4ef-190">Use of the legacy [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) is not recommended, and is not available in Windows Store apps.</span></span> <span data-ttu-id="7d4ef-191">Le informazioni in questa sezione si applicano solo alla versione di XInput di DirectX SDK (XInput 1,3).</span><span class="sxs-lookup"><span data-stu-id="7d4ef-191">The info in this section only applies to the DirectX SDK version of XInput (XInput 1.3).</span></span> <span data-ttu-id="7d4ef-192">La versione di Windows 8 di XInput (XInput 1,4) usa esclusivamente identificatori di dispositivo WASAPI (Windows Audio Session API) ottenuti tramite [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span><span class="sxs-lookup"><span data-stu-id="7d4ef-192">The Windows 8 version of XInput (XInput 1.4) exclusively uses Windows Audio Session API (WASAPI) device identifiers that are obtained through [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span></span>

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

<span data-ttu-id="7d4ef-193">Una volta recuperati i GUID, è possibile creare le interfacce appropriate chiamando DirectSoundCreate8 e DirectSoundCaptureCreate8 come segue:</span><span class="sxs-lookup"><span data-stu-id="7d4ef-193">Once you have retrieved the GUIDs you can create the appropriate interfaces by calling DirectSoundCreate8 and DirectSoundCaptureCreate8 like this:</span></span>

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a><span data-ttu-id="7d4ef-194">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d4ef-194">Related topics</span></span>

[<span data-ttu-id="7d4ef-195">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="7d4ef-195">Programming Reference</span></span>](programming-reference.md)