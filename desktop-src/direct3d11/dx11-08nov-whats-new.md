---
title: Novità della versione 2008 di Direct3D 11 Tech Preview
description: Questa versione di Direct3D 11 contiene nuove funzionalità, strumenti e documentazione.
ms.assetid: 7d259764-b826-4609-b415-2093cc6df874
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a49529882eafaf092a866d1b172de62fe15c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399076"
---
# <a name="whats-new-in-the-nov-2008-direct3d-11-tech-preview"></a>Novità della versione 2008 di Direct3D 11 Tech Preview

Questa versione di Direct3D 11 contiene nuove funzionalità, strumenti e documentazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>Tassellatura<br/></td>
<td>Direct3D 11 fornisce fasi della pipeline aggiuntive per supportare il <a href="direct3d-11-advanced-stages-tessellation.md">mosaico in tempo reale</a> di primitivi di ordine elevato. Grazie a numerose funzionalità programmabili, questa funzionalità consente molti metodi diversi per la valutazione di superfici di ordine elevato, incluse le aree di sottodivisione usando le tecniche di approssimazione, le patch di Bezier, lo schema a mosaico adattivo e il mapping di spostamento. Questa funzionalità sarà disponibile solo in componenti hardware Direct3D a 11 classi, quindi per valutare questa funzionalità sarà necessario usare l'rasterizzazione dei riferimenti. Per una dimostrazione dello schema a mosaico in azione, vedere l'esempio <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> disponibile tramite il browser di esempio.<br/></td>
</tr>
<tr class="even">
<td><span id="Compute_Shader"></span><span id="compute_shader"></span><span id="COMPUTE_SHADER"></span>Compute Shader<br/></td>
<td><a href="direct3d-11-advanced-stages-compute-shader.md">Compute shader</a> è una fase aggiuntiva indipendente dalla pipeline Direct3D 11 che consente l'elaborazione di utilizzo generico nella GPU. Oltre a tutte le funzionalità dello shader fornite da Unified shader core, compute shader supporta anche le letture e le Scritture sparse nelle risorse tramite viste di accesso non ordinate, un pool di memoria condiviso all'interno di un gruppo di thread in esecuzione, primitive di sincronizzazione, operatori atomici e molte altre funzionalità avanzate di Parallel Data. In questa versione è stata abilitata una variante di Compute Shader Direct3D 11 che può funzionare su hardware Direct3D a 10 classi. È pertanto possibile sviluppare compute shader su hardware effettivo, ma è necessario un driver aggiornato. La funzionalità completa di compute shader di Direct3D 11 è progettata per supportare l'hardware di livello Direct3D 11, quindi, per valutare la funzionalità completa, è necessario usare l'rasterizzazione dei riferimenti finché tale hardware non sarà disponibile. Per una demo di compute shader in azione, vedere l'esempio <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> disponibile tramite il browser di esempio.<br/></td>
</tr>
<tr class="odd">
<td><span id="Multithreaded_Rendering"></span><span id="multithreaded_rendering"></span><span id="MULTITHREADED_RENDERING"></span>Rendering multithreading<br/></td>
<td>La differenza principale dell'API da Direct3D 10 in Direct3D 11 è l'aggiunta di <a href="overviews-direct3d-11-render-multi-thread.md">contesti posticipati</a>, che consente l'esecuzione scalabile di comandi Direct3D distribuiti su più core. Un contesto posticipato acquisisce e assembla azioni come le modifiche di stato e gli invii di disegni che possono essere eseguiti sul dispositivo effettivo in un secondo momento. Utilizzando i contesti posticipati su più thread, un'applicazione può distribuire l'overhead della CPU necessario nel runtime Direct3D11 e il driver a più core, consentendo un utilizzo migliore della configurazione del computer dell'utente finale. Questa funzionalità è disponibile per l'uso nell'hardware Direct3D 10 corrente e nell'rasterizzazione dei riferimenti. Per una dimostrazione dell'utilizzo dell'API, vedere l'esempio <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> disponibile tramite il browser di esempio.<br/></td>
</tr>
<tr class="even">
<td><span id="Dynamic_Shader_Linkage_"></span><span id="dynamic_shader_linkage_"></span><span id="DYNAMIC_SHADER_LINKAGE_"></span>Collegamento dinamico dello shader <br/></td>
<td>Per risolvere il problema di esplosione combinatoria riscontrato nella specializzazione degli shader per le prestazioni, Direct3D 11 introduce una forma limitata di <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">collegamento dello shader</a> di runtime che consente la specializzazione dello shader quasi ottimale durante l'esecuzione di un'applicazione. Questa operazione viene eseguita specificando le implementazioni di funzioni specifiche nel codice dello shader quando lo shader viene assegnato alla pipeline, consentendo al driver di inline le istruzioni di shader native rapidamente anziché forzare il driver a ricompilare il linguaggio intermedio in istruzioni native con la nuova configurazione. Lo sviluppo dello shader viene esposto tramite l'introduzione di classi e interfacce a HLSL. Per una dimostrazione, vedere l'esempio <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">Dynamic shader linkage 11</a> disponibile tramite il browser di esempio.<br/></td>
</tr>
<tr class="odd">
<td><span id="Windows_Advanced_Rasterizer__WARP_"></span><span id="windows_advanced_rasterizer__warp_"></span><span id="WINDOWS_ADVANCED_RASTERIZER__WARP_"></span>Rasterizzazione avanzata di Windows (WARP)<br/></td>
<td>Disponibile in questo SDK tramite Direct3D 11 e infine anche tramite Direct3D 10,1, WARP è un rasterizzatore veloce e multicore che è completamente compatibile con Direct3D 10,1. L'utilizzo di questa tecnologia è semplice quanto il passaggio del flag di D3D_DRIVER_TYPE_WARP nella creazione del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><span id="Direct3D_10_and_Direct3D_11_on_Direct3D_9_Hardware__D3D10_Level_9_"></span><span id="direct3d_10_and_direct3d_11_on_direct3d_9_hardware__d3d10_level_9_"></span><span id="DIRECT3D_10_AND_DIRECT3D_11_ON_DIRECT3D_9_HARDWARE__D3D10_LEVEL_9_"></span>Direct3D 10 e Direct3D 11 su hardware Direct3D 9 (D3D10 livello 9)<br/></td>
<td>Disponibile in questo SDK tramite Direct3D 11 e infine anche tramite Direct3D 10,1, l'API Direct3D può essere destinata alla maggior parte dei componenti hardware Direct3D 9 e Direct3D 10, Direct3D 10,1 e Direct3D 11. Questa operazione viene eseguita fornendo il meccanismo a livello di funzionalità, che raggruppa l'hardware in sei categorie a seconda della funzionalità: 9_1, 9_2, 9_3, 10_0, 10_1 e 11_0. Una scheda soddisfa solo un livello di funzionalità se è completamente conforme a tale livello e ogni livello è un super set rigoroso di quelli sottostanti. La funzionalità è emulata in modo minimo per garantire che non vengano rilevate scogliere di prestazioni impreviste. Di conseguenza, le funzionalità come la geometria shader non sono disponibili per le destinazioni a livello di Direct3D 9. <br/></td>
</tr>
<tr class="odd">
<td><span id="Runtime_Binaries"></span><span id="runtime_binaries"></span><span id="RUNTIME_BINARIES"></span>File binari di runtime<br/></td>
<td>Tutti i file binari di runtime inclusi in Direct3D 11 Tech Preview che saranno disponibili in Windows 7 e Windows Vista SP1 vengono installati con l'SDK e vengono etichettati &quot; come &quot; componenti beta, ad esempio D3D11_beta.DLL. Tutti i componenti con etichetta beta hanno un bombardamento temporale. Per creare progetti per valutare questi nuovi componenti, è necessario collegarsi alle librerie di importazione con etichetta beta equivalenti (ad esempio D3D11_beta. lib). Se si dispone di una copia PDC di Windows 7, le intestazioni, le librerie e PDB fornite nel Windows SDK con la compilazione sono appropriate per lo sviluppo usando i componenti di Direct3D 11 forniti in Windows 7. Riservare l'uso delle intestazioni, delle librerie e di PDB in questo SDK ai componenti beta disponibili qui.<br/></td>
</tr>
<tr class="even">
<td><span id="D3DX11"></span><span id="d3dx11"></span>D3DX11<br/></td>
<td>D3DX11 supporta attualmente il caricamento di trama, la compilazione dello shader, il caricamento dei dati e le funzioni dei thread di lavoro per le risorse Direct3D 11. In futuro, questo componente fornirà un maggior numero di tecnologie disponibili in D3DX10. La funzionalità di compilazione dello shader viene fornita anche direttamente tramite il componente del compilatore Direct3D, descritta di seguito.<br/></td>
</tr>
<tr class="odd">
<td><span id="HLSL_and_Direct3D_Compiler"></span><span id="hlsl_and_direct3d_compiler"></span><span id="HLSL_AND_DIRECT3D_COMPILER"></span>HLSL e compilatore Direct3D<br/></td>
<td>Il compilatore HLSL presenta diverse nuove funzionalità per il supporto delle nuove tecnologie disponibili in Direct3D 11. Ciò include la programmazione orientata a oggetti attraverso interfacce e classi, una sintassi di indicizzazione diretta per i caricamenti di risorse e la parola chiave "precisa" per garantire che tutte le operazioni eseguite con una variabile specifica rispettino le regole a virgola mobile restrittive. Quasi tutte le nuove funzionalità linguistiche hanno funzionalità valide per le destinazioni shader esistenti. Oltre a supportare tutti gli shader Direct3D 9, Direct3D 10, Direct3D 10,1 e Direct3D 11, il compilatore HLSL supporta anche gli obiettivi speciali necessari per scrivere gli shader per le destinazioni Direct3D 10 di livello 9. Il compilatore D3D è ora direttamente accessibile all'esterno di D3DX10 e D3DX11 tramite D3DCompiler. H e D3DCompiler. lib. Con questi nuovi file, non è necessario che un'applicazione venga collegata a D3DX per eseguire la compilazione del runtime e non è necessario che un'applicazione includa il compilatore se è necessaria solo la funzionalità D3DX.<br/></td>
</tr>
<tr class="even">
<td><span id="D3D11_Reference_Rasterizer"></span><span id="d3d11_reference_rasterizer"></span><span id="D3D11_REFERENCE_RASTERIZER"></span>Rasterizzatore di riferimento D3D11<br/></td>
<td>L'rasterizzazione dei riferimenti fornisce un'implementazione di rasterizzazione standard Gold per la valutazione delle funzionalità di Direct3D 11 non ancora disponibili nell'hardware. L'rasterizzazione dei riferimenti è inoltre disponibile come metodo per verificare l'accuratezza di un'implementazione hardware specifica allo standard di rasterizzazione. L'rasterizzazione dei riferimenti è progettata per la correttezza, non per le prestazioni. Per creare un dispositivo di riferimento, passare semplicemente il flag di D3D_DRIVER_TYPE_REFERENCE al momento della creazione del dispositivo. <br/></td>
</tr>
<tr class="odd">
<td><span id="D3D11_SDK_Layers"></span><span id="d3d11_sdk_layers"></span><span id="D3D11_SDK_LAYERS"></span>Livelli di D3D11 SDK<br/></td>
<td>I livelli SDK di Direct3D11 forniscono un meccanismo per tenere traccia del funzionamento del runtime di Direct3D 11 durante lo sviluppo. Attualmente viene utilizzato per fornire informazioni di debug utili, che non solo includono errori di utilizzo non corretto, ma anche avvisi che consigliano l'utilizzo di procedure consigliate per il runtime e spesso forniscono informazioni dettagliate e utili per il debug. È consigliabile che l'output di debug dai livelli di D3D11 SDK venga attivato in qualsiasi momento durante lo sviluppo e che un'applicazione non generi output di debug durante l'esecuzione prima che venga rilasciata o utilizzata con PIX per Windows per la profilatura. L'abilitazione del livello di debug è semplice quanto il passaggio del flag di D3D11_CREATE_DEVICE_DEBUG al momento della creazione del dispositivo. Gli sviluppatori sono vivamente invitati a usare i livelli nelle build di debug. Non è consigliabile usare i livelli nelle build del profilo o della versione.<br/></td>
</tr>
<tr class="even">
<td><span id="New_Samples"></span><span id="new_samples"></span><span id="NEW_SAMPLES"></span>Nuovi esempi<br/></td>
<td>Questa versione include quattro nuovi esempi.<br/>
<ul>
<li>Nell'esempio <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">Dynamic shader linkage 11</a> viene illustrato l'utilizzo di interfacce Shader Model 5 shader e il supporto Direct3D 11 per il collegamento dei metodi di interfaccia dello shader in fase di esecuzione.</li>
<li>Nell'esempio <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> viene illustrato come configurare ed eseguire compute shader (CS per un breve periodo di tempo), una delle nuove funzionalità più interessanti di Direct3D 11. Sebbene nell'esempio venga utilizzato solo il CS per implementare il mapping dei toni HDR, il concetto dovrebbe estendersi facilmente ad altri algoritmi di post-elaborazione, nonché calcoli più generali.</li>
<li>Nell'esempio <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> viene illustrato come suddividere il rendering tra più thread, con un sovraccarico molto basso.</li>
<li>Il nuovo esempio <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> è molto simile all'esempio SubD10 in DirectX SDK, ad eccezione del fatto che è stato migliorato per sfruttare tre nuove fasi della pipeline Direct3D 11: Hull shader, mosaico e Domain shader.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità introdotte nelle versioni precedenti](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

 

