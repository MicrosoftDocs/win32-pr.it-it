---
description: A partire da Windows 8, DirectX SDK è incluso come parte del Windows SDK.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Dov'è DirectX SDK?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c070313c5c7f6105afaf7b629ff1ca2618a469fb
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314624"
---
# <a name="where-is-the-directx-sdk"></a>Dov'è DirectX SDK?

A partire da Windows 8, DirectX SDK è incluso come parte del Windows SDK.

In origine, DirectX SDK è stato creato come piattaforma a prestazioni elevate per lo sviluppo di giochi su Windows. Man mano che le tecnologie DirectX sono maturate, diventano rilevanti per una più ampia gamma di applicazioni. Attualmente, la disponibilità dell'hardware Direct3D nei computer consente anche alle applicazioni desktop tradizionali di utilizzare l'accelerazione hardware grafica. In parallelo, le tecnologie DirectX sono più integrate in Windows. DirectX è ora una parte fondamentale di Windows.

Dato che Windows SDK è il principale SDK per sviluppatori per Windows, DirectX è ora incluso nel kit. Puoi usare Windows SDK per creare giochi eccezionali per Windows. Per scaricare Windows 8. x SDK o Windows 10 SDK, vedere [Windows SDK e l'archivio dell'emulatore](https://developer.microsoft.com/windows/downloads/sdk-archive).

Le tecnologie e gli strumenti seguenti, in precedenza parte di DirectX SDK, fanno ora parte del Windows SDK.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tecnologia o strumento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Componenti grafici Windows<br/></td>
<td>Le intestazioni e le librerie per <a href="/windows/desktop/direct3d">Direct3D</a> e altre API grafiche di Windows, ad esempio <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, sono disponibili nella Windows SDK. <br/>
<blockquote>
[!Note]<br />
Le librerie di utilità D3DX9/D3DX10/D3DX11 deprecate sono disponibili tramite <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, ma esistono anche alcune <a href="https://walbourn.github.io/living-without-d3dx/">alternative open source</a>. La libreria dell'utilità D3DCSX DirectCompute e la DLL ridistribuibile sono disponibili nell'Windows SDK. D3DX12 è disponibile in <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilatore HLSL (FXC.EXE)<br/></td>
<td>Il compilatore <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> è uno strumento della sottodirectory Architecture appropriata nella cartella bin del Windows SDK.<br/>
<blockquote>
[!Note]<br />
L'API D3DCompiler e la DLL ridistribuibile sono disponibili nell'Windows SDK.
</blockquote>
<br/><br/>Per lo sviluppo di DirectX 12, usare DXCompiler nel Windows SDK e ospitato su [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).
<br/></td>
</tr>
<tr class="odd">
<td><span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX per Windows<br/></td>
<td>Una sostituzione dello strumento PIX per Windows è ora una funzionalità di Microsoft Visual Studio, denominata debugger grafica di Visual Studio. Questa funzionalità ha migliorato notevolmente l'usabilità, il supporto per Windows 8 e Direct3D 11,1 e l'integrazione con le funzionalità di Microsoft Visual Studio tradizionali come gli stack di chiamate e le finestre di debug per il debug <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> . Per altre informazioni su questa nuova funzionalità, vedere <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">debug della grafica DirectX</a>.<br/><br/>Per lo sviluppo di DirectX 12, vedere la generazione più recente di <a href="https://devblogs.microsoft.com/pix/">pix in Windows</a><br/></td>
</tr>
<tr class="even">
<td><span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> per Windows<br/></td>
<td>L'API <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> è ora un componente di sistema in Windows 8. x e Windows 10. Le intestazioni e le librerie per XAudio2 sono disponibili nell'Windows SDK. Per il supporto di Windows 7, vedere <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> per Windows<br/></td>
<td>L'API <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1,4 è ora un componente di sistema in Windows 8. x e Windows 10. Le intestazioni e le librerie per XInput sono disponibili nell'Windows SDK.<br/>
<blockquote>
[!Note]<br />
9.1.0 XInput legacy è disponibile anche come parte di Windows 7 o versione successiva.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br/></td>
<td>La versione più recente di XNAMATH, che viene aggiornata per i nuovi set di istruzioni e ARM/ARM64, è ora <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a>. Le intestazioni per DirectXMath sono disponibili nell'Windows SDK e in <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Pannello di controllo DirectX e Visualizzatore funzionalità DirectX<br/></td>
<td>Le utilità pannello di controllo DirectX e Visualizzatore funzionalità DirectX sono incluse nella sottodirectory dell'architettura appropriata nella cartella bin del Windows SDK. Il Visualizzatore funzionalità DirectX è disponibile anche in <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="XACT"></span><span id="xact"></span>XACT<br/></td>
<td>Lo strumento multipiattaforma audio Xbox (XACT) non è più supportato per l'utilizzo in Windows.<br/></td>
</tr>
<tr class="odd">
<td><span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Esplora giochi</a> e GDFMAKER<br/></td>
<td>L'API di <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Esplora giochi</a> presenta giochi agli utenti di Windows. L'API di Esplora giochi è supportata solo in Windows Vista e Windows 7. Per dichiarare le classificazioni dei giochi per le app di Windows Store, è possibile usare lo GDFMAKER.EXE strumento di definizione dei file di definizione dei giochi <br/> Lo strumento di elaborazione dei file di definizione del gioco (GDFMaker.exe) è incluso nella sottodirectory x86 sotto la cartella bin nel Windows SDK e supporta sia le applicazioni Windows Store sia le applicazioni desktop Win32.<br/>
<br/></td>
</tr>
<tr class="even">
<td><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Esempi<br/></td>
<td>È possibile trovare applicazioni di esempio che evidenziano le tecnologie DirectX 12 in Windows nel repository di <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">esempi DirectX</a> . La maggior parte degli esempi per le versioni precedenti di Direct3D è disponibile anche online. Per ulteriori informazioni su questi esempi, vedere il <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">Catalogo degli esempi di DirectX SDK</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1,1 gestito<br/></td>
<td>Gli assembly DirectX .NET sono deprecati e non sono consigliati per l'uso da parte di nuove applicazioni. Sono disponibili diverse alternative. Vedere <a href="https://walbourn.github.io/directx-and-net/">DirectX e .NET</a>. <br/></td>
</tr>
</tbody>
</table>



 

Il Legacy DirectX SDK è disponibile per il download dall' [area download Microsoft](https://go.microsoft.com/fwlink/?LinkId=226640) , se necessario, ma non è consigliabile usare per i nuovi progetti.

> [!Note]  
> Non è possibile installare DirectX SDK se è già installata una certa versione del pacchetto ridistribuibile Visual C++ 2010. Per ulteriori informazioni su e su una soluzione per risolvere questo problema, vedere [l'errore "S1023" durante l'installazione di DirectX SDK (giugno 2010)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Uso di progetti DirectX SDK con Visual Studio

Gli esempi di DirectX SDK di giugno 2010 sono supportati con SKU di Visual Studio Premium (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 o Microsoft Visual Studio Ultimate 2013) in Windows 7 e Windows 8 e versioni successive. A causa della transizione delle intestazioni e delle librerie DirectX nella Windows SDK, sono necessarie modifiche alle impostazioni del progetto per compilare correttamente questi esempi con la modalità di creazione di un pacchetto di Windows 8 SDK e versioni successive con gli SKU di Visual Studio Premium.

Questi passaggi si applicano anche ai propri progetti che dipendono da DirectX SDK.

1.  Verificare che nel computer di sviluppo sia installata la versione di giugno 2010 di DirectX SDK. Se si installa in un computer che esegue Windows 8 e versioni successive, verrà richiesto di abilitare .NET 3,5 come installazione dei prerequisiti per DirectX SDK.

    > [!Note]  
    > Non è possibile installare DirectX SDK se è già installata una certa versione del pacchetto ridistribuibile Visual C++ 2010. Per ulteriori informazioni su e su una soluzione per risolvere questo problema, vedere [l'errore "S1023" durante l'installazione di DirectX SDK (giugno 2010)](https://support.microsoft.com/kb/2728613).

     

2.  Assicurarsi di usare uno degli SKU di Visual Studio Premium. Microsoft Visual Studio Express 2012 per Windows 8 o Microsoft Visual Studio Express 2013 per Windows non compilerà applicazioni desktop Windows 8 e versioni successive, ad esempio gli esempi di DirectX SDK. Per installare uno degli SKU di Visual Studio Premium, vedere Download di [Visual Studio](https://www.microsoft.com/visualstudio/11/downloads) e seguire le istruzioni.

3.  Usare il browser di esempio di DirectX SDK per installare i file di progetto per l'esempio desiderato. Aprire il file di soluzione compatibile Microsoft Visual Studio 2010 dell'esempio (con suffisso **\_ 2010**).

4.  Se si apre l'esempio in un sistema in cui è installato solo Microsoft Visual Studio 2012 o Microsoft Visual Studio 2013, viene ricevuto il messaggio seguente: "Questa soluzione contiene uno o più progetti che usano una versione precedente del compilatore e delle librerie VC + +. Ogni progetto può essere aggiornato in modo da usare il compilatore e le librerie di VC + + (V110). " Scegliere l'opzione **Aggiorna** da questa finestra di dialogo per aggiornare prima di aprire il progetto.

    In caso contrario, è possibile aggiornare il compilatore e le librerie di Visual Studio 2012 o Visual Studio 2013 C++ 11 dopo il caricamento facendo clic con il pulsante destro del mouse sulla soluzione e scegliendo **Aggiorna progetti VC + +**.

5.  D3DX non è considerato l'API canonica per l'uso di Direct3D in Windows 8 e versioni successive e pertanto non è incluso nella Windows SDK corrispondente. Esaminare le soluzioni alternative per l'uso dell'API Direct3D. Per i progetti legacy, ad esempio gli esempi di Windows 7 (e versioni precedenti) di DirectX SDK, i passaggi seguenti sono necessari per compilare applicazioni con D3DX usando DirectX SDK:

    1.  Modificare le directory di **VC + +** del progetto come indicato di seguito per usare l'ordine corretto per le intestazioni e le librerie dell'SDK.

        <dl> i. Aprire le **Proprietà** del progetto e selezionare la pagina **directory di VC + +** .  
        ii. Selezionare **tutte le configurazioni e tutte le piattaforme**.  
        iii. Impostare le directory come indicato di seguito:

        -   Directory eseguibili: **<inherit from parent or project defaults>** (nell'elenco a discesa sul lato destro)
        -   Directory di inclusione: **$ (IncludePath); $ (DXSDK \_ dir) include**
        -   Includi directory libreria: **$ (LibraryPath); $ (DXSDK \_ dir) lib \\ x86**

          
        iv. Fare clic su **Applica**.  
        v. Scegliere la **piattaforma x64**.  
        vi. Impostare la **directory della libreria** come indicato di seguito:

        -   Directory della libreria: **$ (LibraryPath); $ (DXSDK \_ dir) lib \\ x64**

          
        </dl>

    2.  Ogni volta che "d3dx9. h", "d3dx10. h" o "D3DX11. h" sono inclusi nel progetto, assicurarsi di includere in modo esplicito "d3d9. h", "d3d10. h" e "dxgi. h" oppure "d3d11. h" e "dxgi. h" per assicurarsi di selezionare la versione più recente. Se necessario, è possibile disabilitare l' **avviso C4005** ; Tuttavia, questo avviso indica che si sta usando la versione precedente di queste intestazioni.
    3.  Rimuovere tutti i riferimenti a DXGIType. h nel progetto. Questa intestazione non esiste nel Windows SDK e la versione di DirectX SDK è in conflitto con il nuovo Winerror. h.
    4.  Tutte le dll D3DX vengono installate nel computer di sviluppo dall'installazione di DirectX SDK. Assicurarsi che le dipendenze D3DX necessarie vengano ridistribuite con qualsiasi esempio o con l'applicazione se viene spostata in un altro computer.
    5.  Tenere presente che le tecnologie di sostituzione per gli usi correnti di D3DX11 includono [DirectXTex](https://github.com/Microsoft/DirectXTex), [DirectXTK](https://github.com/Microsoft/DirectXTK), [DirectXMesh](https://github.com/Microsoft/DirectXMesh)e [UVAtlas](https://github.com/Microsoft/UVAtlas). D3DXMath viene sostituito da [DirectXMath](./dxmath/directxmath-portal.md).

6.  Assicurarsi di usare la nuova versione del compilatore HLSL shader osservando le condizioni seguenti:

    1.  Se si modifica la directory eseguibile in base al passaggio 5, le compilazioni di progetto utilizzeranno FXC dall'installazione Windows SDK. Tenere presente che i file HLSL sono ora ufficialmente riconosciuti da Visual Studio. È possibile aggiungerli come file di progetto e impostare le opzioni del compilatore tramite il sistema del progetto.

    2.  La chiamata della compilazione in fase di esecuzione tramite la DLL legacy D3DX utilizzerà la versione precedente non corretta del compilatore HLSL. Sostituire tutti i riferimenti alle \* API D3DXCompile, D3DX10Compile \* e D3DX11Compile \* nel codice con la funzione D3DCompile in D3DCOMPILER \_46.DLL o D3DCOMPILER \_47.DLL.

    3.  Tutti i progetti che usano la compilazione shader di run-time devono avere D3DCOMPILER \_xx.DLL copiati nel percorso eseguibile locale per il progetto. Questa dll è disponibile in questa sottodirectory dell'installazione di Windows SDK in **% ProgramFiles (x86)% \\ Windows Kit \\ 8,0 \\ Redist \\ D3D \\ <arch>** o **% ProgramFiles ( \\ \\ \\ \\ \\ <arch> x86)% Windows Kit 8,1 Redist** in cui **<arch>** è **x86** e **x64**.

        Il \_47.DLL D3DCOMPILER46.DLL o D3DCOMPILER \_ dal Windows SDK non è un componente di sistema e non deve essere copiato nella directory di sistema di Windows. È possibile ridistribuire questa DLL ad altri computer con l'applicazione come DLL side-by-side.

7.  Qualsiasi progetto che usa l'API di XInput ed è progettato per essere eseguito in Windows 7 o versioni precedenti di Windows deve usare la versione legacy (9.1.0) o deve includere in modo esplicito le intestazioni e le librerie per questo componente da DirectX SDK. L'intestazione XInput e XINPUT. LIB incluse nel Windows SDK destinate solo alla versione (1,4) che viene fornita come parte di Windows 8 e versioni successive. La stessa intestazione può essere usata con XINPUT9 \_ 1 \_ 0. lib per usare la versione legacy, inclusa nelle versioni precedenti di Windows. La versione legacy di XInput non rileva le funzionalità complete o l'audio integrato del controller di supporto. Pertanto, se è necessario il supporto per queste funzionalità, è necessario usare la versione di DirectX SDK (1,3).

    Per usare l'API XInput di livello completo completa, è consigliabile usare `#include` direttamente le intestazioni XInput specifiche da DirectX SDK:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... e nelle opzioni del linker per le dipendenze aggiuntive, collegarsi direttamente alla libreria XInput di DirectX SDK:

    **% DXSDK \_ dir% include \\ <arch> \\ XInput. lib**

    Il \_ file binario3.DLL XINPUT1 viene installato nelle directory di sistema di Windows tramite l'installazione di DirectX SDK nel computer di sviluppo. Sarà necessario ridistribuire il file binario con l'applicazione usando l'installazione di DirectX SDK da DirectX SDK.

8.  Tutti i progetti che usano l'API di XAudio2 e sono progettati per l'esecuzione in Windows 7 o versioni precedenti di Windows devono usare la versione precedente (9.1.0) o includere in modo esplicito le intestazioni e le librerie per questo componente da DirectX SDK. Le intestazioni e le librerie XAudio2 incluse nel Windows SDK sono destinate solo alla versione (2,8) inclusa come parte di Windows 8.

    Ad esempio, con XAudio2, è consigliabile usare `#include` direttamente le intestazioni XAudio2 specifiche da DirectX SDK:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... e nelle opzioni del linker per le dipendenze aggiuntive, collegarsi direttamente alla libreria XAudio2 di DirectX SDK:

    **% DXSDK \_ dir% include \\ <arch> \\ XAudio2. lib**

    Il \_ file binario7.DLL XAUDIO2 viene installato nelle directory di sistema di Windows tramite l'installazione di DirectX SDK nel computer di sviluppo. È necessario ridistribuire queste librerie con l'applicazione usando l'installazione del programma di installazione di DirectX da DirectX SDK.

9.  Se è stato usato DirectX SDK con le versioni precedenti di Visual Studio, l'aggiornamento di Visual Studio 2010 potrebbe aver eseguito la migrazione del percorso di DirectX SDK nelle impostazioni del progetto predefinite. È consigliabile rimuovere queste impostazioni per evitare errori di compilazione futuri. Nella directory **% USERPROFILE% \\ AppData \\ Local \\ Microsoft \\ MSBuild \\ v 4.0** modificare i file **Microsoft. cpp. Win32. User** e **Microsoft. cpp. x64. User** per rimuovere tutti i riferimenti ai \_ percorsi dir DXSDK. In alternativa, è possibile rimuovere l'intero <PropertyGroup> nodo che contiene le voci di percorso, ad esempio <ExecutablePath> e, <IncludePath> per ripristinare le impostazioni predefinite standard. Se non vengono visualizzati i riferimenti alla \_ directory DXSDK in questi file, non sono necessarie modifiche.

10. Se l'app risultante supporta Windows Vista con Service Pack 2 (SP2), oltre a Windows 7 e Windows 8 e versioni successive, impostare la definizione del preprocessore denominata **\_ Win32 \_ WinNT** su 0x600. Se supporta solo Windows 7 e Windows 8 e versioni successive, impostarlo su 0x601.

    Ad esempio:

    1.  Aprire **Proprietà** per il progetto e selezionare   >  **preprocessore** C/C++.
    2.  Selezionare **tutte le configurazioni** e **tutte le piattaforme**.
    3.  Passare alla sezione **definizioni preprocessore** e impostare \_ Win32 \_ WinNT = 0x600.
    4.  Fare clic su **Applica**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Giochi per Windows e DirectX SDK**
</dt> <dt>

[Dove si trova DirectX SDK (2021 Edition)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[SDK DirectX di una determinata età](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Vivere senza D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
