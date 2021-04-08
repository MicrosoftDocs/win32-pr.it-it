---
title: Domande frequenti su DirectX
description: Questo articolo contiene una raccolta di domande frequenti su Microsoft DirectX.
ms.assetid: 58d9fe45-a2c7-8280-2826-e2e14ecea983
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd5fd70f1a651121b8d977dbb9479cef6edd024
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047025"
---
# <a name="directx-frequently-asked-questions"></a>Domande frequenti su DirectX

Questo articolo contiene una raccolta di domande frequenti su Microsoft DirectX.

-   [Problemi generali di sviluppo DirectX](#general-directx-development-issues)
-   [Domande su Direct3D](#direct3d-questions)
    -   [Domande generali su Direct3D](#general-direct3d-questions)
    -   [Elaborazione Geometry (Vertex)](#geometry-vertex-processing)
    -   [Ottimizzazione delle prestazioni](#performance-tuning)
    -   [Libreria di utilità D3DX](#d3dx-utility-library)
-   [Domande DirectSound](#directsound-questions)
-   [Estensioni DirectX per Alias Maya](#directx-extensions-for-alias-maya)
-   [Domande su XInput](#xinput-questions)

## <a name="general-directx-development-issues"></a>Problemi generali di sviluppo DirectX

<dl> <dt>

<span id="Should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="SHOULD_GAME_DEVELOPERS_REALLY_CARE_ABOUT_SUPPORTING_X64_EDITIONS_"></span>**Gli sviluppatori di giochi sono veramente interessati a supportare le edizioni x64?**
</dt> <dd>

Assolutamente sì. la tecnologia x64 è ampiamente disponibile sul mercato. La maggior parte delle nuove CPU vendute negli ultimi anni e quasi tutte le linee dei processori nello sviluppo da AMD e Intel sono compatibili con x64. Windows XP Professional x64 Edition ha introdotto la tecnologia di abilitazione del sistema operativo per x64 rilasciata nel aprile del 2005. Poiché le edizioni x64 richiedono una nuova generazione di driver nativi a 64 bit, questa prima versione è stata limitata alla distribuzione OEM.

Con Windows Vista, i clienti possono scegliere le edizioni a 32 bit o a 64 bit quando acquistano computer basati su Windows e le licenze per Windows Vista sono valide per le edizioni 32 o 64 bit del sistema operativo. Inoltre, molti driver a 64 bit sono disponibili nella casella e i produttori di dispositivi sono necessari per fornire driver nativi sia a 32 bit che a 64 bit come parte del programma di certificazione Windows.

Tutti questi fattori aumenteranno significativamente le distribuzioni delle edizioni di Windows a 64 bit. Quando i nuovi computer iniziano a essere distribuiti con più di 2 GB di RAM fisica, l'incentivo a usare un sistema operativo a 32 bit diminuisce notevolmente a favore delle edizioni a 64 bit. La tecnologia a 64 bit supporta completamente il codice nativo a 32 bit, anche se sono necessarie implementazioni native a 64 bit per sfruttare appieno il nuovo spazio di memoria a 64 bit. Ogni applicazione a 32 bit deve avere una compatibilità a 64 bit come requisito di spedizione minima e soddisfare tale requisito è un requisito di base per la compatibilità con Windows Vista. In genere, le incompatibilità sono dovute all'uso di codice a 16 bit progettato per il sistema operativo Windows 3,1 o all'installazione di driver che non sono disponibili nei moduli nativi a 32 bit e 64 bit.

Per altri dettagli sulla tecnologia a 64 bit, vedere [programmazione a 64 bit per sviluppatori di giochi](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_95__Windows_98_or_Windows_ME_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_95__windows_98_or_windows_me_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_95__WINDOWS_98_OR_WINDOWS_ME_"></span>**Gli sviluppatori di giochi possono comunque pubblicare giochi per Windows 95, Windows 98 o Windows ME?**
</dt> <dd>

Non più per due motivi: prestazioni e set di funzionalità.

Se la velocità minima della CPU necessaria per il gioco è 1.2 GHz o superiore (che è più comune per i titoli a prestazioni elevate), la maggior parte dei computer idonei eseguirà Windows XP. Dal momento in cui sono stati venduti i computer con velocità della CPU superiore a 1,2 GHz, Windows XP è stato installato come sistema operativo predefinito da quasi tutti i produttori. Ciò significa che in Windows XP sono disponibili molte funzionalità che oggi gli sviluppatori di giochi dovrebbero trarre vantaggio da:

-   Multitasking migliorato, che consente di ottenere un'esperienza migliore e più semplice per video, audio e giochi.
-   Modello di driver video più stabile, che consente un debug più semplice, un gioco più uniforme e prestazioni migliori.
-   Configurazione più semplice per la rete, che consente un accesso più semplice ai giochi multiplayer.
-   Supporto per i trasferimenti DMA per impostazione predefinita da unità disco rigido, il che comporta un caricamento più veloce e più rapido delle applicazioni.
-   Segnalazione errori Windows, che comporta un sistema operativo, driver e applicazioni più stabili.
-   Supporto Unicode, che semplifica notevolmente i problemi di localizzazione.
-   Migliore sicurezza e stabilità, che consente di migliorare l'esperienza utente.
-   Supporto migliore per hardware moderno: la maggior parte dei quali non usa più i driver di Windows 98.
-   Gestione della memoria migliorata, con conseguente miglioramento della stabilità e della sicurezza.
-   File system NTFS migliorato, che è più resistente agli errori e offre prestazioni migliori con le funzionalità di sicurezza.

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_2000_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_2000_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_2000_"></span>**Gli sviluppatori di giochi devono ancora pubblicare giochi per Windows 2000?**
</dt> <dd>

Non più. Oltre ai motivi elencati in, **gli sviluppatori di giochi dovrebbero ancora pubblicare giochi per windows 95, windows 98 o Windows me?**, Windows 2000 non dispone di queste funzionalità:

-   Windows XP supporta funzionalità avanzate del processore, ad esempio Hyper-Threading, multicore e x64.
-   Windows XP supporta componenti affiancati che riducono in modo significativo i conflitti di controllo delle versioni dell'applicazione.
-   Windows XP supporta la protezione della memoria senza esecuzione, che consente di impedire i programmi dannosi e può facilitare il debug.
-   Windows XP ha migliorato il supporto per schede video basate su AGP e PCI Express avanzati.
-   Windows XP supporta il cambio rapido utente, desktop remoto e assistenza remota, che può contribuire a ridurre i costi di supporto del prodotto.
-   Gli strumenti per le prestazioni come PIX (in DirectX Developer SDK) non supportano più Windows 2000.

In breve, Windows 2000 non è mai stato progettato o commercializzato come sistema operativo consumer.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_Vista__How_do_they_impact_my_DirectX_application_"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_vista__how_do_they_impact_my_directx_application_"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_VISTA__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION_"></span>**Quali sono le differenze tra le diverse edizioni di Windows Vista? Come influiscano sull'applicazione DirectX?**
</dt> <dd>

La famiglia di Windows Vista include cinque edizioni:

-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Business
-   Windows Vista Enterprise
-   Windows Vista Ultimate

Home Basic e Home Premium sono versioni incentrate sugli utenti, con funzionalità come la sicurezza delle famiglie (precedentemente note come controlli padre) e Home Premium include Media Center. Business ed Enterprise sono edizioni incentrate sull'azienda, con funzionalità quali l'aggiunta a un dominio e Servizi terminal e Desktop remoto. L'edizione Ultimate combina tutte le funzionalità del consumer e delle edizioni aziendali in un'unica versione. Tutte le edizioni sono disponibili in entrambe le edizioni a 32 bit (x86) e a 64 bit (x64) e gli utenti possono usare lo stesso identificatore di prodotto per entrambe le piattaforme.

La tecnologia sottostante le varie edizioni è identica e tutti hanno la stessa versione di DirectX Runtime e altri componenti. Tuttavia, le edizioni presentano alcune piccole differenze rispetto ai giochi:

-   Esplora giochi è disponibile in tutte le edizioni, ma il collegamento dei giochi nel menu Start è solo in Home Basic, Home Premium e Ultimate. Esplora giochi è ancora disponibile in tutte le edizioni (facendo clic sul pulsante Start, scegliendo tutti i programmi e quindi facendo clic su giochi) e l'interfaccia IGameExplorer funzioni su tutte le edizioni.
-   I giochi inclusi in Windows non sono disponibili per impostazione predefinita nell'azienda e nell'azienda, ma possono essere abilitati dall'amministratore.
-   La sicurezza della famiglia e le classificazioni dei giochi non vengono visualizzate o influiscono sul comportamento di business o Enterprise e sono disabilitate in Ultimate quando viene aggiunto un dominio.

Le impostazioni di controllo dell'account utente hanno le stesse impostazioni predefinite in tutte le edizioni, ma possono essere sostituite dalle impostazioni Criteri di gruppo per il dominio in business, Enterprise e Ultimate. Ad esempio, il criterio impostazione controllo account utente: comportamento della richiesta di elevazione dei privilegi per gli utenti standard può essere impostato in modo da rifiutare automaticamente le richieste di elevazione in molte impostazioni aziendali per migliorare la sicurezza e molti utenti in tali ambienti verranno sempre eseguiti come utenti standard senza la possibilità di scegliere di eseguire come amministratore. Qualsiasi programma (ad esempio un programma di installazione) che richiede diritti amministrativi, a causa del rilevamento dell'installazione legacy o della presenza di un manifesto che specifica il livello di esecuzione richiesto come "requireAdministrator", non verrà sempre avviato in tali situazioni. Altre impostazioni di criteri, ad esempio controllo dell'account utente: solo gli eseguibili con privilegi elevati firmati e convalidati, possono anche impedire il funzionamento del programma di installazione se non si firma il file eseguibile tramite Authenticode.

Questi tipi di modifiche ai criteri possono essere applicati a qualsiasi edizione di Windows Vista, ma sono più probabili nei computer aggiunti a un dominio.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_7__How_do_they_impact_my_DirectX_application__"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_7__how_do_they_impact_my_directx_application__"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_7__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION__"></span>**Quali sono le differenze tra le diverse edizioni di Windows 7? Come influiscano sull'applicazione DirectX?** 
</dt> <dd>

La maggior parte degli utenti di Windows 7 avrà probabilmente una delle due edizioni: Windows 7 Home Premium, per gli utenti privati o Windows 7 Professional, per gli utenti e gli sviluppatori aziendali. Per le aziende di grandi dimensioni, Windows 7 Enterprise Edition è dotato di contratti multilicenza, che include tutte le funzionalità di Windows 7. Windows 7 Ultimate è l'equivalente finale di tale edizione.

Windows 7 Starter Edition è disponibile in tutto il mondo per gli OEM ed è previsto che sia distribuito principalmente con netbook e computer notebook a bassa potenza. Windows 7 Home Basic è disponibile solo nei mercati emergenti.

Si noti che tutte le edizioni di Windows 7 (eccetto Starter Edition) sono disponibili per le versioni a 32 bit (x86) e a 64 bit (x64) e tutti i pacchetti finali di Windows 7 includono supporti per entrambe le versioni. Analogamente a Windows Vista, gli utenti possono utilizzare lo stesso identificatore di prodotto al dettaglio in entrambe le piattaforme.

La tecnologia sottostante nelle varie edizioni è identica e tutte le edizioni hanno la stessa versione di DirectX Runtime e di altri componenti. Presentano alcune differenze rispetto alle funzionalità di gioco:

-   Esplora giochi è disponibile in tutte le edizioni, ma il collegamento dei giochi nel menu Start è nascosto per impostazione predefinita in Windows 7 Professional ed Enterprise. Esplora giochi è ancora disponibile nel menu Start (facendo clic su tutti i programmi e quindi facendo doppio clic su giochi) e il collegamento giochi diretti può essere abilitato dall'utente.
-   I giochi inclusi in Windows non sono disponibili per impostazione predefinita in Windows 7 Professional ed Enterprise, ma possono essere abilitati dall'amministratore.
-   Le classificazioni dei giochi e la sicurezza per la famiglia sono disponibili in tutte le edizioni, ma sono disabilitate in Windows 7 Professional, Enterprise e Ultimate quando il sistema operativo viene aggiunto a un dominio. Come in Windows Vista Ultimate, questa funzionalità può essere riabilitata nel computer che è stato aggiunto a un dominio.

Le impostazioni di controllo dell'account utente possono essere influenzate dalle impostazioni Criteri di gruppo nelle edizioni Professional, Enterprise e Ultimate di Windows 7, come Windows Vista. Per ulteriori informazioni, vedere **quali sono le differenze tra le diverse edizioni di Windows Vista? Come influiscano sull'applicazione DirectX?**

</dd> <dt>

<span id="Will_DirectX_10_be_available_for_Windows_XP__"></span><span id="will_directx_10_be_available_for_windows_xp__"></span><span id="WILL_DIRECTX_10_BE_AVAILABLE_FOR_WINDOWS_XP__"></span>**DirectX 10 sarà disponibile per Windows XP?** 
</dt> <dd>

No. Windows Vista, con DirectX 10, include un runtime DirectX aggiornato basato sul runtime di Windows XP SP2 (DirectX 9.0 c) con modifiche per l'utilizzo con il nuovo Windows Display Driver Model (WDDM) e il nuovo stack di driver audio e con altri aggiornamenti nel sistema operativo. Oltre a Direct3D 9, Windows Vista supporta due nuove interfacce quando sono presenti i driver e l'hardware video corretti: Direct3D9Ex e Direct3D10.

Poiché queste nuove interfacce si basano sulla tecnologia WDDM, non saranno mai disponibili nelle versioni precedenti di Windows. Tutte le altre modifiche apportate alle tecnologie DirectX per Windows Vista sono specifiche anche per la nuova versione di Windows. Il nome DirectX 10 è fuorviante in quanto molte tecnologie di spedizione in DirectX SDK (XACT, XINPUT, D3DX) non sono incluse in questo numero di versione. Quindi, fare riferimento al numero di versione di DirectX Runtime nel suo complesso ha perso gran parte del suo significato, anche per 9.0 c. Lo strumento di diagnostica DirectX (DXdiag.exe) in Windows Vista segnala DirectX 10, ma si riferisce in realtà solo a Direct3D 10.

</dd> <dt>

<span id="Will_DirectX_11_be_available_for_Windows_Vista_or_Windows_XP__"></span><span id="will_directx_11_be_available_for_windows_vista_or_windows_xp__"></span><span id="WILL_DIRECTX_11_BE_AVAILABLE_FOR_WINDOWS_VISTA_OR_WINDOWS_XP__"></span>**DirectX 11 sarà disponibile per Windows Vista o Windows XP?** 
</dt> <dd>

DirectX 11 è integrato in Windows 7 ed è disponibile come aggiornamento per Windows Vista (vedere <https://go.microsoft.com/fwlink/p/?linkid=160189> ). Sono incluse le API Direct3D 11, DirectX Graphics Infrastructure (DXGI) 1,1, i livelli di funzionalità 10Level9, Windows Advanced Rasterizzation Platform (WARP) 10 software rendering device, Direct2D, DirectWrite e un aggiornamento dell'API Direct3D 10,1 per supportare 10Level9 e WARP 10.

Per gli stessi motivi indicati nella domanda precedente (**DirectX 10 sarà disponibile per Windows XP?** , Direct3D 11 e le API correlate non sono disponibili in Windows XP.

</dd> <dt>

<span id="What_Happened_to_DirectShow__I_can_t_find_it_in_the_DirectX_SDK._"></span><span id="what_happened_to_directshow__i_can_t_find_it_in_the_directx_sdk._"></span><span id="WHAT_HAPPENED_TO_DIRECTSHOW__I_CAN_T_FIND_IT_IN_THE_DIRECTX_SDK._"></span>**Cosa è successo a DirectShow? Non riesco a trovarlo in DirectX SDK.** 
</dt> <dd>

DirectShow è stato rimosso da DirectX SDK a partire dal 2005 aprile. È possibile ottenere intestazioni, librerie, strumenti ed esempi per DirectShow in Windows Software Development Kit (noto in precedenza come Platform SDK). DirectSetup in DirectX SDK continua a supportare la ridistribuzione dei componenti di sistema di DirectShow e i componenti più recenti sono già installati nei sistemi operativi seguenti: Microsoft Windows XP Service Pack 2, Windows XP Professional x64 Edition, Windows Server 2003 Service Pack 1 e Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_Vista__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_vista__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_VISTA__"></span>**Quali modifiche sono state apportate a DirectX Runtime per Windows Vista?** 
</dt> <dd>

Sono state apportate le modifiche principali per supportare il nuovo WDDM. Per informazioni dettagliate sul nuovo modello di driver, sull'effetto di Direct3D 9 e sulle due nuove interfacce grafiche, Direct3D 9Ex e Direct3D 10, vedere [API grafiche in Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista). Le nuove API di grafica per Windows 7, Direct3D 11, Direct2D, DirectWrite, DXGI 1,1 e un aggiornamento di Direct3D 10.1, sono disponibili come aggiornamento per Windows Vista (vedere <https://go.microsoft.com/fwlink/p/?linkid=160189> ).

Windows Vista Service Pack 1 include una versione aggiornata del runtime di DirectX. Questo aggiornamento estende il supporto di Windows Vista per includere Direct3D 10,1, esponendo nuove funzionalità hardware facoltative. (Tutto l'hardware in grado di supportare Direct3D 10,1 supporta completamente tutte le funzionalità di Direct3D 10).

DirectSound è stato aggiornato per esporre le funzionalità del nuovo stack di driver audio di Windows Vista, che supporta i buffer software multicanale. L'API modalità mantenuta Direct3D è stata completamente rimossa da Windows Vista. È stata anche rimossa la voce DirectPlay, oltre all'interfaccia utente di DirectPlay Helper NAT e DirectInput Action-Mapper. Il supporto per le interfacce DirectX 7 e DirectX 8 per Visual Basic 6,0 non è disponibile in Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_7__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_7__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_7__"></span>**Quali modifiche sono state apportate a DirectX Runtime per Windows 7?** 
</dt> <dd>

Windows 7 include tutti i componenti runtime di DirectX disponibili in Windows Vista e aggiunge i livelli di funzionalità Direct3D 11, DXGI 1,1, 10Level9, WARP10 software, Direct2D, DirectWrite e un aggiornamento a Direct3D 10,1 per supportare 10Level9 e WARP10. Per altre informazioni, vedere [API grafiche in Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista).

Tutti gli altri componenti sono identici a quelli di Windows Vista, con l'aggiunta del supporto nativo a 64 bit (x64) per l'API DirectMusic principale correlata al MIDI con timestamp. Il livello di prestazioni di DirectMusic rimane deprecato ed è disponibile solo per le applicazioni a 32 bit in Windows 7 per la compatibilità delle applicazioni. Si noti che il supporto nativo a 64 bit di DirectMusic non è disponibile in Windows Vista.

</dd> <dt>

<span id="I_think_I_have_found_a_driver_bug__what_do_I_do__"></span><span id="i_think_i_have_found_a_driver_bug__what_do_i_do__"></span><span id="I_THINK_I_HAVE_FOUND_A_DRIVER_BUG__WHAT_DO_I_DO__"></span>**Credo di aver trovato un bug del driver, cosa devo fare?** 
</dt> <dd>

Assicurarsi prima di tutto di avere verificato i risultati con l'rasterizzazione dei riferimenti. Verificare quindi i risultati con la versione certificata WHQL più recente del driver IHV. È possibile controllare a livello di codice lo stato di WHQL usando il metodo GetAdapterIdentifier () sull'interfaccia IDirect3D9 passando il flag del livello di D3DENUM \_ WHQL \_ .

</dd> <dt>

<span id="Why_do_I_get_so_many_error_messages_when_I_try_to_compile_the_samples__"></span><span id="why_do_i_get_so_many_error_messages_when_i_try_to_compile_the_samples__"></span><span id="WHY_DO_I_GET_SO_MANY_ERROR_MESSAGES_WHEN_I_TRY_TO_COMPILE_THE_SAMPLES__"></span>**Perché si ottengono molti messaggi di errore quando si tenta di compilare gli esempi?** 
</dt> <dd>

Probabilmente il percorso di inclusione non è impostato correttamente. Molti compilatori, tra cui Microsoft Visual C++, includono una versione precedente dell'SDK, pertanto se il percorso di inclusione cerca prima le directory di inclusione del compilatore standard, si otterranno versioni non corrette dei file di intestazione. Per risolvere questo problema, assicurarsi che il percorso di inclusione e i percorsi di libreria siano impostati per eseguire prima la ricerca nei percorsi di inclusione e raccolta di Microsoft DirectX. Vedere anche il file di dxreadme.txt nell'SDK. Se si installa DirectX SDK e si utilizza Visual C++, il programma di installazione può facoltativamente impostare i percorsi di inclusione.

</dd> <dt>

<span id="I_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__GUIDs___what_do_I_do__"></span><span id="i_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__guids___what_do_i_do__"></span><span id="I_GET_LINKER_ERRORS_ABOUT_MULTIPLE_OR_MISSING_SYMBOLS_FOR_GLOBALLY_UNIQUE_IDENTIFIERS__GUIDS___WHAT_DO_I_DO__"></span>**Si ottengono errori del linker relativi a simboli multipli o mancanti per gli identificatori univoci globali (GUID), cosa devo fare?** 
</dt> <dd>

I vari GUID usati devono essere definiti una sola volta. La definizione del GUID verrà inserita se si \# definisce il simbolo INITGUID prima di includere i file di intestazione DirectX. Pertanto, è necessario assicurarsi che questo avvenga solo per un'unità di compilazione. Un'alternativa a questo metodo consiste nel collegarsi alla libreria dxguid. lib, che contiene le definizioni per tutti i GUID DirectX. Se si usa questo metodo (scelta consigliata), non è mai necessario \# definire il simbolo INITGUID.

</dd> <dt>

<span id="Can_I_cast_a_pointer_to_a_DirectX_interface_to_a_lower_version_number__"></span><span id="can_i_cast_a_pointer_to_a_directx_interface_to_a_lower_version_number__"></span><span id="CAN_I_CAST_A_POINTER_TO_A_DIRECTX_INTERFACE_TO_A_LOWER_VERSION_NUMBER__"></span>**È possibile eseguire il cast di un puntatore a un'interfaccia DirectX a un numero di versione inferiore?** 
</dt> <dd>

No. Le interfacce DirectX sono interfacce COM. Ciò significa che non esiste alcun requisito per la derivazione di interfacce numerate più elevate da quelle corrispondenti con numeri inferiori. Pertanto, l'unico modo sicuro per ottenere un'interfaccia diversa per un oggetto DirectX consiste nell'usare il metodo QueryInterface dell'interfaccia. Questo metodo fa parte dell'interfaccia IUnknown standard, da cui devono derivare tutte le interfacce COM.

</dd> <dt>

<span id="Can_I_mix_the_use_of_DirectX_9_components_and_DirectX_8_or_earlier_components_within_the_same_application__"></span><span id="can_i_mix_the_use_of_directx_9_components_and_directx_8_or_earlier_components_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECTX_9_COMPONENTS_AND_DIRECTX_8_OR_EARLIER_COMPONENTS_WITHIN_THE_SAME_APPLICATION__"></span>**È possibile combinare l'uso di componenti DirectX 9 e DirectX 8 o componenti precedenti all'interno della stessa applicazione?** 
</dt> <dd>

È possibile combinare liberamente diversi componenti della versione diversa; ad esempio, è possibile usare DirectInput 8 con Direct3D 9 nella stessa applicazione. Tuttavia, in genere non è possibile combinare versioni diverse dello stesso componente all'interno della stessa applicazione. ad esempio, non è possibile combinare DirectDraw 7 con Direct3D 9 (poiché si tratta effettivamente dello stesso componente di DirectDraw è stato sostituito in Direct3D a partire da DirectX 8). Esistono tuttavia alcune eccezioni, ad esempio l'uso di Direct3D 9 e Direct3D 10 insieme nella stessa applicazione, che è consentita.

</dd> <dt>

<span id="Can_I_mix_the_use_of_Direct3D_9_and_Direct3D_10_within_the_same_application__"></span><span id="can_i_mix_the_use_of_direct3d_9_and_direct3d_10_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECT3D_9_AND_DIRECT3D_10_WITHIN_THE_SAME_APPLICATION__"></span>**È possibile combinare l'uso di Direct3D 9 e Direct3D 10 all'interno della stessa applicazione?** 
</dt> <dd>

Sì, è possibile usare queste versioni di Direct3D insieme nella stessa applicazione.

</dd> <dt>

<span id="What_do_the_return_values_from_the_Release_or_AddRef_methods_mean__"></span><span id="what_do_the_return_values_from_the_release_or_addref_methods_mean__"></span><span id="WHAT_DO_THE_RETURN_VALUES_FROM_THE_RELEASE_OR_ADDREF_METHODS_MEAN__"></span>**Cosa significano i valori restituiti dai metodi Release o AddRef?** 
</dt> <dd>

Il valore restituito sarà il conteggio dei riferimenti correnti dell'oggetto. Tuttavia, la specifica COM dichiara che non si deve fare affidamento su questo e il valore è in genere disponibile solo a scopo di debug. I valori osservati potrebbero essere imprevisti poiché diversi altri oggetti di sistema possono contenere riferimenti agli oggetti DirectX creati. Per questo motivo, non è necessario scrivere codice che chiama ripetutamente release fino a quando il conteggio dei riferimenti non è zero, in quanto l'oggetto può essere liberato anche se un altro componente può ancora farvi riferimento.

</dd> <dt>

<span id="Does_it_matter_in_which_order_I_release_DirectX_interfaces__"></span><span id="does_it_matter_in_which_order_i_release_directx_interfaces__"></span><span id="DOES_IT_MATTER_IN_WHICH_ORDER_I_RELEASE_DIRECTX_INTERFACES__"></span>**È importante l'ordine in cui vengono rilasciate le interfacce DirectX?** 
</dt> <dd>

Non dovrebbe essere importante perché le interfacce COM sono conteggiate come riferimento. Tuttavia, esistono alcuni bug noti con l'ordine di rilascio delle interfacce in alcune versioni di DirectX. Per garantire la sicurezza, è consigliabile rilasciare le interfacce in ordine di creazione inversa quando possibile.

</dd> <dt>

<span id="What_is_a_smart_pointer_and_should_I_use_it__"></span><span id="what_is_a_smart_pointer_and_should_i_use_it__"></span><span id="WHAT_IS_A_SMART_POINTER_AND_SHOULD_I_USE_IT__"></span>**Che cos'è un puntatore intelligente ed è consigliabile usarlo?** 
</dt> <dd>

Un puntatore intelligente è una classe modello C++ progettata per incapsulare la funzionalità del puntatore. In particolare, sono disponibili classi di puntatore intelligente standard progettate per incapsulare i puntatori di interfaccia COM. Questi puntatori eseguono automaticamente QueryInterface anziché un cast e gestiscono AddRef e release. La possibilità di usarle è in gran parte una questione di gusto. Se il codice contiene un numero elevato di copie di puntatori di interfaccia con più AddRefs e versioni, i puntatori intelligenti possono probabilmente rendere il codice più semplice e meno soggetto a errori. In caso contrario, è possibile eseguire l'operazione senza di esse. Visual C++ include un puntatore intelligente Microsoft COM standard, definito nel file di intestazione "Comdef. h" (cercare com \_ ptr \_ t nella Guida).

</dd> <dt>

<span id="I_have_trouble_debugging_my_DirectX_application__any_tips__"></span><span id="i_have_trouble_debugging_my_directx_application__any_tips__"></span><span id="I_HAVE_TROUBLE_DEBUGGING_MY_DIRECTX_APPLICATION__ANY_TIPS__"></span>**Si verificano problemi durante il debug dell'applicazione DirectX, eventuali suggerimenti?** 
</dt> <dd>

Il problema più comune del debug delle applicazioni DirectX è il tentativo di eseguire il debug mentre è bloccata una superficie DirectDraw. Questa situazione può causare un "blocco Win16" nei sistemi Microsoft Windows 9x, che impedisce il disegno della finestra del debugger. La specifica del \_ flag D3DLOCK NOSYSLOCK quando si blocca la superficie può in genere eliminare questo problema. Windows 2000 non subisce questo problema. Quando si sviluppa un'applicazione, è utile eseguire con la versione di debug di DirectX Runtime (selezionata quando si installa l'SDK), che esegue una convalida dei parametri e restituisce messaggi utili all'output del debugger.

</dd> <dt>

<span id="What_s_the_correct_way_to_check_return_codes__"></span><span id="what_s_the_correct_way_to_check_return_codes__"></span><span id="WHAT_S_THE_CORRECT_WAY_TO_CHECK_RETURN_CODES__"></span>**Qual è il modo corretto per controllare i codici restituiti?** 
</dt> <dd>

Utilizzare le macro SUCCEEDed e FAILED. I metodi DirectX possono restituire più codici di esito positivo e negativo, quindi un semplice:

``` syntax
== D3D_OK
```

o un test simile non è sempre sufficiente.

</dd> <dt>

<span id="How_do_I_disable_ALT_TAB_and_other_task_switching__"></span><span id="how_do_i_disable_alt_tab_and_other_task_switching__"></span><span id="HOW_DO_I_DISABLE_ALT_TAB_AND_OTHER_TASK_SWITCHING__"></span>**Ricerca per categorie disabilitare ALT + TAB e altre attività di cambio?** 
</dt> <dd>

Non è possibile. I giochi devono essere in grado di gestire correttamente il cambio di attività, in quanto molti di essi provocano l'evento: ALT + TAB, connessioni Desktop remoto, cambio rapido utente, limiti di utilizzo dei controlli padre e molti altri eventi.

Allo stesso tempo, due origini comuni di attività accidentali che passano a giochi con schemi di controllo incentrati sulla tastiera sono la pressione del tasto logo Windows e l'attivazione della funzionalità di accessibilità StickyKeys con il tasto MAIUSC. Per risolvere questi casi disabilitando la funzionalità, vedere le tecniche descritte in [disabilitazione dei tasti di scelta rapida nei giochi](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Is_there_a_recommended_book_explaining_COM__"></span><span id="is_there_a_recommended_book_explaining_com__"></span><span id="IS_THERE_A_RECOMMENDED_BOOK_EXPLAINING_COM__"></span>**C'è un libro consigliato che spiega COM?** 
</dt> <dd>

*All'interno di com* , Dale Rogerson, pubblicato da Microsoft Press, è un'ottima introduzione a com. Per un'analisi più dettagliata di COM, è consigliabile usare anche il libro *Essential com* by Don Box, pubblicato da Longman.

</dd> <dt>

<span id="What_is_managed_code__"></span><span id="what_is_managed_code__"></span><span id="WHAT_IS_MANAGED_CODE__"></span>**Che cos'è il codice gestito?** 
</dt> <dd>

Il codice gestito è un codice in cui l'esecuzione viene gestita dal .NET Framework Common Language Runtime (CLR). Si riferisce a un contratto di collaborazione tra l'esecuzione nativa del codice e il Runtime. Questo contratto specifica che in qualsiasi punto di esecuzione, il runtime può arrestare una CPU in esecuzione e recuperare informazioni specifiche per l'indirizzo di istruzione della CPU corrente. Le informazioni che devono essere in grado di eseguire query sono in genere relative allo stato di runtime, ad esempio il contenuto del registro o della memoria dello stack.

Prima dell'esecuzione del codice, il linguaggio il viene compilato in codice eseguibile nativo. Poiché questa compilazione viene eseguita dall'ambiente di esecuzione gestita (o, in modo più corretto, da un compilatore compatibile con il runtime che sa come definire come destinazione l'ambiente di esecuzione gestito), l'ambiente di esecuzione gestito può garantire le informazioni sulle operazioni eseguite dal codice. Può inserire trap e Hook Garbage Collection appropriati, la gestione delle eccezioni, l'indipendenza dai tipi, i limiti della matrice e il controllo degli indici e così via. Un compilatore di questo tipo, ad esempio, garantisce la disposizione degli stack frame e tutti gli elementi giusti, in modo che il Garbage Collector possa essere eseguito in background in un thread separato, esaminando costantemente lo stack di chiamate attivo, individuando tutte le radici, eseguendo la ricerca di tutti gli oggetti attivi. Inoltre, poiché il ha una nozione di indipendenza dai tipi, il motore di esecuzione manterrà la garanzia di indipendenza dai tipi eliminando un'intera classe di errori di programmazione che spesso portano a buchi di sicurezza.

Contrariamente al mondo non gestito: i file eseguibili non gestiti sono fondamentalmente un'immagine binaria, il codice x86, caricato in memoria. Il contatore del programma viene inserito ed è l'ultimo che conosce il sistema operativo. Sono disponibili protezioni per la gestione della memoria e l'I/O della porta e così via, ma il sistema non conosce effettivamente le operazioni svolte dall'applicazione. Pertanto, non può garantire alcuna garanzia su cosa accade quando viene eseguita l'applicazione.

</dd> <dt>

<span id="What_books_are_there_about_general_Windows_programming__"></span><span id="what_books_are_there_about_general_windows_programming__"></span><span id="WHAT_BOOKS_ARE_THERE_ABOUT_GENERAL_WINDOWS_PROGRAMMING__"></span>**Quali sono i libri sulla programmazione generale di Windows?** 
</dt> <dd>

Lotti. Tuttavia, i due consigliati sono:

-   Programmazione di Windows da Charles Petzold (Microsoft Press)
-   Programmazione di applicazioni per Windows di Jeffrey Richter (Microsoft Press)

</dd> <dt>

<span id="How_do_I_debug_using_the_Windows_symbol_files__"></span><span id="how_do_i_debug_using_the_windows_symbol_files__"></span><span id="HOW_DO_I_DEBUG_USING_THE_WINDOWS_SYMBOL_FILES__"></span>**Ricerca per categorie eseguire il debug usando i file di simboli di Windows?** 
</dt> <dd>

Microsoft pubblica i simboli rimossi per tutte le DLL di sistema (più altri). Per accedervi, aggiungere quanto segue al percorso dei simboli nelle impostazioni del progetto all'interno di Visual Studio:

``` syntax
srv*https://msdl.microsoft.com/download/symbols
```

per la memorizzazione nella cache dei simboli localmente, usare la sintassi seguente:

``` syntax
srv*c:\cache*https://msdl.microsoft.com/download/symbols
```

Dove c: \\ cache è una directory locale per la memorizzazione nella cache dei file di simboli.

</dd> </dl>

## <a name="direct3d-questions"></a>Domande su Direct3D

### <a name="general-direct3d-questions"></a>Domande generali su Direct3D

<dl> <dt>

<span id="Where_can_I_find_information_about_3D_graphics_techniques__"></span><span id="where_can_i_find_information_about_3d_graphics_techniques__"></span><span id="WHERE_CAN_I_FIND_INFORMATION_ABOUT_3D_GRAPHICS_TECHNIQUES__"></span>**Dove è possibile reperire informazioni sulle tecniche grafiche 3D?** 
</dt> <dd>

Il libro standard sul tema è la grafica dei computer: principi e prassi di Foley, Van Dam et al. Si tratta di una risorsa preziosa per chiunque desideri comprendere le fondamenta matematiche delle tecniche di geometria, rasterizzazione e illuminazione. Le domande frequenti per il gruppo comp. graphics. Algorithms Usenet contengono anche materiale utile.

</dd> <dt>

<span id="Does_Direct3D_emulate_functionality_not_provided_by_hardware__"></span><span id="does_direct3d_emulate_functionality_not_provided_by_hardware__"></span><span id="DOES_DIRECT3D_EMULATE_FUNCTIONALITY_NOT_PROVIDED_BY_HARDWARE__"></span>**Direct3D emula la funzionalità non fornita dall'hardware?** 
</dt> <dd>

Dipende. Direct3D ha una pipeline di elaborazione dei vertici software completa (incluso il supporto per i vertex shader personalizzati). Tuttavia, non viene fornita alcuna emulazione per le operazioni a livello di pixel; le applicazioni devono controllare i bit di estremità appropriati e usare l'API ValidateDevice per determinare il supporto.

</dd> <dt>

<span id="Is_there_a_software_rasterizer_included_with_Direct3D__"></span><span id="is_there_a_software_rasterizer_included_with_direct3d__"></span><span id="IS_THERE_A_SOFTWARE_RASTERIZER_INCLUDED_WITH_DIRECT3D__"></span>**È disponibile un rasterizzatore software incluso in Direct3D?** 
</dt> <dd>

Non per le applicazioni per le prestazioni. Viene fornita un'unità di rasterizzazione dei riferimenti per la convalida del driver, ma l'implementazione è progettata per l'accuratezza e non per le prestazioni. Direct3D supporta i rasterizzatori del software plug-in.

</dd> <dt>

<span id="How_can_I_perform_color_keying_with_DirectX_graphics__"></span><span id="how_can_i_perform_color_keying_with_directx_graphics__"></span><span id="HOW_CAN_I_PERFORM_COLOR_KEYING_WITH_DIRECTX_GRAPHICS__"></span>**Come è possibile eseguire la trasparenza dei colori con la grafica DirectX?** 
</dt> <dd>

La chiave di colore non è supportata direttamente, ma sarà necessario usare la fusione alfa per emulare la chiave di colore. Per semplificare questa operazione, è possibile usare la funzione D3DXCreateTextureFromFileEx (). Questa funzione accetta un parametro di colore della chiave e sostituirà tutti i pixel dell'immagine di origine contenente il colore specificato con i pixel neri trasparenti nella trama creata.

</dd> <dt>

<span id="Does_the_Direct3D_geometry_code_utilize_3DNow__and_or_Pentium_III_SIMD_instructions__"></span><span id="does_the_direct3d_geometry_code_utilize_3dnow__and_or_pentium_iii_simd_instructions__"></span><span id="DOES_THE_DIRECT3D_GEOMETRY_CODE_UTILIZE_3DNOW__AND_OR_PENTIUM_III_SIMD_INSTRUCTIONS__"></span>**Il codice di geometria Direct3D usa le istruzioni SIMD 3DNow! e/o Pentium III?** 
</dt> <dd>

Sì. La pipeline di geometria Direct3D include diversi percorsi di codice, a seconda del tipo di processore, e utilizzerà le speciali operazioni a virgola mobile fornite da 3DNow. o le istruzioni SIMD Pentium III in cui sono disponibili. Questa operazione include l'elaborazione di vertex shader personalizzati.

</dd> <dt>

<span id="How_do_I_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="how_do_i_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="HOW_DO_I_PREVENT_TRANSPARENT_PIXELS_BEING_WRITTEN_TO_THE_Z-BUFFER__"></span>**Ricerca per categorie impedire che i pixel trasparenti vengano scritti nel buffer z?** 
</dt> <dd>

È possibile filtrare i pixel con un valore alfa al di sopra o al di sotto di una determinata soglia. Per controllare questo comportamento, usare renderstates ALPHATESTENABLE, ALPHAREF e ALPHAFUNC.

</dd> <dt>

<span id="What_is_a_stencil_buffer__"></span><span id="what_is_a_stencil_buffer__"></span><span id="WHAT_IS_A_STENCIL_BUFFER__"></span>**Che cos'è un buffer di stencil?** 
</dt> <dd>

Un buffer di stencil è un buffer aggiuntivo di informazioni per pixel, molto simile a un buffer z. Infatti, si trova in alcuni dei bit di un buffer z. I formati comuni per gli stencil e i buffer z sono a 15 bit a z e a 1 bit, oppure a 24 bit z e a 8 bit. È possibile eseguire semplici operazioni aritmetiche sul contenuto del buffer dello stencil in base ai singoli pixel, quando viene eseguito il rendering dei poligoni. Ad esempio, il buffer dello stencil può essere incrementato o decrementato oppure il pixel può essere rifiutato se il valore dello stencil non riesce a eseguire un semplice test di confronto. Questa operazione è utile per gli effetti che comportano il contrassegno di un'area del buffer dei frame e l'esecuzione del rendering solo dell'area contrassegnata (o non contrassegnata). Esempi validi sono gli effetti volumetrici come i volumi shadow.

</dd> <dt>

<span id="How_do_I_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="how_do_i_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="HOW_DO_I_USE_A_STENCIL_BUFFER_TO_RENDER_SHADOW_VOLUMES__"></span>**Ricerca per categorie utilizzare un buffer di stencil per eseguire il rendering dei volumi shadow?** 
</dt> <dd>

La chiave per questo e altri effetti del buffer di stencil volumetrico è l'interazione tra il buffer dello stencil e il buffer z. Viene eseguito il rendering di una scena con un volume shadow in tre fasi. Per prima cosa, viene eseguito il rendering della scena senza l'ombreggiatura, usando il buffer z. L'ombreggiatura viene quindi contrassegnata nel buffer dello stencil come indicato di seguito. I front-end del volume shadow vengono disegnati usando poligoni invisibili, con il test z abilitato, ma le Scritture z disabilitate e il buffer dello stencil viene incrementato a ogni pixel passando il test z. Il rendering dei volti indietro del volume shadow viene eseguito in modo analogo, ma decremento invece il valore dello stencil.

A questo punto, si consideri un singolo pixel. Supponendo che la fotocamera non si trovi nel volume ombreggiato, sono disponibili quattro possibilità per il punto corrispondente nella scena. Se il raggio dalla fotocamera al punto non interseca il volume shadow, non verrà disegnato alcun poligono ombreggiato e il buffer dello stencil è ancora zero. In caso contrario, se il punto si trova davanti al volume ombreggiato, i poligoni shadow verranno memorizzati nel buffer z e lo stencil rimarrà invariato. Se i punti si trovano dietro il volume dell'ombreggiatura, sarà stato eseguito il rendering dello stesso numero di facce di ombreggiatura anteriore dei volti indietro e lo stencil sarà pari a zero, che è stato incrementato il numero di volte che diminuisce.

La possibilità finale è che il punto si trovi all'interno del volume shadow. In questo caso, il lato posteriore del volume shadow verrà memorizzato nel buffer z, ma non in quello anteriore, quindi il buffer dello stencil sarà un valore diverso da zero. Il risultato è che le parti del buffer del frame che si trovano nell'ombreggiatura hanno un valore di stencil diverso da zero. Infine, per eseguire effettivamente il rendering dell'ombreggiatura, l'intera scena viene trascinata con un poligono con alfa blend impostato in modo da influire solo sui pixel con un valore stencil diverso da zero. Un esempio di questa tecnica può essere illustrato nell'esempio "Volume Shadow" incluso in DirectX SDK.

</dd> <dt>

<span id="What_are_the_texel_alignment_rules__How_do_I_get_a_one-to-one_mapping__"></span><span id="what_are_the_texel_alignment_rules__how_do_i_get_a_one-to-one_mapping__"></span><span id="WHAT_ARE_THE_TEXEL_ALIGNMENT_RULES__HOW_DO_I_GET_A_ONE-TO-ONE_MAPPING__"></span>**Quali sono le regole di allineamento Texel? Ricerca per categorie ottenere un mapping uno-a-uno?** 
</dt> <dd>

Questa operazione è descritta completamente nella documentazione di Direct3D 9. Tuttavia, il riepilogo generale è che è necessario polarizzare le coordinate dello schermo per-0,5 di un pixel per allinearsi correttamente con i Texel. La maggior parte delle schede è ora conforme correttamente alle regole di allineamento Texel, tuttavia esistono alcune schede o driver meno recenti. Per gestire questi casi, è consigliabile contattare il fornitore dell'hardware in questione e richiedere driver aggiornati o la soluzione alternativa consigliata. Si noti che in Direct3D 10 questa regola non include più.

</dd> <dt>

<span id="What_is_the_purpose_of_the_D3DCREATE_PUREDEVICE_flag__"></span><span id="what_is_the_purpose_of_the_d3dcreate_puredevice_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_D3DCREATE_PUREDEVICE_FLAG__"></span>**Qual è lo scopo del \_ flag PUREDEVICE di D3DCREATE?** 
</dt> <dd>

Usare il \_ flag PUREDEVICE di D3DCREATE durante la creazione del dispositivo per creare un dispositivo puro. Un dispositivo puro non salva lo stato corrente (durante le modifiche di stato), che spesso migliora le prestazioni. Questo dispositivo richiede anche l'elaborazione dei vertici hardware. Un dispositivo puro viene in genere usato quando vengono completati lo sviluppo e il debug e si desidera ottenere prestazioni ottimali.

Uno svantaggio di un dispositivo puro è che non supporta tutte le chiamate API Get. Ciò significa che non è \* possibile usare un dispositivo pure per eseguire query sullo stato della pipeline. Questo rende più difficile eseguire il debug durante l'esecuzione di un'applicazione. Di seguito è riportato un elenco di tutti i metodi disabilitati da un dispositivo pure.

-   [**IDirect3DDevice9:: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane)
-   [**IDirect3DDevice9:: GetClipStatus**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipstatus)
-   [**IDirect3DDevice9:: getlight**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight)
-   [**IDirect3DDevice9:: getalleggeriscible**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable)
-   [**IDirect3DDevice9:: getmaterial**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getmaterial)
-   [**IDirect3DDevice9:: GetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf)
-   [**IDirect3DDevice9:: GetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstanti)
-   [**IDirect3DDevice9:: GetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantb)
-   [**IDirect3DDevice9:: GetRenderState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrenderstate)
-   [**IDirect3DDevice9:: GetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsamplerstate)
-   [**IDirect3DDevice9:: GetTextureStageState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate)
-   [**IDirect3DDevice9:: GetTransform**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettransform)
-   [**IDirect3DDevice9:: GetVertexShaderConstantF**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantf)
-   [**IDirect3DDevice9:: GetVertexShaderConstantI**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstanti)
-   [**IDirect3DDevice9:: GetVertexShaderConstantB**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantb)

Un secondo svantaggio di un dispositivo puro è che non filtra le modifiche di stato ridondanti. Quando si usa un dispositivo puro, l'applicazione deve ridurre al minimo il numero di modifiche di stato nel ciclo di rendering. Questo può includere modifiche allo stato del filtro per assicurarsi che gli Stati non vengano impostati più di una volta. Questo compromesso dipende dall'applicazione. Se si usano più di un set di 1000 chiamate per fotogramma, è consigliabile sfruttare i vantaggi del filtro di ridondanza che viene eseguito automaticamente da un dispositivo non puro.

Come per tutti i problemi di prestazioni, l'unico modo per sapere se l'applicazione verrà eseguita meglio con un dispositivo puro consiste nel confrontare le prestazioni dell'applicazione con un dispositivo puro e non puro. Un dispositivo puro può velocizzare l'applicazione riducendo il sovraccarico della CPU dell'API. Prestare attenzione. Per alcuni scenari, un dispositivo puro rallenterà l'applicazione (a causa del lavoro aggiuntivo della CPU causato da modifiche di stato ridondanti). Se non si è certi del tipo di dispositivo più adatto per l'applicazione e non si filtrano le modifiche ridondanti nell'applicazione, usare un dispositivo non puro.

</dd> <dt>

<span id="How_do_I_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="how_do_i_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="HOW_DO_I_ENUMERATE_THE_DISPLAY_DEVICES_IN_A_MULTI-MONITOR_SYSTEM__"></span>**Ricerca per categorie enumerare i dispositivi di visualizzazione in un sistema con più monitor?** 
</dt> <dd>

L'enumerazione può essere eseguita tramite una semplice iterazione da parte dell'applicazione usando i metodi dell'interfaccia IDirect3D9. Chiamare GetAdapterCount per determinare il numero di schede di visualizzazione nel sistema. Chiamare GetAdapterMonitor per determinare il monitor fisico a cui è connessa una scheda (questo metodo restituisce un HMONITOR, che è quindi possibile usare nell'API Win32 GetMonitorInfo per determinare le informazioni sul monitoraggio fisico). Determinare le caratteristiche di una particolare scheda di visualizzazione o creare un dispositivo Direct3D su tale scheda è semplice quanto passare il numero di adapter appropriato al posto di D3DADAPTER \_ default durante la chiamata di GetDeviceCaps, CreateDevice o altri metodi.

</dd> <dt>

<span id="What_happened_to_Fixed_Function_Bumpmapping_in_D3D9__"></span><span id="what_happened_to_fixed_function_bumpmapping_in_d3d9__"></span><span id="WHAT_HAPPENED_TO_FIXED_FUNCTION_BUMPMAPPING_IN_D3D9__"></span>**Cosa è successo alla funzione Fixed Bumpmapping in D3D9?** 
</dt> <dd>

A partire da Direct3D 9 è stata ristretta la convalida sulle schede che potevano supportare solo > 2 trame simultanee. Alcune schede meno recenti hanno solo 3 fasi di trama disponibili quando si usa un'operazione Alpha modulare specifica. L'utilizzo più comune usato dalle 3 fasi per è emboss Bumpmapping ed è comunque possibile eseguire questa operazione con D3D9.

Il campo height deve essere archiviato nel canale alfa e viene usato per modulare il contributo delle luci, ovvero:

``` syntax
// Stage 0 is the base texture, with the height map in the alpha channel
m_pd3dDevice->SetTexture(0, m_pEmbossTexture );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 0 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP,   D3DTOP_MODULATE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP,   D3DTOP_SELECTARG1 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE );
if( m_bShowEmbossMethod )
{
 // Stage 1 passes through the RGB channels (SELECTARG2 = CURRENT), and 
 // does a signed add with the inverted alpha channel. 
 // The texture coords associated with Stage 1 are the shifted ones, so 
 // the result is:
 //    (height - shifted_height) * tex.RGB * diffuse.RGB
   m_pd3dDevice->SetTexture( 1, m_pEmbossTexture );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_SELECTARG2 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAOP, D3DTOP_ADDSIGNED );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG1, D3DTA_TEXTURE|D3DTA_COMPLEMENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG2, D3DTA_CURRENT );

   // Set up the alpha blender to multiply the alpha channel 
   // (monochrome emboss) with the src color (lighted texture)
   m_pd3dDevice->SetRenderState( D3DRS_ALPHABLENDENABLE, TRUE );
   m_pd3dDevice->SetRenderState( D3DRS_SRCBLEND,  D3DBLEND_SRCALPHA );
   m_pd3dDevice->SetRenderState( D3DRS_DESTBLEND, D3DBLEND_ZERO );
}
```

Questo esempio, insieme ad altri esempi meno recenti, non viene più fornito nella versione corrente di SDK e non verrà fornito nelle versioni future dell'SDK.

</dd> </dl>

### <a name="geometry-vertex-processing"></a>Elaborazione Geometry (Vertex)

<dl> <dt>

<span id="Vertex_streams_confuse_me_how_do_they_work__"></span><span id="vertex_streams_confuse_me_how_do_they_work__"></span><span id="VERTEX_STREAMS_CONFUSE_ME_HOW_DO_THEY_WORK__"></span>**I flussi di vertici confondeno come funzionano?** 
</dt> <dd>

Direct3D assembla ogni vertice inserito nella parte di elaborazione della pipeline da uno o più flussi di vertici. Avere un solo flusso di vertici corrisponde al modello precedente a DirectX 8, in cui i vertici provengono da un'unica origine. Con DirectX 8, i diversi componenti Vertex possono provenire da origini diverse. un buffer dei vertici, ad esempio, può contenere le posizioni e le normali, mentre un secondo mantiene i valori di colore e le coordinate di trama.

</dd> <dt>

<span id="What_is_a_vertex_shader__"></span><span id="what_is_a_vertex_shader__"></span><span id="WHAT_IS_A_VERTEX_SHADER__"></span>**Che cos'è un vertex shader?** 
</dt> <dd>

Un vertex shader è una procedura per l'elaborazione di un singolo vertice. Viene definito usando un semplice linguaggio simile a un assembly assemblato dalla libreria di utilità D3DX in un flusso di token accettato da Direct3D. Il vertex shader accetta come input un singolo vertice e un set di valori costanti; Restituisce una posizione del vertice (nello spazio di ritaglio) e, facoltativamente, un set di colori e coordinate di trama, usati per la rasterizzazione. Si noti che quando si dispone di un vertex shader personalizzato, i componenti dei vertici non hanno più una semantica applicata da Direct3D e i vertici sono semplicemente dati arbitrari interpretati dal vertex shader creato.

</dd> <dt>

<span id="Does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="DOES_A_VERTEX_SHADER_PERFORM_PERSPECTIVE_DIVISION_OR_CLIPPING__"></span>**Un vertex shader esegue la divisione o il ritaglio prospettico?** 
</dt> <dd>

No. Il vertex shader restituisce una coordinata omogenea nello spazio di ritaglio per la posizione del vertice trasformato. La divisione prospettica e il ritaglio vengono eseguiti automaticamente dopo lo shader.

</dd> <dt>

<span id="Can_I_generate_geometry_with_a_vertex_shader__"></span><span id="can_i_generate_geometry_with_a_vertex_shader__"></span><span id="CAN_I_GENERATE_GEOMETRY_WITH_A_VERTEX_SHADER__"></span>**È possibile generare la geometria con un vertex shader?** 
</dt> <dd>

Un vertex shader non è in grado di creare o distruggere i vertici; opera su un singolo vertice alla volta, accettando un vertice non elaborato come input e l'output di un singolo vertice elaborato. Può quindi essere usato per modificare la geometria esistente (applicando le deformazioni o l'esecuzione di operazioni di skinning) ma non può generare effettivamente una nuova geometria per se.

</dd> <dt>

<span id="Can_I_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="can_i_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="CAN_I_APPLY_A_CUSTOM_VERTEX_SHADER_TO_THE_RESULTS_OF_THE_FIXED-FUNCTION_GEOMETRY_PIPELINE__OR_VICE-VERSA___"></span>**È possibile applicare un vertex shader personalizzato ai risultati della pipeline di geometria a funzione fissa (o viceversa)?** 
</dt> <dd>

No. È necessario scegliere l'uno o l'altro. Se si usa un vertex shader personalizzato, si è responsabili dell'esecuzione dell'intera trasformazione del vertice.

</dd> <dt>

<span id="Can_I_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="can_i_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="CAN_I_USE_A_CUSTOM_VERTEX_SHADER_IF_MY_HARDWARE_DOES_NOT_SUPPORT_IT__"></span>**È possibile usare un vertex shader personalizzato se l'hardware non lo supporta?** 
</dt> <dd>

Sì. Il motore di elaborazione dei vertici software Direct3D supporta completamente i vertex shader personalizzati con un livello di prestazioni sorprendentemente elevato.

</dd> <dt>

<span id="How_do_I_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="how_do_i_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="HOW_DO_I_DETERMINE_IF_THE_HARDWARE_SUPPORTS_MY_CUSTOM_VERTEX_SHADER__"></span>**Ricerca per categorie determinare se l'hardware supporta il vertex shader personalizzato?** 
</dt> <dd>

I dispositivi in grado di supportare vertex shader nell'hardware sono necessari per compilare il campo D3DCAPS9:: VertexShaderVersion per indicare il livello di versione del vertex shader supportato. Qualsiasi dispositivo che richiede il supporto di un determinato livello di vertex shader deve supportare tutti i vertex shader validi che soddisfano le specifiche per tale livello o sotto.

</dd> <dt>

<span id="How_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="how_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="HOW_MANY_CONSTANT_REGISTERS_ARE_AVAILABLE_FOR_VERTEX_SHADERS__"></span>**Quanti registri costanti sono disponibili per i vertex shader?** 
</dt> <dd>

I dispositivi che supportano Visual Studio 1,0 vertex shader sono necessari per supportare un minimo di 96 registri costanti. I dispositivi possono supportare più di questo numero minimo e possono segnalarlo tramite il campo D3DCAPS9:: MaxVertexShaderConst.

</dd> <dt>

<span id="Can_I_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="can_i_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="CAN_I_SHARE_POSITION_DATA_BETWEEN_VERTICES_WITH_DIFFERENT_TEXTURE_COORDINATES__"></span>**È possibile condividere i dati di posizione tra i vertici con coordinate di trama diverse?** 
</dt> <dd>

Il solito esempio di questa situazione è costituito da un cubo in cui si desidera utilizzare una trama diversa per ogni viso. Sfortunatamente, la risposta è no. non è attualmente possibile indicizzare i componenti Vertex in modo indipendente. Anche con più flussi di vertici, tutti i flussi vengono indicizzati insieme.

</dd> <dt>

<span id="When_I_submit_an_indexed_list_of_primitives__does_Direct3D_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_I_indexed__"></span><span id="when_i_submit_an_indexed_list_of_primitives__does_direct3d_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_i_indexed__"></span><span id="WHEN_I_SUBMIT_AN_INDEXED_LIST_OF_PRIMITIVES__DOES_DIRECT3D_PROCESS_ALL_OF_THE_VERTICES_IN_THE_BUFFER__OR_JUST_THE_ONES_I_INDEXED__"></span>**Quando si invia un elenco indicizzato di primitive, Direct3D elabora tutti i vertici nel buffer o solo quelli indicizzati?** 
</dt> <dd>

Quando si usa la pipeline di geometria software, Direct3D trasforma prima tutti i vertici nell'intervallo inviato, invece di trasformarli "su richiesta" Man mano che vengono indicizzati. Per i dati compressi in modo denso (ovvero in cui viene usata la maggior parte dei vertici), questo è più efficiente, in particolare quando sono disponibili le istruzioni SIMD. Se i dati sono di tipo sparse, ovvero molti vertici non vengono usati, è consigliabile riorganizzare i dati per evitare un numero eccessivo di trasformazioni ridondanti. Quando si usa l'accelerazione della geometria hardware, i vertici vengono in genere trasformati su richiesta quando sono necessari.

</dd> <dt>

<span id="What_is_an_index_buffer__"></span><span id="what_is_an_index_buffer__"></span><span id="WHAT_IS_AN_INDEX_BUFFER__"></span>**Che cos'è un buffer di indice?** 
</dt> <dd>

Un buffer di indice è esattamente analogo a un buffer di vertici, ma contiene indici da usare nelle chiamate DrawIndexedPrimitive. È consigliabile utilizzare buffer di indice anziché la memoria non elaborata allocata dall'applicazione quando possibile, per gli stessi motivi dei buffer dei vertici.

</dd> <dt>

<span id="I_notice_that_32-bit_indices_are_a_supported_type__can_I_use_them_on_all_devices__"></span><span id="i_notice_that_32-bit_indices_are_a_supported_type__can_i_use_them_on_all_devices__"></span><span id="I_NOTICE_THAT_32-BIT_INDICES_ARE_A_SUPPORTED_TYPE__CAN_I_USE_THEM_ON_ALL_DEVICES__"></span>**Si noti che gli indici a 32 bit sono un tipo supportato. è possibile usarli su tutti i dispositivi?** 
</dt> <dd>

No. È necessario controllare il campo D3DCAPS9:: MaxVertexIndex per determinare il valore di indice massimo supportato dal dispositivo. Questo valore deve essere maggiore di 2 alla 16a Power-1 (0xFFFF) per consentire il supporto dei buffer di indice di tipo D3DFMT \_ INDEX32. Si noti inoltre che alcuni dispositivi possono supportare gli indici a 32 bit, ma supportano un valore di indice massimo inferiore a 2 per la 32a Power-1 (0xFFFFFFFF); in questo caso l'applicazione deve rispettare il limite segnalato dal dispositivo.

</dd> <dt>

<span id="Does_S_W_vertex_processing_support_64_bit__"></span><span id="does_s_w_vertex_processing_support_64_bit__"></span><span id="DOES_S_W_VERTEX_PROCESSING_SUPPORT_64_BIT__"></span>**L'elaborazione dei vertici S/W supporta 64 bit?** 
</dt> <dd>

È disponibile una pipeline di vertici s/w ottimizzata per x64, che però non esiste per IA64.

</dd> </dl>

### <a name="performance-tuning"></a>Ottimizzazione delle prestazioni

<dl> <dt>

<span id="How_can_I_improve_the_performance_of_my_Direct3D_application__"></span><span id="how_can_i_improve_the_performance_of_my_direct3d_application__"></span><span id="HOW_CAN_I_IMPROVE_THE_PERFORMANCE_OF_MY_DIRECT3D_APPLICATION__"></span>**Come è possibile migliorare le prestazioni dell'applicazione Direct3D?** 
</dt> <dd>

Di seguito sono elencate le aree principali da esaminare per l'ottimizzazione delle prestazioni:

<dl> <dt>

<span id="Batch_size_"></span><span id="batch_size_"></span><span id="BATCH_SIZE_"></span>**Dimensioni batch** 
</dt> <dd>

Direct3D è ottimizzato per grandi batch di primitive. Maggiore è il numero di poligoni che possono essere inviati in una singola chiamata. Una regola empirica consiste nel puntare alla media dei vertici 1000 per ogni chiamata primitiva. Al di sotto di tale livello è probabile che non si stiano ottenendo prestazioni ottimali e che si stia diminuendo i ritorni e i potenziali conflitti con le considerazioni sulla concorrenza (vedere di seguito).

</dd> <dt>

<span id="State_changes_"></span><span id="state_changes_"></span><span id="STATE_CHANGES_"></span>**Modifiche di stato** 
</dt> <dd>

La modifica dello stato di rendering può essere un'operazione costosa, in particolare quando si modifica la trama. Per questo motivo, è importante ridurre al minimo quanto possibile il numero di modifiche di stato effettuate per frame. Inoltre, provare a ridurre al minimo le modifiche di vertex o index buffer.

> [!Note]  
> A partire da DirectX 8, il costo della modifica del buffer dei vertici non è più costoso come con le versioni precedenti, ma è comunque consigliabile evitare le modifiche al buffer dei vertici laddove possibile.

 

</dd> <dt>

<span id="Concurrency"></span><span id="concurrency"></span><span id="CONCURRENCY"></span>**Concorrenza**
</dt> <dd>

Se è possibile disporre per eseguire il rendering simultaneamente con altre elaborazioni, sarà possibile sfruttare appieno le prestazioni del sistema. Questo obiettivo può essere in conflitto con l'obiettivo di ridurre le modifiche apportate a RenderState. È necessario stabilire un equilibrio tra la suddivisione in batch per ridurre le modifiche di stato e il push dei dati al driver prima di ottenere la concorrenza. L'uso di più buffer dei vertici nello stile round robin può essere utile per la concorrenza.

</dd> <dt>

<span id="Texture_uploads_"></span><span id="texture_uploads_"></span><span id="TEXTURE_UPLOADS_"></span>**Caricamenti di trama** 
</dt> <dd>

Il caricamento di trame nel dispositivo consuma la larghezza di banda e causa una concorrenza della larghezza di banda con i dati dei vertici. Pertanto, è importante non superare la memoria di trama del commit, il che impone allo schema di memorizzazione nella cache di caricare quantità eccessive di trame ogni frame.

</dd> <dt>

<span id="Vertex_and_index_buffers_"></span><span id="vertex_and_index_buffers_"></span><span id="VERTEX_AND_INDEX_BUFFERS_"></span>**Buffer di Vertex e index** 
</dt> <dd>

È consigliabile usare sempre i buffer di Vertex e index, anziché i blocchi semplici della memoria allocata dell'applicazione. Come minimo, la semantica di blocco per i buffer dei vertici e degli indici può evitare un'operazione di copia ridondante. Con alcuni driver, il vertex buffer o index buffer può essere inserito in una quantità di memoria ottimale, ad esempio nella memoria video o AGP, per l'accesso da parte dell'hardware.

</dd> <dt>

<span id="State_macro_blocks_"></span><span id="state_macro_blocks_"></span><span id="STATE_MACRO_BLOCKS_"></span>**Blocchi macro di stato** 
</dt> <dd>

Questi sono stati introdotti in DirectX 7,0. Forniscono un meccanismo per la registrazione di una serie di modifiche di stato (incluse le modifiche di illuminazione, materiale e matrice) in una macro, che può quindi essere rieseguita da una singola chiamata. Ciò comporta due vantaggi:

-   Per ridurre l'overhead delle chiamate, è necessario effettuare una chiamata invece di molti.
-   Un driver compatibile può pre-analizzare e pre-compilare le modifiche dello stato, rendendolo molto più veloce da inviare all'hardware grafico.

Le modifiche di stato possono comunque essere costose, ma l'uso di macro di stato consente di ridurre almeno alcuni costi. Usare solo un singolo dispositivo Direct3D. Se è necessario eseguire il rendering in più destinazioni, usare SetRenderTarget. Se si sta creando un'applicazione a finestra con più finestre 3D, usare l'API CreateAdditionalSwapChain. Il runtime è ottimizzato per un singolo dispositivo ed esiste una notevole riduzione della velocità per l'uso di più dispositivi.

</dd> </dl> </dd> <dt>

<span id="Which_primitive_types__strips__fans__lists_and_so_on__should_I_use__"></span><span id="which_primitive_types__strips__fans__lists_and_so_on__should_i_use__"></span><span id="WHICH_PRIMITIVE_TYPES__STRIPS__FANS__LISTS_AND_SO_ON__SHOULD_I_USE__"></span>**Quali tipi primitivi (strisce, ventilatori, elenchi e così via) devono essere usati?** 
</dt> <dd>

Molte maglie rilevate nei vertici delle funzionalità dati reali condivise da più poligoni. Per ottimizzare le prestazioni, è consigliabile ridurre la duplicazione nei vertici trasformati e inviati attraverso il bus al dispositivo di rendering. È chiaro che l'uso di semplici elenchi di triangolo non consente di ottenere la condivisione dei vertici, rendendolo il metodo meno ottimale. La scelta tra l'utilizzo di strisce e ventilatori implica una specifica relazione di connettività tra poligoni e l'utilizzo di elenchi indicizzati. Il modo in cui i dati rientrano naturalmente in strip e ventilatori è la scelta più appropriata, dal momento che consentono di ridurre al minimo i dati inviati al driver. Tuttavia, la scomposizione delle mesh in strisce e ventilatori spesso comporta un numero elevato di parti separate, che implicano un numero elevato di chiamate DrawPrimitive. Per questo motivo, il metodo più efficiente consiste in genere nell'usare una singola chiamata DrawIndexedPrimitive con un elenco di triangolo. Un ulteriore vantaggio dell'uso di un elenco indicizzato è che è possibile ottenere un vantaggio anche quando i triangoli consecutivi condividono solo un singolo vertice. In breve, se i dati rientrano naturalmente in nastri o fan di grandi dimensioni, usare strisce o ventilatori; in caso contrario, usare elenchi indicizzati.

</dd> <dt>

<span id="How_do_you_determine_the_total_texture_memory_a_card_has__excluding_AGP_memory__"></span><span id="how_do_you_determine_the_total_texture_memory_a_card_has__excluding_agp_memory__"></span><span id="HOW_DO_YOU_DETERMINE_THE_TOTAL_TEXTURE_MEMORY_A_CARD_HAS__EXCLUDING_AGP_MEMORY__"></span>**Come è possibile determinare la memoria di trama totale di una scheda, esclusa la memoria AGP?** 
</dt> <dd>

[**IDirect3DDevice9:: GetAvailableTextureMem**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getavailabletexturemem) restituisce la memoria totale disponibile, incluso AGP. L'allocazione delle risorse in base a un presupposto della quantità di memoria video non è una buona idea. Ad esempio, cosa accade se la scheda viene eseguita con un'architettura di memoria unificata (UMA) o è in grado di comprimere le trame? Potrebbe essere disponibile più spazio del previsto. È necessario creare le risorse e verificare la presenza di errori di memoria insufficiente, quindi ridimensionare le trame. Ad esempio, è possibile rimuovere i primi livelli MIP delle trame.

</dd> <dt>

<span id="What_s_a_good_usage_pattern_for_vertex_buffers_if_I_m_generating_dynamic_data__"></span><span id="what_s_a_good_usage_pattern_for_vertex_buffers_if_i_m_generating_dynamic_data__"></span><span id="WHAT_S_A_GOOD_USAGE_PATTERN_FOR_VERTEX_BUFFERS_IF_I_M_GENERATING_DYNAMIC_DATA__"></span>**Qual è il modello di utilizzo corretto per i buffer dei vertici se si generano dati dinamici?** 
</dt> <dd>

1.  Creare un buffer vertex usando i \_ flag di utilizzo D3DUSAGE dinamici e D3DUSAGE \_ WRITEONLY e il \_ flag di pool predefinito D3DPOOL. (Specificare anche D3DUSAGE \_ SOFTWAREPROCESSING se si utilizza l'elaborazione dei vertici software.
2.  I = 0.
3.  Impostare lo stato (trame, renderstates e così via).
4.  Verificare che sia presente spazio nel buffer, ad esempio I + M <= N? (Dove M è il numero di nuovi vertici).
5.  In caso affermativo, bloccare VB con D3DLOCK \_ overwrite. Ciò indica a Direct3D e al driver di aggiungere i vertici e non verranno modificati quelli precedentemente in batch. Pertanto, se è in corso un'operazione DMA, non viene interrotta. Se no, vai a 11.
6.  Inserire i vertici M.
7.  Sbloccare.
8.  Chiamata \[ \] primitiva indicizzata. Per le primitive non indicizzate, usare I come parametro StartVertex. Per le primitive indicizzate, verificare che gli indici puntino alla porzione corretta del buffer dei vertici. per ottenere questo risultato, potrebbe essere più semplice usare il parametro BaseVertexIndex della chiamata SetIndices.
9.  I + = M.
10. GOTO 3.
11. OK. ora abbiamo esaurito lo spazio, quindi inizieremo con una nuova VB. Non si vuole usare lo stesso perché potrebbe essere in corso un'operazione DMA. Si comunica a questo a Direct3D e al driver bloccando la stessa VB con il \_ flag di eliminazione D3DLOCK. Ciò significa che è possibile assegnare un nuovo indicatore di misura perché ho finito con quello precedente e non mi interessa più del vecchio contenuto. "
12. I = 0.
13. GOTO 4 (o 6).

</dd> <dt>

<span id="Why_do_I_have_to_specify_more_information_in_the_D3DVERTEXELEMENT9_structure__"></span><span id="why_do_i_have_to_specify_more_information_in_the_d3dvertexelement9_structure__"></span><span id="WHY_DO_I_HAVE_TO_SPECIFY_MORE_INFORMATION_IN_THE_D3DVERTEXELEMENT9_STRUCTURE__"></span>**Perché è necessario specificare altre informazioni nella struttura D3DVERTEXELEMENT9?** 
</dt> <dd>

A partire da Direct3D 9, la dichiarazione del flusso di vertici non è più solo una matrice DWORD, ora è una matrice di strutture D3DVERTEXELEMENT9. Il runtime usa le informazioni aggiuntive sulla semantica e sull'utilizzo per associare il contenuto dei flussi di vertici ai registri/variabili di input di vertex shader. Per Direct3D 9, le dichiarazioni dei vertici sono separate da vertex shader, semplificando l'uso di shader con geometrie di formati diversi, perché il runtime associa solo i dati necessari per lo shader.

Le nuove dichiarazioni di vertice possono essere utilizzate con la pipeline della funzione fissa o con shader. Per la pipeline della funzione fixed, non è necessario chiamare SetVertexShader. Se tuttavia si desidera passare alla pipeline della funzione fissa e in precedenza è stato utilizzato un vertex shader, chiamare SetVertexShader (NULL). Al termine, sarà comunque necessario chiamare SetFVF per dichiarare il codice FVF.

Quando si usano vertex shader, chiamare SetVertexShader con l'oggetto vertex shader. Inoltre, chiamare SetFVF per impostare una dichiarazione del vertice. Questa operazione usa le informazioni implicite in FVF. SetVertexDeclaration può essere chiamato al posto di SetFVF perché supporta le dichiarazioni dei vertici che non possono essere espresse con un FVF.

</dd> </dl>

### <a name="d3dx-utility-library"></a>Libreria di utilità D3DX

<dl> <dt>

<span id="What_file_formats_are_supported_by_the_D3DX_image_file_loader_functions__"></span><span id="what_file_formats_are_supported_by_the_d3dx_image_file_loader_functions__"></span><span id="WHAT_FILE_FORMATS_ARE_SUPPORTED_BY_THE_D3DX_IMAGE_FILE_LOADER_FUNCTIONS__"></span>**Quali formati di file sono supportati dalle funzioni del caricatore di file di immagine D3DX?** 
</dt> <dd>

Le funzioni del caricatore di file di immagine D3DX supportano i file BMP, TGA, JPG, DIB, PPM e DDS.

</dd> <dt>

<span id="The_text_rendering_functions_in_D3DX_don_t_seem_to_work__what_am_I_doing_wrong__"></span><span id="the_text_rendering_functions_in_d3dx_don_t_seem_to_work__what_am_i_doing_wrong__"></span><span id="THE_TEXT_RENDERING_FUNCTIONS_IN_D3DX_DON_T_SEEM_TO_WORK__WHAT_AM_I_DOING_WRONG__"></span>**Le funzioni di rendering del testo in D3DX non sembrano funzionare, cosa si sta facendo male?** 
</dt> <dd>

Un errore comune quando si usano le funzioni ID3DXFont::D rawText è quello di specificare un componente alfa zero per il parametro color; risultato di testo completamente trasparente, ovvero invisibile. Per il testo completamente opaco, verificare che il componente alfa del parametro color sia completamente saturo (255).

</dd> <dt>

<span id="How_can_I_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="how_can_i_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="HOW_CAN_I_SAVE_THE_CONTENTS_OF_A_SURFACE_OR_TEXTURE_TO_A_FILE__"></span>**Come è possibile salvare il contenuto di una superficie o di una trama in un file?** 
</dt> <dd>

DirectX 8,1 SDK ha aggiunto due funzioni alla libreria D3DX in modo specifico per questo scopo: D3DXSaveSurfaceToFile () e D3DXSaveTextureToFile (). Queste funzioni supportano il salvataggio di un'immagine in un file in formato BMP o DDS. Nelle versioni precedenti sarà necessario bloccare la superficie e leggere i dati dell'immagine, quindi scriverli in un file bitmap. Per informazioni sulla scrittura di una funzione per archiviare le bitmap, vedere [archiviazione di un'immagine](/windows/desktop/gdi/storing-an-image).

In alternativa, è possibile usare GDI+ per salvare l'immagine in un'ampia gamma di formati, anche se questa operazione richiede la distribuzione di altri file di supporto con l'applicazione.

</dd> <dt>

<span id="How_can_I_make_use_of_the_High_Level_Shader_Language__HLSL__in_my_game__"></span><span id="how_can_i_make_use_of_the_high_level_shader_language__hlsl__in_my_game__"></span><span id="HOW_CAN_I_MAKE_USE_OF_THE_HIGH_LEVEL_SHADER_LANGUAGE__HLSL__IN_MY_GAME__"></span>**Come è possibile usare il linguaggio HLSL (High Level Shader Language) nel gioco?** 
</dt> <dd>

Sono disponibili tre modi per incorporare Microsoft High Level Shader Language (HLSL) nel motore di gioco:

-   Compilare l'origine shader in un assembly di ombreggiatura vertex o pixel (usando l'utilità della riga di comando fxc.exe) e usare D3DXAssembleShader () in fase di esecuzione. In questo modo anche un gioco DirectX 8 può sfruttare la potenza di HLSL.
-   Utilizzare D3DXCompileShader () per compilare l'origine dello shader in un flusso di token e in un formato di tabella costante. In fase di esecuzione caricare il flusso di token e la tabella costante e chiamare CreateVertexShader () o CreatePixelShader () sul dispositivo per creare gli shader.
-   Il modo più semplice per iniziare a usare è sfruttare il sistema D3DX Effects chiamando D3DXCreateEffectFromFile () o D3DXCreateEffectFromResource () con il file di effetti.

</dd> <dt>

<span id="What_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="what_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_NEW_SHADER_COMPILER_FLAG__"></span>**Qual è lo scopo del nuovo flag del compilatore shader?** 
</dt> <dd>

A partire da dicembre 2006 DirectX SDK, il nuovo compilatore HLSL sviluppato per Direct3D 10 è stato abilitato per gli obiettivi di Direct3D 9. Il nuovo compilatore non dispone del supporto per \_ le \_ destinazioni PS 1 x ed è ora il compilatore predefinito per tutti gli shader HLSL Direct3D. È possibile usare un flag per la compatibilità con le versioni precedenti per forzare la \_ compilazione delle destinazioni PS 1 \_ x come \_ destinazioni PS 2 \_ 0.

Le applicazioni che vogliono usare il compilatore legacy possono continuare a farlo fornendo un flag in fase di esecuzione (vedere [**flag del compilatore**](/windows/desktop/direct3d9/d3dxshader-flags)) o specificando un'opzione quando si usa fxc.

</dd> <dt>

<span id="What_is_the_correct_way_to_get_shaders_from_an_Effect__"></span><span id="what_is_the_correct_way_to_get_shaders_from_an_effect__"></span><span id="WHAT_IS_THE_CORRECT_WAY_TO_GET_SHADERS_FROM_AN_EFFECT__"></span>**Qual è il modo corretto per ottenere gli shader da un effetto?** 
</dt> <dd>

Usare D3DXCreateEffect per creare un ID3DXEffect e quindi usare GetPassDesc per recuperare un D3DXPASS \_ desc. Questa struttura contiene puntatori a Vertex e pixel shader.

Non usare ID3DXEffectCompiler:: GetPassDesc. Gli handle Vertex e pixel shader restituiti da questo metodo sono NULL.

</dd> <dt>

<span id="What_is_the_HLSL_noise___intrinsic_for__"></span><span id="what_is_the_hlsl_noise___intrinsic_for__"></span><span id="WHAT_IS_THE_HLSL_NOISE___INTRINSIC_FOR__"></span>**Qual è la funzione intrinseca HLSL Noise () per?** 
</dt> <dd>

La funzione intrinseca Noise genera il rumore Perlin come definito da Ken Perlin. Attualmente, la funzione HLSL può essere usata solo per riempire le trame in shader di trama, perché il metodo h/w corrente non supporta il metodo in modo nativo. Gli shader con trama vengono usati in ID insieme ad con le \* funzioni di trama D3DXFill (), che sono funzioni di supporto utili per generare trame definite in modo procedurale durante il tempo di caricamento.

</dd> <dt>

<span id="How_do_I_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="how_do_i_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="HOW_DO_I_DETECT_WHETHER_TO_USE_PIXEL_SHADER_MODEL_2.0_OR_2.A__"></span>**Ricerca per categorie rilevare se utilizzare pixel shader modello 2,0 o 2. a?** 
</dt> <dd>

È possibile usare le funzioni D3DXGetPixelShaderProfile () e D3DXGetPixelShaderProfile () che restituiscono una stringa che determina quale profilo HLSL è più adatto al dispositivo in esecuzione.

</dd> <dt>

<span id="How_do_I_access_the_Parameters_in_my_Precompiled_Effects_Shaders__"></span><span id="how_do_i_access_the_parameters_in_my_precompiled_effects_shaders__"></span><span id="HOW_DO_I_ACCESS_THE_PARAMETERS_IN_MY_PRECOMPILED_EFFECTS_SHADERS__"></span>**Ricerca per categorie accedere ai parametri negli shader degli effetti precompilati?** 
</dt> <dd>

Tramite l'interfaccia ID3DXConstantTable utilizzata per accedere alla tabella Constant. Questa tabella contiene le variabili utilizzate dagli shader e dagli effetti dei linguaggi di alto livello.

</dd> <dt>

<span id="Is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="IS_THERE_A_WAY_TO_ADD_USER_DATA_TO_AN_EFFECT_OR_OTHER_RESOURCE__"></span>**Esiste un modo per aggiungere dati utente a un effetto o ad altre risorse?** 
</dt> <dd>

Sì, per impostare i dati privati viene chiamato SetPrivateData (pReal è l'oggetto trama D3D, pSpoof è l'oggetto trama di cui è stato eseguito il wrapper).

``` syntax
hr = pReal->SetPrivateData(IID_Spoof, &pSpoof, 
            sizeof(IDirect3DResource9*), 0)));
```

Per cercare il puntatore di cui è stato eseguito il wrapper:

``` syntax
    IDirect3DResource9* pSpoof;
    DWORD dwSize = sizeof(pSpoof);
    hr = pReal->GetPrivateData(IID_Spoof, (void*) &pSpoof, &dwSize);
```

</dd> <dt>

<span id="Why_does_rendering_of_an_ID3DXMesh_object_slow_down_significantly_after_I_define_subsets__"></span><span id="why_does_rendering_of_an_id3dxmesh_object_slow_down_significantly_after_i_define_subsets__"></span><span id="WHY_DOES_RENDERING_OF_AN_ID3DXMESH_OBJECT_SLOW_DOWN_SIGNIFICANTLY_AFTER_I_DEFINE_SUBSETS__"></span>**Perché il rendering di un oggetto ID3DXMesh rallenta significativamente dopo aver definito I subset?** 
</dt> <dd>

È probabile che la rete non sia stata ottimizzata dopo aver definito gli attributi del viso. Se si specificano gli attributi e quindi si chiama ID3DXMesh::D rawSubset (), questo metodo deve eseguire una ricerca della mesh per tutti i visi contenenti gli attributi richiesti. Inoltre, è probabile che i visi sottoposti a rendering si trovino in un modello di accesso casuale, in modo da non utilizzare la cache vertex. Dopo aver definito gli attributi viso per i subset, chiamare i metodi ID3DXMesh:: Optimize o ID3DXMesh:: OptimizeInPlace e specificando un metodo di ottimizzazione di D3DXMESHOPT \_ ATTRSORT o più forte. Si noti che per ottenere prestazioni ottimali, è consigliabile ottimizzare con il \_ flag VERTEXCACHE di D3DXMESHOPT, che consente anche di riordinare i vertici per un utilizzo ottimale della cache dei vertici. La matrice adiacenza generata per una mesh D3DX include tre voci per ogni volto, ma alcuni visi potrebbero non avere visi adiacenti su tutti e tre i bordi. Come viene codificato? Le voci in cui non sono presenti visi adiacenti vengono codificate come 0xFFFFFFFF.

</dd> <dt>

<span id="I_ve_heard_a_lot_about_Pre-computed_Radiance_Transfer__PRT___where_can_I_learn_more__"></span><span id="i_ve_heard_a_lot_about_pre-computed_radiance_transfer__prt___where_can_i_learn_more__"></span><span id="I_VE_HEARD_A_LOT_ABOUT_PRE-COMPUTED_RADIANCE_TRANSFER__PRT___WHERE_CAN_I_LEARN_MORE__"></span>**Ho sentito parlare molto del trasferimento di luminosità pre-calcolato (PRT), dove posso ottenere altre informazioni?** 
</dt> <dd>

PRT è una nuova funzionalità di D3DX aggiunta nell'aggiornamento dell'SDK per l'estate 2003. Consente il rendering di scenari di illuminazione complessi, ad esempio llumination globale, ombreggiatura soft e dispersione della superficie secondaria in tempo reale. L'SDK contiene documentazione ed esempi relativi all'integrazione della tecnologia nel gioco. Gli esempi di esempio PRT demo e LocalDeformablePRT illustrano come usare il simulatore per gli scenari di illuminazione per vertice e per pixel rispettivamente. Altre informazioni su questo e altri argomenti sono disponibili anche nella pagina Web di Peter Pike Sloan.

</dd> <dt>

<span id="How_can_I_render_to_a_texture_and_make_use_of_Anti_Aliasing__"></span><span id="how_can_i_render_to_a_texture_and_make_use_of_anti_aliasing__"></span><span id="HOW_CAN_I_RENDER_TO_A_TEXTURE_AND_MAKE_USE_OF_ANTI_ALIASING__"></span>**Come è possibile eseguire il rendering in una trama e usare l'anti-aliasing?** 
</dt> <dd>

Creare una destinazione di rendering multicampionata usando Direct3DDevice9:: CreateRenderTarget. Dopo aver eseguito il rendering della scena nella destinazione di rendering, StretchRect da tale destinazione a una trama di destinazione di rendering. Se si apportano modifiche al textre di Offscreen (ad esempio sfocatura o Bloom), ricopiarlo nel buffer nascosto prima di presentare ().

</dd> </dl>

## <a name="directsound-questions"></a>Domande DirectSound

<dl> <dt>

<span id="Why_do_I_get_a_burst_of_static_when_my_application_starts_up__I_notice_this_problem_with_other_applications_too._"></span><span id="why_do_i_get_a_burst_of_static_when_my_application_starts_up__i_notice_this_problem_with_other_applications_too._"></span><span id="WHY_DO_I_GET_A_BURST_OF_STATIC_WHEN_MY_APPLICATION_STARTS_UP__I_NOTICE_THIS_PROBLEM_WITH_OTHER_APPLICATIONS_TOO._"></span>**Perché si ottiene un impeto di static quando viene avviata l'applicazione? Ho notato questo problema anche con altre applicazioni.** 
</dt> <dd>

È probabile che sia stato installato il runtime DirectX di debug. La versione di debug del runtime riempie i buffer con static per consentire agli sviluppatori di rilevare i bug con buffer non inizializzati. Non è possibile garantire il contenuto di un buffer DirectSound dopo la creazione. in particolare, non è possibile presupporre che un buffer con sia azzerato.

</dd> <dt>

<span id="Why_I_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="why_i_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="WHY_I_AM_EXPERIENCING_A_DELAY_IN_BETWEEN_CHANGING_AN_EFFECTS_PARAMETERS_AND_HEARING_THE_RESULTS__"></span>**Perché si verifica un ritardo tra la modifica di un parametro degli effetti e l'audizione dei risultati?** 
</dt> <dd>

Le modifiche ai parametri effetti non avvengono sempre immediatamente in DirectX 8. Per migliorare l'efficienza, DirectSound elabora 100 millisecondi di dati audio in un buffer, a partire dal cursore di riproduzione, prima che il buffer venga riprodotto. Questa pre-elaborazione viene eseguita dopo tutte le chiamate seguenti:

``` syntax
IDirectSoundBuffer8::SetCurrentPosition
IDirectSoundBuffer8::SetFX
IDirectSoundBuffer8::Stop
IDirectSoundBuffer8::Unlock
```

A partire da DirectX 9, un nuovo algoritmo di elaborazione FX che elabora gli effetti JIT risolve questo problema e ha ridotto la latenza. L'algoritmo è stato aggiunto alla chiamata IDirectSoundBuffer8::P Lay (), insieme a un thread aggiuntivo che elabora gli effetti immediatamente prima del cursore di scrittura. Quindi, è possibile impostare i parametri in qualsiasi momento e funzionano come previsto. Si noti, tuttavia, che in un buffer di riproduzione si verifica un piccolo ritardo, in genere 100 ms, prima che venga rilevata la modifica del parametro, perché l'audio tra i cursori di riproduzione e scrittura (e un po' più di riempimento) è già stato elaborato in quel momento.

</dd> <dt>

<span id="How_do_I_detect_if_DSound_is_installed__"></span><span id="how_do_i_detect_if_dsound_is_installed__"></span><span id="HOW_DO_I_DETECT_IF_DSOUND_IS_INSTALLED__"></span>**Ricerca per categorie rilevare se DSound è installato?** 
</dt> <dd>

Se non è necessario usare DirectSoundEnumerate () per elencare i dispositivi DSound disponibili, non collegare l'applicazione a DSOUND. lib e usarla invece tramite il sistema com CoCreateInstance (CLSID \_ DirectSound...) e quindi inizializzare l'oggetto DSOUND usando Initialize (null). Se è necessario usare DirectSoundEnumerate (), è possibile caricare dinamicamente dsound.dll usando LoadLibrary ("dsound.dll"); e accedono ai metodi usando GetProcAddress ("DirectSoundEnumerateA/W") e GetProcAddress ("DirectSoundCreateA/W") e così via.

</dd> <dt>

<span id="How_do_I_create_multichannel_audio_with_WAVEFORMATEXTENSIBLE__"></span><span id="how_do_i_create_multichannel_audio_with_waveformatextensible__"></span><span id="HOW_DO_I_CREATE_MULTICHANNEL_AUDIO_WITH_WAVEFORMATEXTENSIBLE__"></span>**Ricerca per categorie creare audio multicanale con WAVEFORMATEXTENSIBLE?** 
</dt> <dd>

Se non si riesce a trovare una risposta alla domanda nei file della Guida DirectSound, è disponibile un articolo con altre informazioni su file di dati audio e WAVE a più canali.

</dd> <dt>

<span id="How_can_I_use_the_DirectSound_Voice_Manager_with_property_sets_like_EAX__"></span><span id="how_can_i_use_the_directsound_voice_manager_with_property_sets_like_eax__"></span><span id="HOW_CAN_I_USE_THE_DIRECTSOUND_VOICE_MANAGER_WITH_PROPERTY_SETS_LIKE_EAX__"></span>**In che modo è possibile utilizzare la funzionalità DirectSound Voice Manager con set di proprietà come EAX?** 
</dt> <dd>

In DirectSound 9,0 quando si duplica un buffer è ora possibile ottenere l'interfaccia IDirectSoundBuffer8 sul buffer duplicato, che consente di accedere al metodo AcquireResources. Ciò consentirà di associare un buffer al \_ flag LOCDEFER di DSBCAPS con una risorsa hardware. È quindi possibile impostare i parametri EAX in questo buffer prima di chiamare Play ().

</dd> <dt>

<span id="I_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._How_can_I_get_more_accurate_information__"></span><span id="i_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._how_can_i_get_more_accurate_information__"></span><span id="I_AM_HAVING_PROBLEMS_WITH_UNRELIABLE_BEHAVIOR_WHEN_USING_CURSOR_POSITION_NOTIFICATIONS._HOW_CAN_I_GET_MORE_ACCURATE_INFORMATION__"></span>**Si verificano problemi con un comportamento non affidabile quando si utilizzano le notifiche di posizione del cursore. Come è possibile ottenere informazioni più accurate?** 
</dt> <dd>

Le varie versioni di DirectSound, lo stack audio principale di Windows e i driver audio che rendono le notifiche di posizioni del cursore inaffidabili. A meno che non si abbia la destinazione di una configurazione HW/SW nota in cui si è certi che le notifiche siano correttamente corrette, evitare le notifiche di posizione del cursore. Per il rilevamento della posizione GetCurrentPosition () è una tecnica più sicura.

</dd> <dt>

<span id="I_am_suffering_from_performance_degradation_when_using_GetCurrentPosition__._What_can_I_do_to_improve_performance__"></span><span id="i_am_suffering_from_performance_degradation_when_using_getcurrentposition__._what_can_i_do_to_improve_performance__"></span><span id="I_AM_SUFFERING_FROM_PERFORMANCE_DEGRADATION_WHEN_USING_GETCURRENTPOSITION__._WHAT_CAN_I_DO_TO_IMPROVE_PERFORMANCE__"></span>**Si è verificato un calo delle prestazioni quando si usa GetCurrentPosition (). Quali operazioni è possibile eseguire per migliorare le prestazioni?** 
</dt> <dd>

Ogni chiamata a GetCurrentPosition () su ogni buffer causa una chiamata di sistema e le chiamate di sistema dovrebbero essere ridotte al minimo perché costituiscono un componente di grandi dimensioni del footprint della CPU di DSound. In NT (Win2K e XP) i cursori nei buffer SW (e i buffer HW in alcuni dispositivi) si spostano in incrementi di 10 ms, quindi la chiamata a GetCurrentPosition () ogni 10 ms è ideale. La chiamata più spesso di ogni 5 MS provocherà una riduzione delle prestazioni.

</dd> <dt>

<span id="My_DirectSound_application_is_taking_up_too_much_CPU_time_or_is_performing_slowly._Is_there_anything_I_can_do_to_optimize_my_code__"></span><span id="my_directsound_application_is_taking_up_too_much_cpu_time_or_is_performing_slowly._is_there_anything_i_can_do_to_optimize_my_code__"></span><span id="MY_DIRECTSOUND_APPLICATION_IS_TAKING_UP_TOO_MUCH_CPU_TIME_OR_IS_PERFORMING_SLOWLY._IS_THERE_ANYTHING_I_CAN_DO_TO_OPTIMIZE_MY_CODE__"></span>**L'applicazione DirectSound sta occupando troppo tempo della CPU o sta eseguendo lentamente. C'è qualcosa che posso fare per ottimizzare il mio codice?** 
</dt> <dd>

Per migliorare le prestazioni del codice audio, è possibile eseguire diverse operazioni:

-   Non chiamare GetCurrentPosition troppo spesso. Ogni chiamata a GetCurrentPosition () su ogni buffer causa una chiamata di sistema e le chiamate di sistema dovrebbero essere ridotte al minimo perché costituiscono un componente di grandi dimensioni del footprint della CPU di DSound. In NT (Win2K e XP) i cursori nei buffer SW (e i buffer HW in alcuni dispositivi) si spostano in incrementi di 10 ms, quindi la chiamata a GetCurrentPosition () ogni 10 ms è ideale. La chiamata più spesso di ogni 5 MS provocherà una riduzione delle prestazioni.
-   Usare una frequenza dei fotogrammi separata e inferiore per l'audio. Attualmente molti giochi di Windows possono superare 100 frame al secondo e non è necessario nella maggior parte dei casi aggiornare i parametri audio 3D con la stessa frequenza dei fotogrammi. L'elaborazione dell'audio ogni secondo o terzo frame grafica, o ogni 30ms, può ridurre il numero di chiamate audio in modo significativo nell'intera applicazione senza ridurre la qualità dell'audio.
-   Usare DS3D \_ posticipato per oggetti 3D. La maggior parte delle schede audio risponde immediatamente alle modifiche dei parametri e in un singolo frame può cambiare molto, soprattutto se si modifica la posizione o l'orientamento del listener. In questo modo la scheda audio/CPU esegue molti calcoli non necessari, quindi un'altra ottimizzazione rapida e universale consiste nel rinviare alcune modifiche dei parametri ed eseguirne il commit alla fine del frame.

    oppure utilizzare almeno SetAllParameters anziché le singole chiamate Set3DParamX sui buffer.

    Analogamente, è consigliabile usare almeno le chiamate SetAllParamenters sui buffer 3D anziché le singole chiamate Set3DParamX. È sufficiente provare a ridurre al minimo le chiamate di sistema, laddove possibile.

-   Non effettuare chiamate ridondanti; archiviare e ordinare un elenco di chiamate di riproduzione. Spesso, in un frame di aggiornamento audio, sono disponibili 2 richieste per riprodurre nuovi suoni. Se le richieste vengono elaborate all'arrivo, il primo nuovo suono può essere avviato e quindi sostituito immediatamente il secondo suono richiesto. Ciò comporta calcoli ridondanti, una chiamata di riproduzione non necessaria e una chiamata di arresto non necessaria. È preferibile archiviare un elenco di richieste per la riproduzione di nuovi suoni, in modo che l'elenco possa essere ordinato e solo le voci che dovrebbero iniziare a giocare, siano effettivamente riprodotte.

    Inoltre, è consigliabile archiviare le copie locali dei parametri 3D e EAX per ogni origine audio. Se viene effettuata una richiesta per impostare un parametro su un valore specifico, è possibile verificare se il valore è effettivamente diverso dall'ultimo set di valori. In caso contrario, non è necessario eseguire la chiamata.

    Sebbene il driver della scheda audio rilevi probabilmente questo scenario e non esegua di nuovo il calcolo (stesso), la chiamata audio dovrà raggiungere il driver audio (tramite una transizione dell'anello) ed è già un'operazione lenta.

</dd> <dt>

<span id="When_I_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._What_s_the_best_way_to_stream_a_buffer__"></span><span id="when_i_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._what_s_the_best_way_to_stream_a_buffer__"></span><span id="WHEN_I_STREAM_A_BUFFER_IT_TENDS_TO_GLITCH_AND_PERFORM_POORLY._WHAT_S_THE_BEST_WAY_TO_STREAM_A_BUFFER__"></span>**Quando si esegue il flusso di un buffer, il problema si verifica in modo anomalo. Qual è il modo migliore per eseguire lo streaming di un buffer?** 
</dt> <dd>

Quando si esegue lo streaming di audio in un buffer sono disponibili due algoritmi di base: After-Write-Cursor (AWC) e before-Play-Cursor (BPC). AWC riduce al minimo la latenza a scapito della glitching, mentre BPC è l'opposto. Poiché in genere non sono presenti modifiche interattive al suono trasmesso, questo tipo di latenza rappresenta raramente un problema per i giochi e applicazioni simili, quindi la funzione BPC è l'algoritmo più appropriato. In AWC ogni volta che il thread di streaming esegue l'operazione "top up" dei dati nei buffer di ciclo fino a N ms oltre i cursori di scrittura, in genere N = 40, per consentire l'instabilità della pianificazione di Windows. In BPC è sempre possibile scrivere tutti i dati nei buffer, inserendoli fino ai cursori di riproduzione (o probabilmente 32 byte prima di consentire ai driver che segnalano erroneamente lo stato di avanzamento del cursore).

Usare la funzione BPC per Mimimize le anomalie e usare i buffer 100 ms o una dimensione maggiore anche se i giochi non inconvenienti nell'hardware di test, si verificherà un problema in alcuni computer.

</dd> <dt>

<span id="I_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_Play___call_takes_a_long_time._What_should_I_do__"></span><span id="i_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_play___call_takes_a_long_time._what_should_i_do__"></span><span id="I_AM_PLAYING_THE_SAME_SOUNDS_OVER_AND_OVER_VERY_OFTEN_AND_VERY_QUICKLY_AND_SOMETIMES_THEY_DON_T_PLAY_PROPERLY__OR_THE_PLAY___CALL_TAKES_A_LONG_TIME._WHAT_SHOULD_I_DO__"></span>**Sto suonando gli stessi suoni spesso e molto rapidamente e talvolta non funzionano correttamente oppure la chiamata Play () richiede molto tempo. Cosa dovrei fare?** 
</dt> <dd>

La latenza di avvio (diversa dalla latenza di streaming indicata in precedenza) può costituire un problema nel caso di hardware (la chiamata di Play () richiede molto tempo a volte su determinate schede audio). Se si vuole ridurre questa latenza, per i suoni di contrazione (sparatorie, orme e così via), un trucco utile consiste nel lasciare che i buffer siano sempre in loop e in gioco. Quando è necessario riprodurre un suono contrazione, scegliere un buffer libero, vedere dove è il cursore di scrittura e inserire il suono nel buffer oltre il cursore di scrittura. Alcuni schede hanno esito negativo QuerySupport per le proprietà posticipate che sono a conoscenza del supporto. Esiste una soluzione alternativa? È possibile QuerySupport solo per le versioni non posticipate delle proprietà e usare comunque le impostazioni posticipate. I driver della scheda audio più recenti possono anche risolvere questo problema.

</dd> <dt>

<span id="How_do_I_encode_WAV_files_into_WMA__"></span><span id="how_do_i_encode_wav_files_into_wma__"></span><span id="HOW_DO_I_ENCODE_WAV_FILES_INTO_WMA__"></span>**Ricerca per categorie codificare i file WAV in WMA?** 
</dt> <dd>

Vedere la documentazione di Windows Media Encoder in: Windows Media Encoder 9 Series.

</dd> <dt>

<span id="How_do_I_decode_MP3_files_with_DirectSound__"></span><span id="how_do_i_decode_mp3_files_with_directsound__"></span><span id="HOW_DO_I_DECODE_MP3_FILES_WITH_DIRECTSOUND__"></span>**Ricerca per categorie decodificare i file MP3 con DirectSound?** 
</dt> <dd>

DirectSound non supporta in modo nativo la decodifica MP3. È possibile decodificare i file in anticipo (usando un codec ACM di un filtro DirectShow), altrimenti è sufficiente usare DirectShow, che può eseguire la decodifica automaticamente. è quindi possibile copiare i dati audio PCM risultanti nei buffer DirectSound.

</dd> </dl>

## <a name="directx-extensions-for-alias-maya"></a>Estensioni DirectX per Alias Maya

<dl> <dt>

<span id="Why_aren_t_my_NURBS_showing_up__"></span><span id="why_aren_t_my_nurbs_showing_up__"></span><span id="WHY_AREN_T_MY_NURBS_SHOWING_UP__"></span>**Perché non viene visualizzata la NURBS?** 
</dt> <dd>

NURBS non è supportato. È possibile convertirli in mesh poligonali.

</dd> <dt>

<span id="Why_aren_t_my_SUBDs_showing_up_"></span><span id="why_aren_t_my_subds_showing_up_"></span><span id="WHY_AREN_T_MY_SUBDS_SHOWING_UP_"></span>**Perché non vengono visualizzati i SUBDs?**
</dt> <dd>

SUBDs non sono supportati. È possibile convertirli in mesh poligonali.

</dd> <dt>

<span id="Why_does_my_animation_in_the_X_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="why_does_my_animation_in_the_x_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="WHY_DOES_MY_ANIMATION_IN_THE_X_FILE_LOOK_DIFFERENT_THAN_THE_ANIMATION_IN_THE_PREVIEW_WINDOW__"></span>**Perché l'animazione nel file X ha un aspetto diverso dall'animazione nella finestra di anteprima?** 
</dt> <dd>

La finestra di anteprima non sta aggiungendo un'animazione nel senso più rigoroso della situazione. Non sta eseguendo l'animazione ma sta eseguendo la sincronizzazione allo stato più recente della scena Maya. Quando l'animazione viene esportata, le matrici a ogni trasformazione sono decomposte nei componenti di scala, rotazione (Quaternion) e traduzione (spesso denominati SRTs). SRTs sono più auspicabili delle matrici perché interpolano bene, forniscono una forma più compatta dei dati e possono essere compressi in modo indipendente. Non tutte le matrici possono suddividere in SRTs. Se non è possibile scomporre, il SRTs risultante sarà sconosciuto, quindi potrebbero essere rilevati piccoli errori nell'animazione. Le due funzionalità di Maya che più spesso provocano problemi durante la scomposizione sono le cesoie e le rotazioni fuori centro o le scale. Se si riscontra questo problema, poiché si utilizzano le rotazioni o le scale fuori centro, è consigliabile aggiungere ulteriori trasformazioni aumentando il livello di gerarchia.

Dove D3DX Animation supporta SRTs, l'aspetto è simile al seguente:

``` syntax
[S]x[R]x[T]
```

Le matrici di Maya sono molto più complesse e richiedono una quantità significativa di processi aggiuntivi, che hanno un aspetto simile al seguente:

``` syntax
[SpInv]x[S]x[Sh]x[Sp]x[St]x[RpInv]x[Ro]x[R]x[Rp]x[Rt]x[T]
```

</dd> <dt>

<span id="I_skinned_my_mesh_with_RigidSkin_but_the_mesh__or_portion__isn_t_moving._Why__"></span><span id="i_skinned_my_mesh_with_rigidskin_but_the_mesh__or_portion__isn_t_moving._why__"></span><span id="I_SKINNED_MY_MESH_WITH_RIGIDSKIN_BUT_THE_MESH__OR_PORTION__ISN_T_MOVING._WHY__"></span>**Ho scuoiato la mesh con RigidSkin, ma la rete (o parte) non è in fase di trasferimento. Perché?** 
</dt> <dd>

Al momento non sono supportate le interfacce rigide di Maya. Usare Smooth Skin.

</dd> <dt>

<span id="Where_has_all_of_my_IK_gone_in_the_X-file__"></span><span id="where_has_all_of_my_ik_gone_in_the_x-file__"></span><span id="WHERE_HAS_ALL_OF_MY_IK_GONE_IN_THE_X-FILE__"></span>**Dove tutto il mio IK è andato nel file X?** 
</dt> <dd>

I file X non supportano IK. Al contrario, le soluzioni IK vengono cotte nei frame archiviati nel file X.

</dd> <dt>

<span id="Why_do_none_of_my_materials_colors_show_up_except_DirectXShaders__"></span><span id="why_do_none_of_my_materials_colors_show_up_except_directxshaders__"></span><span id="WHY_DO_NONE_OF_MY_MATERIALS_COLORS_SHOW_UP_EXCEPT_DIRECTXSHADERS__"></span>**Perché nessuno dei miei colori materiali viene visualizzato ad eccezione di DirectXShaders?** 
</dt> <dd>

Le estensioni DirectX per Maya attualmente supportano solo materiali DirectXShader per l'anteprima e l'esportazione. In una versione futura potrebbero essere supportati altri materiali.

</dd> </dl>

## <a name="xinput-questions"></a>Domande su XInput

<dl> <dt>

<span id="Can_I_use_DirectInput_to_read_the_triggers__"></span><span id="can_i_use_directinput_to_read_the_triggers__"></span><span id="CAN_I_USE_DIRECTINPUT_TO_READ_THE_TRIGGERS__"></span>**È possibile utilizzare DirectInput per leggere i trigger?** 
</dt> <dd>

Sì, ma agiscono come lo stesso asse. Quindi, non è possibile leggere i trigger in modo indipendente con DirectInput. Utilizzando XInput, i trigger restituiscono valori distinti.

Per altre informazioni sui motivi per cui DirectInput interpreta i trigger come un asse, vedere [uso del controller Xbox 360 con DirectInput](/windows/desktop/xinput/xinput-and-directinput).

</dd> <dt>

<span id="How_many_controllers_does_XInput_support__"></span><span id="how_many_controllers_does_xinput_support__"></span><span id="HOW_MANY_CONTROLLERS_DOES_XINPUT_SUPPORT__"></span>**Quanti controller supportano XInput?** 
</dt> <dd>

XInput supporta 4 controller collegati alla volta.

</dd> <dt>

<span id="Does_XInput_support_non-common_controllers__"></span><span id="does_xinput_support_non-common_controllers__"></span><span id="DOES_XINPUT_SUPPORT_NON-COMMON_CONTROLLERS__"></span>**XInput supporta i controller non comuni?** 
</dt> <dd>

No.

</dd> <dt>

<span id="Are_common_controllers_available_through_DirectInput__"></span><span id="are_common_controllers_available_through_directinput__"></span><span id="ARE_COMMON_CONTROLLERS_AVAILABLE_THROUGH_DIRECTINPUT__"></span>**I controller comuni sono disponibili tramite DirectInput?** 
</dt> <dd>

Sì, è possibile accedere a controller comuni tramite DirectInput.

</dd> <dt>

<span id="How_do_I_get_force_feedback_on_the_common_controllers__"></span><span id="how_do_i_get_force_feedback_on_the_common_controllers__"></span><span id="HOW_DO_I_GET_FORCE_FEEDBACK_ON_THE_COMMON_CONTROLLERS__"></span>**Ricerca per categorie ottenere feedback forzato sui controller comuni?** 
</dt> <dd>

Usare la funzione [**XInputSetState**](/windows/desktop/api/xinput/nf-xinput-xinputsetstate) .

</dd> <dt>

<span id="Why_does_my_default_audio_device_change__"></span><span id="why_does_my_default_audio_device_change__"></span><span id="WHY_DOES_MY_DEFAULT_AUDIO_DEVICE_CHANGE__"></span>**Perché il dispositivo audio predefinito cambia?** 
</dt> <dd>

Quando si connette l'auricolare, l'auricolare del controller funge da dispositivo audio USB standard, quindi, quando è connesso, Windows cambia automaticamente per usare questo dispositivo audio USB come valore predefinito. Poiché l'utente probabilmente non desidera che tutti i file audio passino attraverso l'auricolare, sarà necessario modificarlo manualmente sull'impostazione originale.

</dd> <dt>

<span id="How_do_I_control_the_lights_on_the_controller__"></span><span id="how_do_i_control_the_lights_on_the_controller__"></span><span id="HOW_DO_I_CONTROL_THE_LIGHTS_ON_THE_CONTROLLER__"></span>**Ricerca per categorie controllare le luci del controller?** 
</dt> <dd>

Le spie sul controller sono predeterminate dal sistema operativo e non possono essere modificate.

</dd> <dt>

<span id="How_do_I_access_the_Xbox_360_button_in_my_applications__"></span><span id="how_do_i_access_the_xbox_360_button_in_my_applications__"></span><span id="HOW_DO_I_ACCESS_THE_XBOX_360_BUTTON_IN_MY_APPLICATIONS__"></span>**Ricerca per categorie accedere al pulsante Xbox 360 in applicazioni personali?** 
</dt> <dd>

Questo pulsante è riservato per un uso futuro.

</dd> <dt>

<span id="Where_do_I_get_drivers__"></span><span id="where_do_i_get_drivers__"></span><span id="WHERE_DO_I_GET_DRIVERS__"></span>**Dove si ottengono i driver?** 
</dt> <dd>

I driver saranno disponibili tramite Windows Update.

</dd> <dt>

<span id="How_is_controller_ID_determined__"></span><span id="how_is_controller_id_determined__"></span><span id="HOW_IS_CONTROLLER_ID_DETERMINED__"></span>**Come viene determinato l'ID del controller?** 
</dt> <dd>

All'avvio di XInput, l'ID viene determinato in modo non deterministico dal motore XInput e dai controller collegati. Se i controller sono collegati mentre un'applicazione XInput è in esecuzione, il sistema assegnerà il nuovo controller al numero più basso disponibile. Se un controller è disconnesso, il relativo numero verrà nuovamente reso disponibile.

</dd> <dt>

<span id="How_do_I_get_the_audio_devices_for_the_controller__"></span><span id="how_do_i_get_the_audio_devices_for_the_controller__"></span><span id="HOW_DO_I_GET_THE_AUDIO_DEVICES_FOR_THE_CONTROLLER__"></span>**Ricerca per categorie ottenere i dispositivi audio per il controller?** 
</dt> <dd>

Usare la funzione [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/xinput/nf-xinput-xinputgetdsoundaudiodeviceguids) . Per informazioni dettagliate, vedere l'esempio AudioController.

</dd> <dt>

<span id="What_should_I_do_when_a_controller_is_unplugged__"></span><span id="what_should_i_do_when_a_controller_is_unplugged__"></span><span id="WHAT_SHOULD_I_DO_WHEN_A_CONTROLLER_IS_UNPLUGGED__"></span>**Cosa devo fare quando un controller viene scollegato?** 
</dt> <dd>

Se il controller è stato usato da un lettore, è necessario sospendere il gioco finché il controller non viene riconnesso e il lettore preme un pulsante per segnalare che è pronto per l'interruzione.

</dd> </dl>

 

 