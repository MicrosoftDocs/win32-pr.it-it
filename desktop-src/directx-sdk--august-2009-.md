---
description: A partire Windows 8, DirectX SDK è incluso come parte di Windows SDK.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Dov'è DirectX SDK?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46559e839abea9d6e0c89ab7e5940e46b2d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886454"
---
# <a name="where-is-the-directx-sdk"></a>Dov'è DirectX SDK?

A partire Windows 8, DirectX SDK è incluso come parte di Windows SDK.

In origine, DirectX SDK è stato creato come piattaforma ad alte prestazioni per lo sviluppo di giochi Windows. Con la maturazione delle tecnologie DirectX, sono diventate rilevanti per una gamma più ampia di applicazioni. Attualmente, la disponibilità dell'hardware Direct3D nei computer fa in modo che anche le applicazioni desktop tradizionali usino l'accelerazione hardware grafica. In parallelo, le tecnologie DirectX sono più integrate con Windows. DirectX è ora una parte fondamentale del Windows.

Dato che Windows SDK è il principale SDK per sviluppatori per Windows, DirectX è ora incluso nel kit. Puoi usare Windows SDK per creare giochi eccezionali per Windows. Per scaricare l'SDK Windows 8.x o Windows 10 SDK, vedere Windows [SDK e archivio dell'emulatore.](https://developer.microsoft.com/windows/downloads/sdk-archive)

Le tecnologie e gli strumenti seguenti, in precedenza parte di DirectX SDK, fanno ora parte di Windows SDK.


| Tecnologia o strumento | Descrizione | 
|--------------------|-------------|
| <span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows Componenti grafici<br /> | Le intestazioni e le librerie <a href="/windows/desktop/direct3d">per Direct3D</a> e altre API Windows grafica, ad esempio <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D,</a>sono disponibili in Windows SDK. <br /><blockquote>[!Note]<br />Le librerie di utilità D3DX9/D3DX10/D3DX11 deprecate sono disponibili tramite <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, ma esistono anche diverse open source <a href="https://walbourn.github.io/living-without-d3dx/">alternative.</a> La libreria dell'utilità D3DCSX DirectCompute e la DLL ridistribuibile sono disponibili in Windows SDK. D3DX12 è disponibile in <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.</blockquote><br /> | 
| <span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilatore HLSL (FXC.EXE)<br /> | Il <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">compilatore HLSL</a> è uno strumento nella sottodirectory architecture appropriata nella cartella bin in Windows SDK.<br /><blockquote>[!Note]<br />L'API D3DCompiler e la DLL ridistribuibile sono disponibili in Windows SDK.</blockquote><br /><br />Per lo sviluppo DirectX 12, usare DXCompiler in Windows SDK e ospitato in [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).<br /> | 
| <span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX per Windows<br /> | Una sostituzione dello strumento PIX per Windows è ora una funzionalità di Microsoft Visual Studio, denominata debugger Visual Studio grafica. Questa funzionalità ha migliorato notevolmente l'usabilità, il supporto per Windows 8 e Direct3D 11.1 e l'integrazione con le funzionalità Microsoft Visual Studio tradizionali, ad esempio stack di chiamate e finestre di debug per il debug <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL.</a> Per altre informazioni su questa nuova funzionalità, vedere <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">Debug della grafica DirectX.</a><br /><br />Per lo sviluppo DirectX 12, vedere l'ultima generazione di <a href="https://devblogs.microsoft.com/pix/">PIX in Windows</a><br /> | 
| <span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> per Windows<br /> | <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">L'API XAudio2</a> è ora un componente di sistema in Windows 8.x e Windows 10. Le intestazioni e le librerie per XAudio2 sono disponibili in Windows SDK. Per Windows 7, vedere <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist.</a><br /> | 
| <span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> per Windows<br /> | <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">L'API XInput</a> 1.4 è ora un componente di sistema in Windows 8.x e Windows 10. Le intestazioni e le librerie per XInput sono disponibili in Windows SDK.<br /><blockquote>[!Note]<br />XInput 9.1.0 legacy è disponibile anche come parte di Windows 7 o versione successiva.</blockquote><br /> | 
| <span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br /> | La versione più recente di XNAMATH, aggiornata per i nuovi set di istruzioni e ARM/ARM64, è ora <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath.</a> Le intestazioni per DirectXMath sono disponibili in Windows SDK e <a href="https://github.com/Microsoft/DirectXMath">in GitHub</a>.<br /> | 
| <span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>DirectX Pannello di controllo e DirectX Capabilities Viewer<br /> | Le utilità DirectX Pannello di controllo e DirectX Capabilities Viewer sono incluse nella sottodirectory architecture appropriata nella cartella bin in Windows SDK. DirectX Capabilities Viewer è disponibile anche in <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br /> | 
| <span id="XACT"></span><span id="xact"></span>XACT<br /> | Lo strumento XACT (Xbox Audio Cross Platform Tool) non è più supportato per l'uso Windows.<br /> | 
| <span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Games Explorer</a> e GDFMAKER<br /> | <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">L Games Explorer API</a> presenta giochi agli utenti di Windows. L Games Explorer API è supportata solo in Windows Vista e Windows 7. Usare lo strumento Games Definition File Maker (GDFMAKER.EXE) per dichiarare le classificazioni dei giochi per Windows Store. <br /> Lo strumento Game Definition File Maker (GDFMaker.exe) è incluso nella sottodirectory x86 nella cartella bin in Windows SDK e supporta sia le app Windows Store che le applicazioni desktop Win32.<br /><br /> | 
| <span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Esempi<br /> | È possibile trovare applicazioni di esempio che evidenziano le tecnologie DirectX 12 Windows nel repo <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">degli esempi di DirectX.</a> La maggior parte degli esempi per le versioni precedenti di Direct3D è disponibile anche online. Per altre informazioni su questi esempi, vedere <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">Catalogo degli esempi di DirectX SDK.</a><br /> | 
| <span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1.1 gestito<br /> | Gli assembly DirectX .NET sono deprecati e non sono consigliati per l'uso da parte delle nuove applicazioni. Sono disponibili diverse alternative. Vedere <a href="https://walbourn.github.io/directx-and-net/">DirectX e .NET.</a> <br /> | 




 

DirectX SDK legacy è disponibile per il download [dall'Area download Microsoft,](https://go.microsoft.com/fwlink/?LinkId=226640) se necessario, ma l'uso per i nuovi progetti non è consigliato.

> [!Note]  
> L'installazione di DirectX SDK non riesce se è già installata una determinata versione di Visual C++ 2010 Redistributable Package. Per altre informazioni su e una soluzione per risolvere questo problema, vedere [l'errore "S1023" quando si installa DirectX SDK (giugno 2010).](https://support.microsoft.com/kb/2728613)

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Uso di progetti DirectX SDK con Visual Studio

Gli esempi di DirectX SDK di giugno 2010 sono supportati con SKU premium Visual Studio (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 o Microsoft Visual Studio Ultimate 2013) in Windows 7 e Windows 8 e versioni successive. A causa della transizione delle intestazioni e delle librerie DirectX in Windows SDK, sono necessarie modifiche alle impostazioni del progetto per compilare correttamente questi esempi con il modo in cui Windows 8 SDK e versioni successive vengono inclusi nel pacchetto con gli SKU di Visual Studio Premium.

Questi passaggi si applicano anche ai progetti che dipendono da DirectX SDK.

1.  Assicurarsi che nel computer di sviluppo sia installata la versione di giugno 2010 di DirectX SDK. Se si installa in un computer che esegue Windows 8 e versioni successive, verrà richiesto e richiesto di abilitare .NET 3.5 come installazione prerequisita per DirectX SDK.

    > [!Note]  
    > L'installazione di DirectX SDK non riesce se è già installata una determinata versione di Visual C++ 2010 Redistributable Package. Per altre informazioni su e una soluzione per risolvere questo problema, vedere [l'errore "S1023" quando si installa DirectX SDK (giugno 2010).](https://support.microsoft.com/kb/2728613)

     

2.  Assicurarsi di usare uno degli SKU Visual Studio Premium. Microsoft Visual Studio Express 2012 per Windows 8 o Microsoft Visual Studio Express 2013 per Windows non compila applicazioni desktop Windows 8 e versioni successive, ad esempio gli esempi di DirectX SDK. Per installare uno degli SKU Visual Studio premium, passare a: Visual Studio [download](https://www.microsoft.com/visualstudio/11/downloads) e seguire le istruzioni.

3.  Usare il browser di esempio di DirectX SDK per installare i file di progetto per l'esempio desiderato. Aprire il file della soluzione Microsoft Visual Studio 2010 dell'esempio (con suffisso **\_ 2010).**

4.  Se si apre l'esempio in un sistema in cui è installato solo Microsoft Visual Studio 2012 o Microsoft Visual Studio 2013, viene visualizzato il messaggio seguente: "Questa soluzione contiene uno o più progetti che usano una versione precedente del compilatore e delle librerie di VC++. Ogni progetto può essere aggiornato per usare il compilatore VC++ e le librerie (v110)." Scegliere **l'opzione** Aggiorna da questa finestra di dialogo per eseguire l'aggiornamento prima di aprire il progetto.

    In caso contrario, è possibile eseguire l'aggiornamento al compilatore e alle librerie di Visual Studio 2012 o Visual Studio 2013 C++ 11 dopo il caricamento facendo clic con il pulsante destro del mouse sulla soluzione e scegliendo **Aggiorna VC++ progetti**.

5.  D3DX non è considerato l'API canonica per l'uso di Direct3D in Windows 8 e versioni successive e pertanto non è incluso nell'SDK Windows corrispondente. Esaminare le soluzioni alternative per l'uso dell'API Direct3D. Per i progetti legacy, ad esempio gli esempi di DirectX SDK Windows 7 (e versioni precedenti), per compilare applicazioni con D3DX con DirectX SDK sono necessari i passaggi seguenti:

    1.  Modificare le directory del **progetto** VC++ come indicato di seguito per usare l'ordine corretto per le intestazioni e le librerie dell'SDK.

        <dl> i. Aprire **Proprietà** per il progetto e selezionare la **VC++ Directory.**  
        ii. Selezionare **Tutte le configurazioni e Tutte le piattaforme.**  
        iii. Impostare queste directory come indicato di seguito:

        -   Directory eseguibili: **<inherit from parent or project defaults>** (nell'elenco a discesa a destra)
        -   Directory di inclusione: **$(IncludePath);$(DIR DXSDK)Include \_**
        -   Directory delle librerie di **inclusione: $(LibraryPath);$(DXSDK \_ DIR)Lib \\ x86**

          
        iv. Fare clic su **Applica**.  
        v. Scegliere la **piattaforma x64**.  
        vi. Impostare la **directory della libreria come** indicato di seguito:

        -   Directory della libreria: **$(LibraryPath);$(DXSDK \_ DIR)Lib \\ x64**

          
        </dl>

    2.  Quando "d3dx9.h", "d3dx10.h" o "d3dx11.h" sono inclusi nel progetto, assicurarsi di includere prima "d3d9.h", "d3d10.h" e "dxgi.h" o "d3d11.h" e "dxgi.h" in modo esplicito per assicurarsi di selezionare la versione più recente. Se necessario, è possibile disabilitare l'avviso **C4005.** Tuttavia, questo avviso indica che si sta usando la versione precedente di queste intestazioni.
    3.  Rimuovere tutti i riferimenti a DXGIType.h nel progetto. Questa intestazione non esiste in Windows SDK e la versione di DirectX SDK è in conflitto con il nuovo winerror.h.
    4.  Tutte le DLL D3DX vengono installate nel computer di sviluppo dall'installazione di DirectX SDK. Assicurarsi che le dipendenze D3DX necessarie siano ridistribuite con qualsiasi esempio o con l'applicazione se viene spostata in un altro computer.
    5.  Tenere presente che le tecnologie di sostituzione per gli usi correnti di D3DX11 includono [DirectXTex,](https://github.com/Microsoft/DirectXTex) [DirectXTK,](https://github.com/Microsoft/DirectXTK) [DirectXMesh](https://github.com/Microsoft/DirectXMesh)e [UVAtlas.](https://github.com/Microsoft/UVAtlas) D3DXMath viene sostituito [da DirectXMath](./dxmath/directxmath-portal.md).

6.  Assicurarsi di usare la nuova versione del compilatore shader HLSL osservando le condizioni seguenti:

    1.  Se si modifica la directory eseguibile in base al passaggio 5, le compilazioni del progetto useranno FXC dall'Windows SDK. Tenere presente che i file HLSL sono ora riconosciuti ufficialmente da Visual Studio. È possibile aggiungerli come file di progetto e impostare le opzioni del compilatore tramite il sistema del progetto.

    2.  Se si richiama la compilazione in fase di esecuzione tramite la DLL D3DX legacy, verrà utilizzata la versione precedente non corretta del compilatore HLSL. Sostituire tutti i riferimenti alle API D3DXCompile \* , D3DX10Compile e D3DX11Compile nel codice con la funzione \* \* D3DCompile in D3DCOMPILER \_46.DLL o D3DCOMPILER \_47.DLL.

    3.  Qualsiasi progetto che usa la compilazione dello shader in fase di esecuzione devexx.DLL D3DCOMPILER nel \_ percorso eseguibile locale per il progetto. Questa DLL è disponibile in questa sottodirectory dell'installazione di Windows SDK in **%ProgramFiles(x86)% \\ Windows Kits \\ 8.0 \\ Redist \\ D3D \\ &lt; arch &gt;** o **%ProgramFiles(x86)% \\ Windows Kits \\ 8.1 \\ Redist \\ D3D \\ &lt; arch &gt;** dove **&lt; arch &gt;** è **x86** e **x64**.

        Il \_46.DLL D3DCOMPILER o D3DCOMPILER47.DLL da Windows SDK non è un componente di sistema e non deve essere copiato nella directory Windows \_ di sistema. È possibile ridistribuire questa DLL in altri computer con l'applicazione come DLL side-by-side.

7.  Qualsiasi progetto che usa l'API XInput ed è progettato per l'esecuzione in Windows 7 o versioni precedenti di Windows deve usare la versione legacy (9.1.0) o dovrà includere in modo esplicito le intestazioni e le librerie per questo componente da DirectX SDK. Intestazione XInput e XINPUT. LIB inclusi nell'SDK Windows destinazione solo la versione (1.4) disponibile come parte di Windows 8 e versioni successive. La stessa intestazione può essere usata con XINPUT9 \_ 1 0.LIB per usare la versione legacy, inclusa nelle versioni precedenti di \_ Windows. La versione legacy di XInput non rileva le funzionalità complete o supporta l'audio integrato nel controller, quindi se è necessario il supporto per queste funzionalità, è necessario usare DirectX SDK versione (1.3).

    Per usare l'API XInput di livello inferiore completa, è necessario usare direttamente le intestazioni `#include` XInput specifiche di DirectX SDK:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... e nelle opzioni del linker per Dipendenze aggiuntive collegarsi direttamente alla libreria XInput di DirectX SDK:

    **%DXSDK \_ DIR%Include \\ &lt; arch &gt; \\ xinput.lib**

    Il file binario3.DLL XINPUT1 viene installato nelle Windows di sistema dall'installazione di \_ DirectX SDK nel computer di sviluppo. Sarà necessario ridistribuire questo file binario con l'applicazione usando l'installazione di DirectX Setup da DirectX SDK.

8.  Qualsiasi progetto che usa l'API XAudio2 ed è progettato per l'esecuzione in Windows 7 o versioni precedenti di Windows deve usare la versione precedente (9.1.0) o includere in modo esplicito le intestazioni e le librerie per questo componente da DirectX SDK. Le intestazioni e le librerie XAudio2 incluse in Windows SDK hanno come destinazione solo la versione (2.8) inclusa nell'Windows 8.

    Ad esempio, con XAudio2, è necessario che le intestazioni `#include` XAudio2 specifiche di DirectX SDK:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... e nelle opzioni del linker per Dipendenze aggiuntive, collegarsi direttamente alla libreria XAudio2 di DirectX SDK:

    **%DXSDK \_ DIR%Include \\ &lt; arch &gt; \\ xaudio2.lib**

    Il file binario7.DLL XAUDIO2 viene installato nelle Windows di sistema dall'installazione di \_ DirectX SDK nel computer di sviluppo. È necessario ridistribuire queste librerie con l'applicazione usando l'installazione di DirectX Setup da DirectX SDK.

9.  Se è stato usato DirectX SDK con le versioni precedenti di Visual Studio, l'aggiornamento di Visual Studio 2010 potrebbe aver eseguito la migrazione del percorso di DirectX SDK nelle impostazioni di progetto predefinite. È consigliabile rimuovere queste impostazioni per evitare errori di compilazione futuri. Nella directory **%USERPROFILE% AppData Local \\ Microsoft MSBuild \\ \\ \\ \\ v4.0** modificare i file **Microsoft.Cpp.Win32.user** e **Microsoft.Cpp.x64.user** per rimuovere tutti i riferimenti ai percorsi DIR DXSDK. \_ In alternativa, è possibile rimuovere l'intero nodo PropertyGroup che contiene le voci Path, ad esempio ExecutablePath e &lt; &gt; &lt; &gt; &lt; IncludePath, per ripristinare &gt; le impostazioni predefinite standard. Se non vengono visualizzati riferimenti a DXSDK DIR in questi \_ file, non sono necessarie modifiche.

10. Se l'app risultante supporta Windows Vista con Service Pack 2 (SP2), Windows 7 e Windows 8 e versioni successive, impostare la definizione del preprocessore denominata **\_ WIN32 \_ WINNT** su 0x600. Se supporta solo Windows 7 e Windows 8 versioni successive, impostarlo su 0x601.

    Ad esempio:

    1.  Aprire **Proprietà** per il progetto e selezionare **Preprocessore C/C++.**  >  
    2.  Selezionare **Tutte le configurazioni** e **Tutte le piattaforme**.
    3.  Passare alla sezione **Definizioni preprocessore** e impostare \_ WIN32 \_ WINNT=0x600.
    4.  Fare clic su **Applica**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Giochi per Windows e DirectX SDK**
</dt> <dt>

[Dove si trova DirectX SDK (edizione 2021)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[SDK DirectX di una determinata età](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Vita senza D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
