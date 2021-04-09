---
title: Sviluppo di applicazioni desktop con DPI elevato in Windows
description: Questo contenuto è destinato agli sviluppatori che vogliono aggiornare le applicazioni desktop per gestire il fattore di scalabilità della visualizzazione dinamica (noto anche come
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104118595"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a><span data-ttu-id="fc35e-103">Sviluppo di applicazioni desktop con DPI elevato in Windows</span><span class="sxs-lookup"><span data-stu-id="fc35e-103">High DPI Desktop Application Development on Windows</span></span>

<span data-ttu-id="fc35e-104">Questo contenuto è destinato agli sviluppatori che desiderano aggiornare le applicazioni desktop per gestire in modo dinamico il fattore di scalabilità di visualizzazione (punti per pollice o DPI), consentendo alle applicazioni di essere nitide in qualsiasi visualizzazione di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="fc35e-104">This content is targeted at developers who are looking to update desktop applications to handle display scale factor (dots per inch, or DPI) changes dynamically, allowing their applications to be crisp on any display they're rendered on.</span></span>

<span data-ttu-id="fc35e-105">Per iniziare, se si sta creando una nuova app di Windows da zero, è consigliabile creare un'applicazione [piattaforma UWP (Universal Windows Platform) (UWP)](/windows/uwp/get-started/whats-a-uwp) .</span><span class="sxs-lookup"><span data-stu-id="fc35e-105">To start, if you're creating a new Windows app from scratch, it is highly recommended that you create a [Universal Windows Platform (UWP)](/windows/uwp/get-started/whats-a-uwp) application.</span></span> <span data-ttu-id="fc35e-106">Le applicazioni UWP vengono &mdash; ridimensionate automaticamente e in modo dinamico &mdash; per ogni visualizzazione su cui sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fc35e-106">UWP applications automatically&mdash;and dynamically&mdash;scale for each display that they're running on.</span></span>

<span data-ttu-id="fc35e-107">Le applicazioni desktop che usano le tecnologie di programmazione Windows precedenti (programmazione Win32 non elaborata, Windows Form, Windows Presentation Framework (WPF) e così via) non sono in grado di gestire automaticamente il ridimensionamento DPI senza ulteriori operazioni da parte degli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="fc35e-107">Desktop applications using older Windows programming technologies (raw Win32 programming, Windows Forms, Windows Presentation Framework (WPF), etc.) are unable to automatically handle DPI scaling without additional developer work.</span></span> <span data-ttu-id="fc35e-108">Senza questo tipo di lavoro, le applicazioni appariranno sfocate o ridimensionate in modo errato in molti scenari di utilizzo comuni.</span><span class="sxs-lookup"><span data-stu-id="fc35e-108">Without such work, applications will appear blurry or incorrectly-sized in many common usage scenarios.</span></span> <span data-ttu-id="fc35e-109">Questo documento fornisce il contesto e le informazioni relative all'aggiornamento di un'applicazione desktop per il rendering corretto.</span><span class="sxs-lookup"><span data-stu-id="fc35e-109">This document provides context and information about what is involved in updating a desktop application to render correctly.</span></span>

## <a name="display-scale-factor--dpi"></a><span data-ttu-id="fc35e-110">Visualizzare il fattore di scala & DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-110">Display Scale Factor & DPI</span></span>

<span data-ttu-id="fc35e-111">Con l'avanzare della tecnologia di visualizzazione, i produttori del pannello di visualizzazione hanno compresso un numero crescente di pixel in ogni unità di spazio fisico nei rispettivi pannelli.</span><span class="sxs-lookup"><span data-stu-id="fc35e-111">As display technology has progressed, display panel manufacturers have packed an increasing number of pixels into each unit of physical space on their panels.</span></span> <span data-ttu-id="fc35e-112">Ciò ha comportato la presenza di punti per pollice (DPI) di pannelli di visualizzazione moderni molto più elevati rispetto a quelli precedenti.</span><span class="sxs-lookup"><span data-stu-id="fc35e-112">This has resulted in the dots per inch (DPI) of modern display panels being much higher than they have historically been.</span></span> <span data-ttu-id="fc35e-113">In passato, la maggior parte degli schermi aveva 96 pixel per ogni pollice lineare di spazio fisico (96 DPI); in 2017, le visualizzazioni con circa 300 DPI o versioni successive sono immediatamente disponibili.</span><span class="sxs-lookup"><span data-stu-id="fc35e-113">In the past, most displays had 96 pixels per linear inch of physical space (96 DPI); in 2017, displays with nearly 300 DPI or higher are readily available.</span></span>

<span data-ttu-id="fc35e-114">La maggior parte dei Framework legacy dell'interfaccia utente desktop include presupposti incorporati che il valore DPI visualizzato non cambierà nel corso del processo.</span><span class="sxs-lookup"><span data-stu-id="fc35e-114">Most legacy desktop UI frameworks have built-in assumptions that the display DPI will not change during the lifetime of the process.</span></span>  <span data-ttu-id="fc35e-115">Questo presupposto non è più valido, con la visualizzazione di dpi di solito modificate più volte durante la durata di un processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc35e-115">This assumption no longer holds true, with display DPIs commonly changing several times throughout an application process's lifetime.</span></span> <span data-ttu-id="fc35e-116">Di seguito sono riportati alcuni scenari comuni in cui le modifiche al fattore di scala/DPI di visualizzazione sono:</span><span class="sxs-lookup"><span data-stu-id="fc35e-116">Some common scenarios where the display scale factor/DPI changes are:</span></span>

-   <span data-ttu-id="fc35e-117">Configurazioni a più monitor in cui ogni schermo presenta un fattore di scala diverso e l'applicazione viene spostata da una visualizzazione all'altra (ad esempio, 4K e una visualizzazione 1080p)</span><span class="sxs-lookup"><span data-stu-id="fc35e-117">Multiple-monitor setups where each display has a different scale factor and the application is moved from one display to another (such as a 4K and a 1080p display)</span></span>
-   <span data-ttu-id="fc35e-118">Ancoraggio e disancoraggio di un computer portatile con DPI elevato con schermo esterno a DPI basso (o viceversa)</span><span class="sxs-lookup"><span data-stu-id="fc35e-118">Docking and undocking a high DPI laptop with a low-DPI external display (or vice versa)</span></span>
-   <span data-ttu-id="fc35e-119">Connessione tramite Desktop remoto da un computer portatile/tablet a DPI elevato a un dispositivo a basso DPI (o viceversa)</span><span class="sxs-lookup"><span data-stu-id="fc35e-119">Connecting via Remote Desktop from a high DPI laptop/tablet to a low-DPI device (or vice versa)</span></span>
-   <span data-ttu-id="fc35e-120">Apportare modifiche alle impostazioni del fattore di scalabilità durante l'esecuzione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="fc35e-120">Making a display-scale-factor settings change while applications are running</span></span>

<span data-ttu-id="fc35e-121">In questi scenari, le applicazioni UWP si ritraggono automaticamente per il nuovo valore DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-121">In these scenarios, UWP applications redraw themselves for the new DPI automatically.</span></span> <span data-ttu-id="fc35e-122">Per impostazione predefinita, e senza altre attività di sviluppo, le applicazioni desktop non lo eseguono.</span><span class="sxs-lookup"><span data-stu-id="fc35e-122">By default, and without additional developer work, desktop applications do not.</span></span> <span data-ttu-id="fc35e-123">Le applicazioni desktop che non eseguono questo lavoro aggiuntivo per rispondere alle modifiche DPI possono apparire sfocate o ridimensionate in modo errato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="fc35e-123">Desktop applications that don't do this extra work to respond to DPI changes may appear blurry or incorrectly-sized to the user.</span></span>

## <a name="dpi-awareness-mode"></a><span data-ttu-id="fc35e-124">Modalità di riconoscimento DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-124">DPI Awareness Mode</span></span>

<span data-ttu-id="fc35e-125">Le applicazioni desktop devono indicare a Windows se supportano la scalabilità DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-125">Desktop applications must tell Windows if they support DPI scaling.</span></span> <span data-ttu-id="fc35e-126">Per impostazione predefinita, il sistema considera le applicazioni desktop DPI incompatibili e bitmap-estende le finestre.</span><span class="sxs-lookup"><span data-stu-id="fc35e-126">By default, the system considers desktop applications DPI unaware and bitmap-stretches their windows.</span></span> <span data-ttu-id="fc35e-127">Impostando una delle seguenti modalità di riconoscimento DPI disponibili, le applicazioni possono comunicare in modo esplicito a Windows come vogliono gestire il ridimensionamento DPI:</span><span class="sxs-lookup"><span data-stu-id="fc35e-127">By setting one of the following available DPI awareness modes, applications can explicitly tell Windows how they wish to handle DPI scaling:</span></span>

### <a name="dpi-unaware"></a><span data-ttu-id="fc35e-128">DPI non a conoscenza</span><span class="sxs-lookup"><span data-stu-id="fc35e-128">DPI Unaware</span></span>

<span data-ttu-id="fc35e-129">Le applicazioni non compatibili con DPI eseguono il rendering con un valore DPI fisso di 96 (100%).</span><span class="sxs-lookup"><span data-stu-id="fc35e-129">DPI unaware applications render at a fixed DPI value of 96 (100%).</span></span> <span data-ttu-id="fc35e-130">Ogni volta che queste applicazioni vengono eseguite su una schermata con una scala di visualizzazione superiore a 96 DPI, Windows estenderà la bitmap dell'applicazione alla dimensione fisica prevista.</span><span class="sxs-lookup"><span data-stu-id="fc35e-130">Whenever these applications are run on a screen with a display scale greater than 96 DPI, Windows will stretch the application bitmap to the expected physical size.</span></span> <span data-ttu-id="fc35e-131">In questo modo l'applicazione risulta sfocata.</span><span class="sxs-lookup"><span data-stu-id="fc35e-131">This results in the application appearing blurry.</span></span>

### <a name="system-dpi-awareness"></a><span data-ttu-id="fc35e-132">Riconoscimento DPI sistema</span><span class="sxs-lookup"><span data-stu-id="fc35e-132">System DPI Awareness</span></span>

<span data-ttu-id="fc35e-133">Le applicazioni desktop che sono compatibili con i valori DPI del sistema ricevono in genere il valore DPI del monitoraggio connesso primario al momento dell'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fc35e-133">Desktop applications that are system DPI aware typically receive the DPI of the primary connected monitor as of the time of user sign-in.</span></span> <span data-ttu-id="fc35e-134">Durante l'inizializzazione, il layout dell'interfaccia utente è appropriato, ovvero i controlli di ridimensionamento, la scelta delle dimensioni del carattere, il caricamento di asset e così via, usando tale valore DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc35e-134">During initialization, they lay out their UI appropriately (sizing controls, choosing font sizes, loading assets, etc.) using that System DPI value.</span></span> <span data-ttu-id="fc35e-135">Di conseguenza, le applicazioni compatibili con DPI di sistema non vengono ridimensionate in DPI (con estensione bitmap) da Windows su Visualizza il rendering in base a tale valore DPI singolo.</span><span class="sxs-lookup"><span data-stu-id="fc35e-135">As such, System DPI-aware applications are not DPI scaled (bitmap stretched) by Windows on displays rendering at that single DPI.</span></span> <span data-ttu-id="fc35e-136">Quando l'applicazione viene spostata in una visualizzazione con un fattore di scala diverso o se il fattore di scala di visualizzazione cambia in altro modo, Windows eseguirà la scalabilità delle finestre dell'applicazione, facendo in modo che risulti sfocata.</span><span class="sxs-lookup"><span data-stu-id="fc35e-136">When the application is moved to a display with a different scale factor, or if the display scale factor otherwise changes, Windows will bitmap scale the application's windows, making them appear blurry.</span></span> <span data-ttu-id="fc35e-137">In realtà, le applicazioni desktop compatibili con DPI di sistema eseguono il rendering in modo nitido a un singolo fattore di scala di visualizzazione, divenendo sfocate ogni volta che il DPI cambia.</span><span class="sxs-lookup"><span data-stu-id="fc35e-137">Effectively, System DPI-aware desktop applications only render crisply at a single display scale factor, becoming blurry whenever the DPI changes.</span></span>

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a><span data-ttu-id="fc35e-138">Riconoscimento DPI Per-Monitor e Per-Monitor (v2)</span><span class="sxs-lookup"><span data-stu-id="fc35e-138">Per-Monitor and Per-Monitor (V2) DPI Awareness</span></span>

<span data-ttu-id="fc35e-139">È consigliabile aggiornare le applicazioni desktop in modo da utilizzare la modalità di riconoscimento DPI per monitor, consentendo di eseguire immediatamente il rendering in modo corretto ogni volta che viene modificato il valore DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-139">It is recommended that desktop applications be updated to use per-monitor DPI awareness mode, allowing them to immediately render correctly whenever the DPI changes.</span></span> <span data-ttu-id="fc35e-140">Quando un'applicazione segnala a Windows che vuole essere eseguita in questa modalità, Windows non consente di estendere l'applicazione quando viene modificato il valore DPI, inviando invece [WM \_ DPICHANGED](wm-dpichanged.md) alla finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc35e-140">When an application reports to Windows that it wants to run in this mode, Windows will not bitmap stretch the application when the DPI changes, instead sending [WM\_DPICHANGED](wm-dpichanged.md) to the application window.</span></span> <span data-ttu-id="fc35e-141">È quindi responsabilità completa dell'applicazione gestire il ridimensionamento per il nuovo valore DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-141">It is then the complete responsibility of the application to handle resizing itself for the new DPI.</span></span> <span data-ttu-id="fc35e-142">La maggior parte dei framework dell'interfaccia utente usati dalle applicazioni desktop (controlli comuni di Windows (Comctl32), Windows Form, Windows Presentation Framework e così via) non supporta la scalabilità DPI automatica, che richiede agli sviluppatori di ridimensionare e riposizionare il contenuto delle proprie finestre.</span><span class="sxs-lookup"><span data-stu-id="fc35e-142">Most UI frameworks used by desktop applications (Windows common controls (comctl32), Windows Forms, Windows Presentation Framework, etc.) do not support automatic DPI scaling, requiring developers to resize and reposition the contents of their windows themselves.</span></span>

<span data-ttu-id="fc35e-143">Esistono due versioni di Per-Monitor consapevolezza che un'applicazione può registrarsi come: versione 1 e versione 2 (PMv2).</span><span class="sxs-lookup"><span data-stu-id="fc35e-143">There are two versions of Per-Monitor awareness that an application can register itself as: version 1 and version 2 (PMv2).</span></span> <span data-ttu-id="fc35e-144">La registrazione di un processo come in esecuzione in modalità di riconoscimento PMv2 comporta:</span><span class="sxs-lookup"><span data-stu-id="fc35e-144">Registering a process as running in PMv2 awareness mode results in:</span></span>

1.  <span data-ttu-id="fc35e-145">L'applicazione a cui viene inviata una notifica quando viene modificato il valore DPI (sia gli HWND di primo livello che quelli figlio)</span><span class="sxs-lookup"><span data-stu-id="fc35e-145">The application being notified when the DPI changes (both the top-level and child HWNDs)</span></span>
2.  <span data-ttu-id="fc35e-146">Applicazione che Visualizza i pixel non elaborati di ogni visualizzazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-146">The application seeing the raw pixels of each display</span></span>
3.  <span data-ttu-id="fc35e-147">L'applicazione non è mai stata ridimensionata in base alla bitmap di Windows</span><span class="sxs-lookup"><span data-stu-id="fc35e-147">The application never being bitmap scaled by Windows</span></span>
4.  <span data-ttu-id="fc35e-148">Area non client automatica (didascalia della finestra, barre di scorrimento e così via) Ridimensionamento DPI per Windows</span><span class="sxs-lookup"><span data-stu-id="fc35e-148">Automatic non-client area (window caption, scroll bars, etc.) DPI scaling by Windows</span></span>
5.  <span data-ttu-id="fc35e-149">Finestre di dialogo Win32 (da [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) dpi automaticamente ridimensionate da Windows</span><span class="sxs-lookup"><span data-stu-id="fc35e-149">Win32 dialogs (from [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatically DPI scaled by Windows</span></span>
6.  <span data-ttu-id="fc35e-150">Asset bitmap disegnati con tema in controlli comuni (caselle di controllo, sfondi dei pulsanti e così via) sottoposti a rendering automatico con il fattore di scala DPI appropriato</span><span class="sxs-lookup"><span data-stu-id="fc35e-150">Theme-drawn bitmap assets in common controls (checkboxes, button backgrounds, etc.) being automatically rendered at the appropriate DPI scale factor</span></span>

<span data-ttu-id="fc35e-151">Quando è in esecuzione in modalità di riconoscimento Per-Monitor V2, le applicazioni ricevono una notifica quando viene modificato il valore DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-151">When running in Per-Monitor v2 Awareness mode, applications are notified when their DPI has changed.</span></span> <span data-ttu-id="fc35e-152">Se un'applicazione non si ridimensiona automaticamente per il nuovo valore DPI, l'interfaccia utente dell'applicazione apparirà troppo piccola o troppo grande (a seconda della differenza tra i valori DPI precedenti e nuovi).</span><span class="sxs-lookup"><span data-stu-id="fc35e-152">If an application does not resize itself for the new DPI, the application UI will appear too small or too large (depending on the difference in the previous and new DPI values).</span></span>

> [!Note]  
> <span data-ttu-id="fc35e-153">Il riconoscimento Per-Monitor V1 (PMv1) è molto limitato.</span><span class="sxs-lookup"><span data-stu-id="fc35e-153">Per-Monitor V1 (PMv1) awareness is very limited.</span></span> <span data-ttu-id="fc35e-154">È consigliabile usare PMv2 per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fc35e-154">It is recommended that applications use PMv2.</span></span>

<span data-ttu-id="fc35e-155">Nella tabella seguente viene illustrato come verrà eseguito il rendering delle applicazioni in scenari diversi:</span><span class="sxs-lookup"><span data-stu-id="fc35e-155">The following table shows how applications will render under different scenarios:</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc35e-156">Modalità di riconoscimento DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-156">DPI Awareness Mode</span></span></th>
<th><span data-ttu-id="fc35e-157">Versione di Windows introdotta</span><span class="sxs-lookup"><span data-stu-id="fc35e-157">Windows Version Introduced</span></span></th>
<th><span data-ttu-id="fc35e-158">Visualizzazione dell'applicazione di DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-158">Application's view of DPI</span></span></th>
<th><span data-ttu-id="fc35e-159">Comportamento sulla modifica DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-159">Behavior on DPI change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc35e-160">A conoscenza</span><span class="sxs-lookup"><span data-stu-id="fc35e-160">Unaware</span></span></td>
<td><span data-ttu-id="fc35e-161">N/D</span><span class="sxs-lookup"><span data-stu-id="fc35e-161">N/A</span></span></td>
<td><span data-ttu-id="fc35e-162">Tutti gli schermi sono 96 DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-162">All displays are 96 DPI</span></span></td>
<td><span data-ttu-id="fc35e-163">Adattamento bitmap (sfocatura)</span><span class="sxs-lookup"><span data-stu-id="fc35e-163">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc35e-164">Sistema</span><span class="sxs-lookup"><span data-stu-id="fc35e-164">System</span></span></td>
<td><span data-ttu-id="fc35e-165">Vista</span><span class="sxs-lookup"><span data-stu-id="fc35e-165">Vista</span></span></td>
<td><span data-ttu-id="fc35e-166">Tutti gli schermi hanno lo stesso valore DPI (il valore DPI dello schermo principale al momento dell'avvio della sessione utente corrente)</span><span class="sxs-lookup"><span data-stu-id="fc35e-166">All displays have the same DPI (the DPI of the primary display at the time the current user session was started)</span></span></td>
<td><span data-ttu-id="fc35e-167">Adattamento bitmap (sfocatura)</span><span class="sxs-lookup"><span data-stu-id="fc35e-167">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc35e-168">Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="fc35e-168">Per-Monitor</span></span></td>
<td><span data-ttu-id="fc35e-169">8.1</span><span class="sxs-lookup"><span data-stu-id="fc35e-169">8.1</span></span></td>
<td><span data-ttu-id="fc35e-170">DPI della visualizzazione in cui si trova la finestra dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-170">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="fc35e-171">HWND di primo livello riceve una notifica di modifica DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-171">Top-level HWND is notified of DPI change</span></span></li>
<li><span data-ttu-id="fc35e-172">Nessuna scala DPI di alcun elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fc35e-172">No DPI scaling of any UI elements.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc35e-173">Per-Monitor V2</span><span class="sxs-lookup"><span data-stu-id="fc35e-173">Per-Monitor V2</span></span></td>
<td><span data-ttu-id="fc35e-174">Windows 10 Creators Update (1703)</span><span class="sxs-lookup"><span data-stu-id="fc35e-174">Windows 10 Creators Update (1703)</span></span></td>
<td><span data-ttu-id="fc35e-175">DPI della visualizzazione in cui si trova la finestra dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-175">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="fc35e-176">Gli HWND di primo livello <span class="underline">e</span> figlio ricevono una notifica di modifica dpi</span><span class="sxs-lookup"><span data-stu-id="fc35e-176">Top-level <span class="underline">and</span> child HWNDs are notified of DPI change</span></span></li>
</ul>
<br/> <span data-ttu-id="fc35e-177"><span class="underline">Ridimensionamento DPI automatico di:</span>
</span><span class="sxs-lookup"><span data-stu-id="fc35e-177"><span class="underline">Automatic DPI scaling of:</span>
</span></span><ul>
<li><span data-ttu-id="fc35e-178">Area non client</span><span class="sxs-lookup"><span data-stu-id="fc35e-178">Non-client area</span></span></li>
<li><span data-ttu-id="fc35e-179">Bitmap disegnate da temi nei controlli comuni (comctl32 v6)</span><span class="sxs-lookup"><span data-stu-id="fc35e-179">Theme-drawn bitmaps in common controls (comctl32 V6)</span></span></li>
<li><span data-ttu-id="fc35e-180">Finestre di dialogo (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span><span class="sxs-lookup"><span data-stu-id="fc35e-180">Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a><span data-ttu-id="fc35e-181">Riconoscimento DPI per monitor (V1)</span><span class="sxs-lookup"><span data-stu-id="fc35e-181">Per Monitor (V1) DPI Awareness</span></span>

<span data-ttu-id="fc35e-182">Con Windows 8.1 è stata introdotta la modalità di riconoscimento DPI Per-Monitor V1 (PMv1).</span><span class="sxs-lookup"><span data-stu-id="fc35e-182">Per-Monitor V1 DPI awareness mode (PMv1) was introduced with Windows 8.1.</span></span> <span data-ttu-id="fc35e-183">Questa modalità di riconoscimento DPI è molto limitata e offre solo le funzionalità elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="fc35e-183">This DPI awareness mode is very limited and only offers the functionality listed below.</span></span> <span data-ttu-id="fc35e-184">È consigliabile che le applicazioni desktop usino la modalità di riconoscimento Per-Monitor V2, supportata in Windows 10 1703 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="fc35e-184">It is recommended that desktop applications use Per-Monitor v2 awareness mode, supported on Windows 10 1703 or above.</span></span>

<span data-ttu-id="fc35e-185">Il supporto iniziale per la consapevolezza per monitoraggio offre solo le applicazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc35e-185">The initial support for per-monitor awareness only offered applications the following:</span></span>

1.  <span data-ttu-id="fc35e-186">Gli HWND di primo livello ricevono una notifica di modifica DPI e forniscono nuove dimensioni suggerite</span><span class="sxs-lookup"><span data-stu-id="fc35e-186">Top-level HWNDs are notified of a DPI change and provided a new suggested size</span></span>
2.  <span data-ttu-id="fc35e-187">Non è possibile estendere l'interfaccia utente dell'applicazione con bitmap</span><span class="sxs-lookup"><span data-stu-id="fc35e-187">Windows will not bitmap stretch the application UI</span></span>
3.  <span data-ttu-id="fc35e-188">L'applicazione Visualizza tutte le visualizzazioni in pixel fisici (vedere virtualizzazione)</span><span class="sxs-lookup"><span data-stu-id="fc35e-188">The application sees all displays in physical pixels (see virtualization)</span></span>

<span data-ttu-id="fc35e-189">In Windows 10 1607 o versioni successive, le applicazioni PMv1 possono anche chiamare [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante WM \_ NCCREATE per richiedere che Windows ridimensioni correttamente l'area non client della finestra.</span><span class="sxs-lookup"><span data-stu-id="fc35e-189">On Windows 10 1607 or above, PMv1 applications may also call [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) during WM\_NCCREATE to request that Windows correctly scale the window's non-client area.</span></span>

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a><span data-ttu-id="fc35e-190">Supporto del ridimensionamento DPI per monitor per interfaccia utente/Framework</span><span class="sxs-lookup"><span data-stu-id="fc35e-190">Per Monitor DPI Scaling Support by UI Framework / Technology</span></span>

<span data-ttu-id="fc35e-191">La tabella seguente mostra il livello di supporto per la consapevolezza DPI per monitor offerto da diversi framework dell'interfaccia utente di Windows a partire da Windows 10 1703:</span><span class="sxs-lookup"><span data-stu-id="fc35e-191">The table below shows the level of per-monitor DPI awareness support offered by various Windows UI frameworks as of Windows 10 1703:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc35e-192">Framework/tecnologia</span><span class="sxs-lookup"><span data-stu-id="fc35e-192">Framework / Technology</span></span></th>
<th><span data-ttu-id="fc35e-193">Supporto</span><span class="sxs-lookup"><span data-stu-id="fc35e-193">Support</span></span></th>
<th><span data-ttu-id="fc35e-194">Versione sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fc35e-194">OS Version</span></span></th>
<th><span data-ttu-id="fc35e-195">Ridimensionamento DPI gestito da</span><span class="sxs-lookup"><span data-stu-id="fc35e-195">DPI Scaling handled by</span></span></th>
<th><span data-ttu-id="fc35e-196">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="fc35e-196">Further Reading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc35e-197">Piattaforma UWP (Universal Windows Platform)</span><span class="sxs-lookup"><span data-stu-id="fc35e-197">Universal Windows Platform (UWP)</span></span></td>
<td><span data-ttu-id="fc35e-198">Full</span><span class="sxs-lookup"><span data-stu-id="fc35e-198">Full</span></span></td>
<td><span data-ttu-id="fc35e-199">1607</span><span class="sxs-lookup"><span data-stu-id="fc35e-199">1607</span></span></td>
<td><span data-ttu-id="fc35e-200">Framework dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fc35e-200">UI framework</span></span></td>
<td><span data-ttu-id="fc35e-201"><a href="/windows/uwp/get-started/whats-a-uwp">Piattaforma UWP (Universal Windows Platform)</a></span><span class="sxs-lookup"><span data-stu-id="fc35e-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universal Windows Platform (UWP)</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc35e-202">Win32/controlli comuni non elaborati V6 (comctl32.dll)</span><span class="sxs-lookup"><span data-stu-id="fc35e-202">Raw Win32/Common Controls V6 (comctl32.dll)</span></span></td>
<td><ul>
<li><span data-ttu-id="fc35e-203">Messaggi di notifica delle modifiche DPI inviati a tutti gli HWND</span><span class="sxs-lookup"><span data-stu-id="fc35e-203">DPI change notification messages sent to all HWNDs</span></span></li>
<li><span data-ttu-id="fc35e-204">Il rendering degli asset disegnati con tema è corretto nei controlli comuni</span><span class="sxs-lookup"><span data-stu-id="fc35e-204">Theme-drawn assets render correctly in common controls</span></span></li>
<li><span data-ttu-id="fc35e-205">Ridimensionamento DPI automatico per le finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="fc35e-205">Automatic DPI scaling for dialogs</span></span></li>
</ul></td>
<td><span data-ttu-id="fc35e-206">1703</span><span class="sxs-lookup"><span data-stu-id="fc35e-206">1703</span></span></td>
<td><span data-ttu-id="fc35e-207">Applicazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-207">Application</span></span></td>
<td><span data-ttu-id="fc35e-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Esempio di GitHub</a></span><span class="sxs-lookup"><span data-stu-id="fc35e-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc35e-209">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fc35e-209">Windows Forms</span></span></td>
<td><span data-ttu-id="fc35e-210">Ridimensionamento automatico limitato per monitoraggio DPI per alcuni controlli</span><span class="sxs-lookup"><span data-stu-id="fc35e-210">Limited automatic per-monitor DPI scaling for some controls</span></span></td>
<td><span data-ttu-id="fc35e-211">1703</span><span class="sxs-lookup"><span data-stu-id="fc35e-211">1703</span></span></td>
<td><span data-ttu-id="fc35e-212">Framework dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fc35e-212">UI framework</span></span></td>
<td><span data-ttu-id="fc35e-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Supporto di valori DPI alti in Windows Form</a></span><span class="sxs-lookup"><span data-stu-id="fc35e-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">High DPI Support in Windows Forms</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc35e-214">Windows Presentation Framework (WPF)</span><span class="sxs-lookup"><span data-stu-id="fc35e-214">Windows Presentation Framework (WPF)</span></span></td>
<td><span data-ttu-id="fc35e-215">Per le applicazioni WPF native la scalabilità DPI di WPF ospitata in altri Framework e altri Framework ospitati in WPF non vengono ridimensionati automaticamente</span><span class="sxs-lookup"><span data-stu-id="fc35e-215">Native WPF applications will DPI scale WPF hosted in other frameworks and other frameworks hosted in WPF do not automatically scale</span></span></td>
<td><span data-ttu-id="fc35e-216">1607</span><span class="sxs-lookup"><span data-stu-id="fc35e-216">1607</span></span></td>
<td><span data-ttu-id="fc35e-217">Framework dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fc35e-217">UI framework</span></span></td>
<td><span data-ttu-id="fc35e-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Esempio di GitHub</a></span><span class="sxs-lookup"><span data-stu-id="fc35e-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc35e-219">GDI</span><span class="sxs-lookup"><span data-stu-id="fc35e-219">GDI</span></span></td>
<td><span data-ttu-id="fc35e-220">nessuno</span><span class="sxs-lookup"><span data-stu-id="fc35e-220">None</span></span></td>
<td><span data-ttu-id="fc35e-221">N/D</span><span class="sxs-lookup"><span data-stu-id="fc35e-221">N/A</span></span></td>
<td><span data-ttu-id="fc35e-222">Applicazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-222">Application</span></span></td>
<td><span data-ttu-id="fc35e-223">Vedere <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI scaling</a></span><span class="sxs-lookup"><span data-stu-id="fc35e-223">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc35e-224">GDI+</span><span class="sxs-lookup"><span data-stu-id="fc35e-224">GDI+</span></span></td>
<td><span data-ttu-id="fc35e-225">nessuno</span><span class="sxs-lookup"><span data-stu-id="fc35e-225">None</span></span></td>
<td><span data-ttu-id="fc35e-226">N/D</span><span class="sxs-lookup"><span data-stu-id="fc35e-226">N/A</span></span></td>
<td><span data-ttu-id="fc35e-227">Applicazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-227">Application</span></span></td>
<td><span data-ttu-id="fc35e-228">Vedere <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI scaling</a></span><span class="sxs-lookup"><span data-stu-id="fc35e-228">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc35e-229">MFC</span><span class="sxs-lookup"><span data-stu-id="fc35e-229">MFC</span></span></td>
<td><span data-ttu-id="fc35e-230">nessuno</span><span class="sxs-lookup"><span data-stu-id="fc35e-230">None</span></span></td>
<td><span data-ttu-id="fc35e-231">N/D</span><span class="sxs-lookup"><span data-stu-id="fc35e-231">N/A</span></span></td>
<td><span data-ttu-id="fc35e-232">Applicazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-232">Application</span></span></td>
<td><span data-ttu-id="fc35e-233">N/D</span><span class="sxs-lookup"><span data-stu-id="fc35e-233">N/A</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a><span data-ttu-id="fc35e-234">Aggiornamento di applicazioni esistenti</span><span class="sxs-lookup"><span data-stu-id="fc35e-234">Updating Existing Applications</span></span>

<span data-ttu-id="fc35e-235">Per aggiornare un'applicazione desktop esistente per gestire correttamente la scalabilità DPI, è necessario aggiornarla in modo che, come minimo, le parti importanti della relativa interfaccia utente vengano aggiornate per rispondere alle modifiche DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-235">In order to update an existing desktop application to handle DPI scaling properly, it needs to be updated such that, at a minimum, the important parts of its UI are updated to respond to DPI changes.</span></span>

<span data-ttu-id="fc35e-236">La maggior parte delle applicazioni desktop viene eseguita con la modalità di riconoscimento DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc35e-236">Most desktop applications run under system DPI awareness mode.</span></span> <span data-ttu-id="fc35e-237">Le applicazioni compatibili con DPI di sistema in genere si adattano al valore DPI dello schermo principale (la visualizzazione in cui si trovava la barra di sistema al momento dell'avvio della sessione di Windows).</span><span class="sxs-lookup"><span data-stu-id="fc35e-237">System-DPI-aware applications typically scale to the DPI of the primary display (the display that the system tray was located on at the time the Windows session was started).</span></span> <span data-ttu-id="fc35e-238">Quando viene modificato il valore DPI, Windows eseguirà il ridimensionamento dell'interfaccia utente di queste applicazioni, il che spesso comporta la sfocatura.</span><span class="sxs-lookup"><span data-stu-id="fc35e-238">When the DPI changes, Windows will bitmap stretch the UI of these applications, which often results in them being blurry.</span></span> <span data-ttu-id="fc35e-239">Quando si aggiorna un'applicazione compatibile con DPI di sistema in modo che sia compatibile con i valori DPI per monitor, il codice che gestisce il layout dell'interfaccia utente deve essere aggiornato in modo che venga eseguito non solo durante l'inizializzazione dell'applicazione, ma anche ogni volta che viene ricevuta una notifica di modifica DPI ([WM \_ DPICHANGED](wm-dpichanged.md) nel caso di Win32).</span><span class="sxs-lookup"><span data-stu-id="fc35e-239">When updating a System DPI-aware application to become per-monitor-DPI aware, the code which handles UI layout needs to be updated such that it is performed not only during application initialization, but also whenever a DPI change notification ([WM\_DPICHANGED](wm-dpichanged.md) in the case of Win32) is received.</span></span> <span data-ttu-id="fc35e-240">Ciò comporta in genere la rivisitazione di qualsiasi presupposto nel codice che l'interfaccia utente deve essere ridimensionata una sola volta.</span><span class="sxs-lookup"><span data-stu-id="fc35e-240">This typically involves revisiting any assumptions in the code that the UI only needs to be scaled once.</span></span>

<span data-ttu-id="fc35e-241">Inoltre, nel caso della programmazione Win32, molte API Win32 non dispongono di un valore DPI o di un contesto di visualizzazione in modo da restituire solo i valori relativi al valore DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc35e-241">Also, in the case of Win32 programming, many Win32 APIs do not have any DPI or display context so they will only return values relative to the System DPI.</span></span> <span data-ttu-id="fc35e-242">Può essere utile grep nel codice per cercare alcune di queste API e sostituirle con varianti compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-242">It can be useful to grep through your code to look for some of these APIs and replace them with DPI-aware variants.</span></span> <span data-ttu-id="fc35e-243">Di seguito sono riportate alcune delle API comuni con varianti compatibili con DPI:</span><span class="sxs-lookup"><span data-stu-id="fc35e-243">Some of the common APIs that have DPI-aware variants are:</span></span>



| <span data-ttu-id="fc35e-244">Versione con DPI singolo</span><span class="sxs-lookup"><span data-stu-id="fc35e-244">Single DPI version</span></span>   | <span data-ttu-id="fc35e-245">Versione Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="fc35e-245">Per-Monitor version</span></span>        |
|----------------------|----------------------------|
| <span data-ttu-id="fc35e-246">GetSystemMetrics</span><span class="sxs-lookup"><span data-stu-id="fc35e-246">GetSystemMetrics</span></span>     | <span data-ttu-id="fc35e-247">GetSystemMetricsForDpi</span><span class="sxs-lookup"><span data-stu-id="fc35e-247">GetSystemMetricsForDpi</span></span>     |
| <span data-ttu-id="fc35e-248">AdjustWindowRectEx</span><span class="sxs-lookup"><span data-stu-id="fc35e-248">AdjustWindowRectEx</span></span>   | <span data-ttu-id="fc35e-249">AdjustWindowRectExForDpi</span><span class="sxs-lookup"><span data-stu-id="fc35e-249">AdjustWindowRectExForDpi</span></span>   |
| <span data-ttu-id="fc35e-250">SystemParametersInfo</span><span class="sxs-lookup"><span data-stu-id="fc35e-250">SystemParametersInfo</span></span> | <span data-ttu-id="fc35e-251">SystemParametersInfoForDpi</span><span class="sxs-lookup"><span data-stu-id="fc35e-251">SystemParametersInfoForDpi</span></span> |
| <span data-ttu-id="fc35e-252">GetDpiForMonitor</span><span class="sxs-lookup"><span data-stu-id="fc35e-252">GetDpiForMonitor</span></span>     | <span data-ttu-id="fc35e-253">GetDpiForWindow</span><span class="sxs-lookup"><span data-stu-id="fc35e-253">GetDpiForWindow</span></span>            |



 

<span data-ttu-id="fc35e-254">È inoltre consigliabile eseguire la ricerca di dimensioni hardcoded nella codebase che presuppongono un valore DPI costante, sostituendo i valori con il codice che rappresenta correttamente la scalabilità DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-254">It is also a good idea to search for hard-coded sizes in your codebase that assume a constant DPI, replacing them with code that correctly accounts for DPI scaling.</span></span> <span data-ttu-id="fc35e-255">Di seguito è riportato un esempio in cui sono incorporati tutti i suggerimenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc35e-255">Below is an example that incorporates all of these suggestions:</span></span>

### <a name="example"></a><span data-ttu-id="fc35e-256">Esempio:</span><span class="sxs-lookup"><span data-stu-id="fc35e-256">Example:</span></span>

<span data-ttu-id="fc35e-257">Nell'esempio seguente viene illustrato un caso Win32 semplificato della creazione di un HWND figlio.</span><span class="sxs-lookup"><span data-stu-id="fc35e-257">The example below shows a simplified Win32 case of creating a child HWND.</span></span> <span data-ttu-id="fc35e-258">La chiamata a CreateWindow presuppone che l'applicazione sia in esecuzione a 96 DPI e che la dimensione o la posizione del pulsante non sia corretta a una DPI superiore:</span><span class="sxs-lookup"><span data-stu-id="fc35e-258">The call to CreateWindow assumes that the application is running at 96 DPI, and neither the button's size nor position will be correct at higher DPIs:</span></span>


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



<span data-ttu-id="fc35e-259">Il codice aggiornato seguente mostra:</span><span class="sxs-lookup"><span data-stu-id="fc35e-259">The updated code below shows:</span></span>

1.  <span data-ttu-id="fc35e-260">Il codice di creazione della finestra DPI ridimensiona la posizione e le dimensioni dell'elemento HWND figlio per il valore DPI della finestra padre</span><span class="sxs-lookup"><span data-stu-id="fc35e-260">The window-creation code DPI scaling the position and size of the child HWND for the DPI of its parent window</span></span>
2.  <span data-ttu-id="fc35e-261">Risposta alle modifiche DPI tramite il riposizionamento e il ridimensionamento dell'HWND figlio</span><span class="sxs-lookup"><span data-stu-id="fc35e-261">Responding to DPI change by repositioning and resizing the child HWND</span></span>
3.  <span data-ttu-id="fc35e-262">Dimensioni hardcoded rimosse e sostituite con codice che risponde alle modifiche DPI</span><span class="sxs-lookup"><span data-stu-id="fc35e-262">Hard-coded sizes removed and replaced with code that responds to DPI changes</span></span>


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



<span data-ttu-id="fc35e-263">Quando si aggiorna un'applicazione compatibile con DPI di sistema, alcuni passaggi comuni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc35e-263">When updating a System DPI-aware application, some common steps to follow are:</span></span>

1.  <span data-ttu-id="fc35e-264">Contrassegnare il processo come DPI compatibile con monitor (v2) usando un manifesto dell'applicazione (o un altro metodo, a seconda dei framework dell'interfaccia utente usati).</span><span class="sxs-lookup"><span data-stu-id="fc35e-264">Mark the process as per-monitor DPI aware (V2) using an application manifest (or other method, depending on the UI framework(s) used).</span></span>
2.  <span data-ttu-id="fc35e-265">Rendere la logica di layout dell'interfaccia utente riutilizzabile e spostarla all'esterno del codice di inizializzazione dell'applicazione in modo che possa essere riutilizzata quando si verifica una modifica DPI (WM \_ DPICHANGED nel caso della programmazione Windows (Win32)).</span><span class="sxs-lookup"><span data-stu-id="fc35e-265">Make UI layout logic reusable and move it out of application-initialization code such that it can be reused when a DPI change occurs (WM\_DPICHANGED in the case of Windows (Win32) programming).</span></span>
3.  <span data-ttu-id="fc35e-266">Invalidare il codice che presuppone che i dati sensibili a DPI (DPI/Fonts/sizes/e così via) non debbano mai essere aggiornati.</span><span class="sxs-lookup"><span data-stu-id="fc35e-266">Invalidate any code that assumes that DPI-sensitive data (DPI/fonts/sizes/etc.) never need to be updated.</span></span> <span data-ttu-id="fc35e-267">Si tratta di una procedura molto comune per memorizzare nella cache le dimensioni dei caratteri e i valori DPI durante l'inizializzazione del processo.</span><span class="sxs-lookup"><span data-stu-id="fc35e-267">It is a very common practice to cache font sizes and DPI values at process initialization.</span></span> <span data-ttu-id="fc35e-268">Quando si aggiorna un'applicazione in modo che diventi compatibile con i DPI del monitor, è necessario rivalutare i dati sensibili a DPI ogni volta che viene rilevato un nuovo valore DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-268">When updating an application to become per-monitor DPI aware, DPI-sensitive data must be reevaluated whenever a new DPI is encountered.</span></span>
4.  <span data-ttu-id="fc35e-269">Quando si verifica una modifica del valore DPI, ricarica o rirasterizza le risorse bitmap per il nuovo valore DPI o, facoltativamente, la bitmap estende gli asset attualmente caricati alla dimensione corretta.</span><span class="sxs-lookup"><span data-stu-id="fc35e-269">When a DPI change occurs, reload (or re-rasterize) any bitmap assets for the new DPI or, optionally, bitmap stretch the currently loaded assets to the correct size.</span></span>
5.  <span data-ttu-id="fc35e-270">Grep per le API che non sono Per-Monitor DPI in grado di riconoscere e sostituirle con Per-Monitor API compatibili con DPI (se applicabile).</span><span class="sxs-lookup"><span data-stu-id="fc35e-270">Grep for APIs that are not Per-Monitor DPI aware and replace them with Per-Monitor DPI-aware APIs (where applicable).</span></span> <span data-ttu-id="fc35e-271">Esempio: sostituire GetSystemMetrics con GetSystemMetricsForDpi.</span><span class="sxs-lookup"><span data-stu-id="fc35e-271">Example: replace GetSystemMetrics with GetSystemMetricsForDpi.</span></span>
6.  <span data-ttu-id="fc35e-272">Testare l'applicazione in un sistema a più visualizzazioni/multi-DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-272">Test your application on a multiple-display/multi-DPI system.</span></span>
7.  <span data-ttu-id="fc35e-273">Per tutte le finestre di primo livello dell'applicazione che non è possibile aggiornare per la scalabilità DPI corretta, usare il ridimensionamento DPI in modalità mista (descritto di seguito) per consentire l'estensione bitmap di queste finestre di primo livello da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc35e-273">For any top-level windows in your application that you are unable to update to properly DPI scale, use mixed-mode DPI scaling (described below) to allow bitmap stretching of these top-level windows by the system.</span></span>

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a><span data-ttu-id="fc35e-274">Ridimensionamento DPI Mixed-Mode (ridimensionamento DPI del processo secondario)</span><span class="sxs-lookup"><span data-stu-id="fc35e-274">Mixed-Mode DPI Scaling (Sub-Process DPI Scaling)</span></span>

<span data-ttu-id="fc35e-275">Quando si aggiorna un'applicazione per supportare la consapevolezza DPI per monitor, può essere talvolta impraticabile o Impossibile aggiornare ogni finestra dell'applicazione in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="fc35e-275">When updating an application to support per-monitor DPI awareness, it can sometimes become impractical or impossible to update every window in the application in one go.</span></span> <span data-ttu-id="fc35e-276">Questo può essere dovuto solo al tempo e al lavoro richiesto per l'aggiornamento e il test di tutte le interfacce utente o perché non si è proprietari di tutto il codice dell'interfaccia utente che è necessario eseguire (se l'applicazione potrebbe caricare l'interfaccia utente di terze parti).</span><span class="sxs-lookup"><span data-stu-id="fc35e-276">This can simply be due to the time and effort required to update and test all UI, or because you do not own all of the UI code that you need to run (if your application perhaps loads third-party UI).</span></span> <span data-ttu-id="fc35e-277">In queste situazioni, Windows offre un modo per semplificare il mondo della consapevolezza per monitoraggio consentendo di eseguire alcune delle finestre dell'applicazione (solo di primo livello) nella modalità di riconoscimento DPI originale, mentre si concentrano il tempo e l'energia nell'aggiornamento delle parti più importanti dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fc35e-277">In these situations, Windows offers a way to ease into the world of per-monitor awareness by letting you run some of your application windows (top-level only) in their original DPI-awareness mode while you focus your time and energy updating the more important parts of your UI.</span></span>

<span data-ttu-id="fc35e-278">Di seguito è riportata un'illustrazione di questo aspetto: si aggiorna l'interfaccia utente principale dell'applicazione ("finestra principale" nell'illustrazione) per eseguire con la consapevolezza DPI per monitor mentre si eseguono altre finestre nella modalità esistente ("finestra secondaria").</span><span class="sxs-lookup"><span data-stu-id="fc35e-278">Below is an illustration of what this could look like: you update your main application UI ("Main Window"  in the illustration) to run with per-monitor DPI awareness while you run other windows in their existing mode ("Secondary Window").</span></span>

![differenze nella scala dpi tra le modalità di riconoscimento](images/hub-page-illustrations.png)

<span data-ttu-id="fc35e-280">Prima dell'aggiornamento dell'anniversario di Windows 10 (1607), la modalità di riconoscimento DPI di un processo era una proprietà a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="fc35e-280">Prior to the Windows 10 Anniversary Update (1607), the DPI awareness mode of a process was a process-wide property.</span></span> <span data-ttu-id="fc35e-281">A partire dall'aggiornamento dell'anniversario di Windows 10, è ora possibile impostare questa proprietà per ogni finestra **di primo livello** .</span><span class="sxs-lookup"><span data-stu-id="fc35e-281">Beginning in the Windows 10 Anniversary Update, this property can now be set per **top-level** window.</span></span> <span data-ttu-id="fc35e-282">(Le finestre **figlio** devono continuare a corrispondere alle dimensioni di ridimensionamento dell'elemento padre). Una finestra di primo livello viene definita come una finestra senza elemento padre.</span><span class="sxs-lookup"><span data-stu-id="fc35e-282">(**Child** windows must continue to match the scaling size of their parent.) A top-level window is defined as a window with no parent.</span></span> <span data-ttu-id="fc35e-283">Si tratta in genere di una finestra "regolare" con i pulsanti Riduci a icona, Ingrandisci e Chiudi.</span><span class="sxs-lookup"><span data-stu-id="fc35e-283">This is typically a "regular" window with minimize, maximize, and close buttons.</span></span> <span data-ttu-id="fc35e-284">Lo scenario a cui è destinata la consapevolezza DPI del sottoprocesso è quello di avere un'interfaccia utente secondaria ridimensionata da Windows (con estensione bitmap), mentre è possibile concentrarsi sul tempo e sulle risorse per l'aggiornamento dell'interfaccia utente principale.</span><span class="sxs-lookup"><span data-stu-id="fc35e-284">The scenario that sub-process DPI awareness is intended for is to have secondary UI scaled by Windows (bitmap stretched) while you focus your time and resources on updating your primary UI.</span></span>

<span data-ttu-id="fc35e-285">Per abilitare la consapevolezza DPI del sottoprocesso, chiamare [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) prima e dopo le chiamate di creazione di finestre.</span><span class="sxs-lookup"><span data-stu-id="fc35e-285">To enable sub-process DPI awareness, call [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) before and after any window creation calls.</span></span> <span data-ttu-id="fc35e-286">La finestra creata verrà associata alla consapevolezza DPI impostata tramite SetThreadDpiAwarenessContext.</span><span class="sxs-lookup"><span data-stu-id="fc35e-286">The window that is created will be associated with the DPI awareness that you set via SetThreadDpiAwarenessContext.</span></span> <span data-ttu-id="fc35e-287">Utilizzare la seconda chiamata per ripristinare la consapevolezza DPI del thread corrente.</span><span class="sxs-lookup"><span data-stu-id="fc35e-287">Use the second call to restore the current thread s DPI awareness.</span></span>

<span data-ttu-id="fc35e-288">Quando si usa il ridimensionamento DPI del processo secondario, è possibile fare affidamento su Windows per eseguire alcune delle operazioni di scalabilità DPI per l'applicazione, che può aumentare la complessità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc35e-288">While using sub-process DPI scaling enables you to rely on Windows to do some of the DPI scaling for your application, it can increase the complexity of your application.</span></span> <span data-ttu-id="fc35e-289">È importante comprendere gli svantaggi di questo approccio e la natura delle complessità introdotte.</span><span class="sxs-lookup"><span data-stu-id="fc35e-289">It is important that you understand the drawbacks of this approach and nature of the complexities that it introduces.</span></span> <span data-ttu-id="fc35e-290">Per altre informazioni sulla consapevolezza DPI del sottoprocesso, vedere [ridimensionamento DPI in modalità mista e API compatibili con dpi.](high-dpi-improvements-for-desktop-applications.md)</span><span class="sxs-lookup"><span data-stu-id="fc35e-290">For more information about sub-process DPI awareness, see [Mixed-Mode DPI Scaling and DPI-aware APIs.](high-dpi-improvements-for-desktop-applications.md)</span></span>

## <a name="testing-your-changes"></a><span data-ttu-id="fc35e-291">Test delle modifiche</span><span class="sxs-lookup"><span data-stu-id="fc35e-291">Testing Your Changes</span></span>

<span data-ttu-id="fc35e-292">Dopo aver aggiornato l'applicazione in modo che sia compatibile con i valori DPI per monitor, è importante convalidare l'applicazione in modo che risponda correttamente alle modifiche DPI in un ambiente con DPI misto.</span><span class="sxs-lookup"><span data-stu-id="fc35e-292">After you have updated your application to become per-monitor DPI aware, it is important to validate your application properly responds to DPI changes in a mixed-DPI environment.</span></span> <span data-ttu-id="fc35e-293">Di seguito sono riportate alcune specifiche da testare:</span><span class="sxs-lookup"><span data-stu-id="fc35e-293">Some specifics to test include:</span></span>

1.  <span data-ttu-id="fc35e-294">Spostare le finestre delle applicazioni tra le visualizzazioni di valori DPI diversi</span><span class="sxs-lookup"><span data-stu-id="fc35e-294">Moving application windows back and forth between displays of different DPI values</span></span>
2.  <span data-ttu-id="fc35e-295">Avvio dell'applicazione in visualizzazione di valori DPI diversi</span><span class="sxs-lookup"><span data-stu-id="fc35e-295">Starting your application on displays of different DPI values</span></span>
3.  <span data-ttu-id="fc35e-296">Modifica del fattore di scala per il monitoraggio durante l'esecuzione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-296">Changing the scale factor for your monitor while the application is running</span></span>
4.  <span data-ttu-id="fc35e-297">Modifica della visualizzazione usata come schermo principale, _disconnettersi da Windows_, quindi eseguire nuovamente il test dell'applicazione dopo aver eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="fc35e-297">Changing the display that you use as the primary display, _signing out of Windows_, then re-testing your application after signing back in.</span></span> <span data-ttu-id="fc35e-298">Questa operazione è particolarmente utile per trovare codice che usa dimensioni/dimensioni hardcoded.</span><span class="sxs-lookup"><span data-stu-id="fc35e-298">This is particularly useful in finding code that uses hard-coded sizes/dimensions.</span></span>

## <a name="common-pitfalls-win32"></a><span data-ttu-id="fc35e-299">Insidie comuni (Win32)</span><span class="sxs-lookup"><span data-stu-id="fc35e-299">Common Pitfalls (Win32)</span></span>

<span data-ttu-id="fc35e-300">**Non usare il rettangolo suggerito fornito in WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="fc35e-300">**Not using the suggested rectangle that is provided in WM\_DPICHANGED**</span></span>

<span data-ttu-id="fc35e-301">Quando Windows invia alla finestra dell'applicazione un messaggio [**WM \_ DPICHANGED**](wm-dpichanged.md) , questo messaggio include un rettangolo suggerito da usare per ridimensionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="fc35e-301">When Windows sends your application window a [**WM\_DPICHANGED**](wm-dpichanged.md) message, this message includes a suggested rectangle that you should use to resize your window.</span></span> <span data-ttu-id="fc35e-302">È fondamentale che l'applicazione usi questo rettangolo per ridimensionarsi, in quanto:</span><span class="sxs-lookup"><span data-stu-id="fc35e-302">It is critical that your application use this rectangle to resize itself, as this will:</span></span>

1.  <span data-ttu-id="fc35e-303">Verificare che il cursore del mouse si trovi nella stessa posizione relativa della finestra durante il trascinamento tra le visualizzazioni</span><span class="sxs-lookup"><span data-stu-id="fc35e-303">Ensure that the mouse cursor will stay in the same relative position on the Window when dragging between displays</span></span>
2.  <span data-ttu-id="fc35e-304">Impedire alla finestra dell'applicazione di entrare in un ciclo di modifica dpi ricorsivo in cui una modifica dpi attiva una modifica DPI successiva, che attiva ancora un'altra variazione DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-304">Prevent the application window from getting into a recursive dpi-change cycle where one DPI change triggers a subsequent DPI change, which triggers yet another DPI change.</span></span>

<span data-ttu-id="fc35e-305">Se sono presenti requisiti specifici dell'applicazione che impediscono l'uso del rettangolo suggerito fornito da Windows nel messaggio WM \_ DPICHANGED, vedere [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span><span class="sxs-lookup"><span data-stu-id="fc35e-305">If you have application-specific requirements that prevent you from using the suggested rectangle that Windows provides in the WM\_DPICHANGED message, see [**WM\_GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span></span> <span data-ttu-id="fc35e-306">Questo messaggio può essere usato per assegnare a Windows una dimensione desiderata da usare una volta che si è verificata la modifica del valore DPI, evitando comunque i problemi descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="fc35e-306">This message can be used to give Windows a desired size you'd like used once the DPI change has occurred, while still avoiding the issues described above.</span></span>

<span data-ttu-id="fc35e-307">**Mancanza di documentazione sulla virtualizzazione**</span><span class="sxs-lookup"><span data-stu-id="fc35e-307">**Lack of documentation about virtualization**</span></span>

<span data-ttu-id="fc35e-308">Quando un HWND o un processo viene eseguito come valore DPI incompatibile o compatibile con DPI di sistema, può essere bitmap esteso da Windows.</span><span class="sxs-lookup"><span data-stu-id="fc35e-308">When an HWND or process is running as either DPI unaware or system DPI aware, it can be bitmap stretched by Windows.</span></span> <span data-ttu-id="fc35e-309">Quando si verifica questa situazione, Windows ridimensiona e converte le informazioni sensibili a DPI da alcune API allo spazio delle coordinate del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="fc35e-309">When this happens, Windows scales and converts DPI-sensitive information from some APIs to the coordinate space of the calling thread.</span></span> <span data-ttu-id="fc35e-310">Se, ad esempio, un thread con compatibilità con DPI esegue una query sulle dimensioni dello schermo mentre è in esecuzione in un display a DPI elevato, Windows virtualizza la risposta assegnata all'applicazione come se la schermata si trovasse in unità 96 DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-310">For example, if a DPI-unaware thread queries the screen size while running on a high-DPI display, Windows will virtualize the answer given to the application as if the screen were in 96 DPI units.</span></span> <span data-ttu-id="fc35e-311">In alternativa, quando un thread compatibile con DPI di sistema interagisce con una visualizzazione con un valore DPI diverso da quello in uso quando è stata avviata la sessione dell'utente corrente, in Windows verrà eseguita la scalabilità di alcune chiamate API nello spazio delle coordinate usato da HWND se era in esecuzione con il fattore di scala DPI originale.</span><span class="sxs-lookup"><span data-stu-id="fc35e-311">Alternatively, when a System DPI-aware thread is interacting with a display at a different DPI than was in use when the current user's session was started, Windows will DPI-scale some API calls into the coordinate space that the HWND would be using if it were running at its original DPI scale factor.</span></span>

<span data-ttu-id="fc35e-312">Quando si aggiorna l'applicazione desktop alla scala DPI, può essere difficile capire quali chiamate API possono restituire valori virtualizzati in base al contesto del thread. Queste informazioni attualmente non sono sufficientemente documentate da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fc35e-312">When you update your desktop application to DPI scale properly, it can difficult to know which API calls can return virtualized values based on the thread context; this information is not currently sufficiently documented by Microsoft.</span></span> <span data-ttu-id="fc35e-313">Tenere presente che se si chiama qualsiasi API di sistema da un contesto del thread compatibile con DPI o con DPI, il valore restituito potrebbe essere virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="fc35e-313">Be aware that if you call any system API from a DPI-unaware or system-DPI-aware thread context, the return value might be virtualized.</span></span> <span data-ttu-id="fc35e-314">Pertanto, assicurarsi che il thread sia in esecuzione nel contesto DPI previsto quando si interagisce con lo schermo o con le singole finestre.</span><span class="sxs-lookup"><span data-stu-id="fc35e-314">As such, make sure your thread is running in the DPI context you expect when interacting with the screen or individual windows.</span></span> <span data-ttu-id="fc35e-315">Quando si modifica temporaneamente il contesto DPI di un thread usando [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), assicurarsi di ripristinare il contesto precedente al termine dell'operazione per evitare di causare un comportamento errato in un'altra posizione nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc35e-315">When temporarily changing a thread's DPI context using [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), be sure to restore the old context when you're done to avoid causing incorrect behavior elsewhere in your application.</span></span>

<span data-ttu-id="fc35e-316">**Molte API Windows non dispongono di un contesto DPI**</span><span class="sxs-lookup"><span data-stu-id="fc35e-316">**Many Windows APIs do not have an DPI context**</span></span>

<span data-ttu-id="fc35e-317">Molte API Windows legacy non includono un contesto DPI o HWND come parte dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fc35e-317">Many legacy Windows APIs do not include a DPI or HWND context as part of their interface.</span></span> <span data-ttu-id="fc35e-318">Di conseguenza, gli sviluppatori devono spesso eseguire ulteriori operazioni per gestire il ridimensionamento di qualsiasi informazione sensibile a DPI, ad esempio dimensioni, punti o icone.</span><span class="sxs-lookup"><span data-stu-id="fc35e-318">As a result, developers often have to do additional work to handle the scaling of any DPI-sensitive information, such as sizes, points, or icons.</span></span> <span data-ttu-id="fc35e-319">Gli sviluppatori che usano [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) , ad esempio, devono avere icone con estensione bitmap caricate o usare API alternative per caricare icone di dimensioni corrette per il valore dpi appropriato, ad esempio [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span><span class="sxs-lookup"><span data-stu-id="fc35e-319">As an example, developers using [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) must either bitmap stretch loaded icons or use alternate APIs to load correctly-sized icons for the appropriate DPI, such as [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span></span>

<span data-ttu-id="fc35e-320">**Ripristino forzato della consapevolezza DPI a livello di processo**</span><span class="sxs-lookup"><span data-stu-id="fc35e-320">**Forced reset of process-wide DPI awareness**</span></span>

<span data-ttu-id="fc35e-321">In generale, la modalità di riconoscimento DPI del processo non può essere modificata dopo l'inizializzazione del processo.</span><span class="sxs-lookup"><span data-stu-id="fc35e-321">In general, the DPI awareness mode of your process cannot be changed after process initialization.</span></span> <span data-ttu-id="fc35e-322">Windows può, tuttavia, modificare forzatamente la modalità di riconoscimento DPI del processo se si tenta di interrompere il requisito in cui tutti gli HWND in una struttura ad albero della finestra hanno la stessa modalità di riconoscimento DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-322">Windows can, however, forcibly change the DPI awareness mode of your process if you attempt to break the requirement that all HWNDs in a window tree have the same DPI awareness mode.</span></span> <span data-ttu-id="fc35e-323">In tutte le versioni di Windows, a partire da Windows 10 1703, non è possibile avere HWND diversi in una struttura ad albero HWND eseguita in modalità di riconoscimento DPI diverse.</span><span class="sxs-lookup"><span data-stu-id="fc35e-323">On all versions of Windows, as of Windows 10 1703, it is not possible to have different HWNDs in an HWND tree run in different DPI awareness modes.</span></span> <span data-ttu-id="fc35e-324">Se si tenta di creare una relazione padre-figlio che interrompe questa regola, è possibile reimpostare la consapevolezza DPI dell'intero processo.</span><span class="sxs-lookup"><span data-stu-id="fc35e-324">If you attempt to create a child-parent relationship that breaks this rule, the DPI awareness of the entire process can be reset.</span></span> <span data-ttu-id="fc35e-325">Questa operazione può essere attivata da:</span><span class="sxs-lookup"><span data-stu-id="fc35e-325">This can be triggered by:</span></span>

1.  <span data-ttu-id="fc35e-326">Chiamata CreateWindow in cui la finestra padre passata è di una modalità di riconoscimento DPI diversa rispetto al thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="fc35e-326">A CreateWindow call where the passed in parent window is of a different DPI awareness mode than the calling thread.</span></span>
2.  <span data-ttu-id="fc35e-327">Una chiamata a padre dove le due finestre sono associate a diverse modalità di riconoscimento DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-327">A SetParent call where the two windows are associated with different DPI awareness modes.</span></span>

<span data-ttu-id="fc35e-328">La tabella seguente mostra cosa accade se si tenta di violare questa regola:</span><span class="sxs-lookup"><span data-stu-id="fc35e-328">The table below shows what happens if you attempt to violate this rule:</span></span>



| <span data-ttu-id="fc35e-329">Operazione</span><span class="sxs-lookup"><span data-stu-id="fc35e-329">Operation</span></span>                 | <span data-ttu-id="fc35e-330">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fc35e-330">Windows 8.1</span></span>                                  | <span data-ttu-id="fc35e-331">Windows 10 (1607 e versioni precedenti)</span><span class="sxs-lookup"><span data-stu-id="fc35e-331">Windows 10 (1607 and earlier)</span></span>                | <span data-ttu-id="fc35e-332">Windows 10 (1703 e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="fc35e-332">Windows 10 (1703 and later)</span></span>                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| <span data-ttu-id="fc35e-333">CreateWindow (in-process)</span><span class="sxs-lookup"><span data-stu-id="fc35e-333">CreateWindow (In-Proc)</span></span>    | <span data-ttu-id="fc35e-334">N/D</span><span class="sxs-lookup"><span data-stu-id="fc35e-334">N/A</span></span>                                          | <span data-ttu-id="fc35e-335">**Eredita figlio** (modalità mista)</span><span class="sxs-lookup"><span data-stu-id="fc35e-335">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="fc35e-336">**Eredita figlio** (modalità mista)</span><span class="sxs-lookup"><span data-stu-id="fc35e-336">**Child inherits** (mixed mode)</span></span>              |
| <span data-ttu-id="fc35e-337">CreateWindow (cross-process)</span><span class="sxs-lookup"><span data-stu-id="fc35e-337">CreateWindow (Cross-Proc)</span></span> | <span data-ttu-id="fc35e-338">**Reimpostazione forzata** (del processo del chiamante)</span><span class="sxs-lookup"><span data-stu-id="fc35e-338">**Forced reset** (of caller's process)</span></span>       | <span data-ttu-id="fc35e-339">**Eredita figlio** (modalità mista)</span><span class="sxs-lookup"><span data-stu-id="fc35e-339">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="fc35e-340">**Reimpostazione forzata** (del processo del chiamante)</span><span class="sxs-lookup"><span data-stu-id="fc35e-340">**Forced reset** (of caller's process)</span></span>       |
| <span data-ttu-id="fc35e-341">Padre (in-process)</span><span class="sxs-lookup"><span data-stu-id="fc35e-341">SetParent (In-Proc)</span></span>       | <span data-ttu-id="fc35e-342">N/D</span><span class="sxs-lookup"><span data-stu-id="fc35e-342">N/A</span></span>                                          | <span data-ttu-id="fc35e-343">**Reimpostazione forzata** (del processo corrente)</span><span class="sxs-lookup"><span data-stu-id="fc35e-343">**Forced reset** (of current process)</span></span>        | <span data-ttu-id="fc35e-344">**Esito negativo** (errore \_ stato non valido \_ )</span><span class="sxs-lookup"><span data-stu-id="fc35e-344">**Fail** (ERROR\_INVALID\_STATE)</span></span>             |
| <span data-ttu-id="fc35e-345">Padre (cross-process)</span><span class="sxs-lookup"><span data-stu-id="fc35e-345">SetParent (Cross-Proc)</span></span>    | <span data-ttu-id="fc35e-346">**Reimpostazione forzata** (del processo della finestra figlio)</span><span class="sxs-lookup"><span data-stu-id="fc35e-346">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="fc35e-347">**Reimpostazione forzata** (del processo della finestra figlio)</span><span class="sxs-lookup"><span data-stu-id="fc35e-347">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="fc35e-348">**Reimpostazione forzata** (del processo della finestra figlio)</span><span class="sxs-lookup"><span data-stu-id="fc35e-348">**Forced reset** (of child window's process)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fc35e-349">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc35e-349">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc35e-350">Riferimento all'API DPI elevato</span><span class="sxs-lookup"><span data-stu-id="fc35e-350">High DPI API Reference</span></span>](high-dpi-reference.md)
</dt> <dt>

[<span data-ttu-id="fc35e-351">Ridimensionamento DPI in modalità mista e API compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="fc35e-351">Mixed-Mode DPI Scaling and DPI-aware APIs.</span></span>](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

