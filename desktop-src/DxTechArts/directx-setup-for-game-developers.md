---
title: Installazione di DirectX per sviluppatori di giochi
description: Questo articolo ha lo scopo di risolvere alcune domande comuni sul runtime DirectX e sull'uso di DirectSetup per installare DirectX.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0509084232f1dcfe63a7d956516aa723f8cd724b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477287"
---
# <a name="directx-installation-for-game-developers"></a>Installazione di DirectX per sviluppatori di giochi

Questo articolo ha lo scopo di risolvere alcune domande comuni sul runtime DirectX e sull'uso di DirectSetup per installare DirectX.

-   [DirectX Runtime](#directx-runtime)
-   [Numero di versione di DirectX](#directx-version-number)
-   [Librerie DirectX](#directx-libraries)
-   [Installazione di DirectX da parte del programma di installazione del gioco](#installation-of-directx-by-the-games-installer)
-   [Pacchetti di installazione di piccole dimensioni](#small-installation-packages)
-   [Distribuzione interna del runtime DirectX di debug](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> DirectX SDK legacy è alla fine del ciclo di vita, ma è ancora disponibile per supportare giochi, esercitazioni e progetti precedenti. I nuovi progetti non devono usarlo. L'uso di DirectX SDK legacy richiede l'uso di DirectSetup deprecato per componenti come D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 e XACT. Per altri dettagli sullo stato corrente di DirectX SDK, vedere Where is the DirectX SDK? (Dove si trova [DirectX SDK?)](../directx-sdk--august-2009-.md)e il post di blog Not So Direct Setup (Configurazione non [così diretta).](https://walbourn.github.io/not-so-direct-setup/)

## <a name="directx-runtime"></a>DirectX Runtime

Il runtime DirectX è costituito da componenti di base e componenti facoltativi.

I componenti principali, ad esempio Direct3D e DirectInput, sono considerati parte del sistema operativo. I componenti principali per DirectX 9.0c non sono stati modificati dopo l'aggiornamento dell'estate 2004 di DirectX SDK e corrispondono a quanto rilasciato con Microsoft Windows XP SP2, Windows XP Pro x64 Edition e Windows Server 2003 SP1. Windows Vista include DirectX 10, che supporta Windows Display Driver Model (WDDM) e Direct3D 10.x. Windows 7 e Windows Vista (vedere [KB971644](https://support.microsoft.com/kb/971644)) supportano DirectX 11, che supporta Direct3D 11, Direct2D, DirectWrite, il dispositivo di rendering software WARP10 e i livelli di funzionalità 10level9. Per [altri dettagli, vedere Api](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) Windows grafica in Windows.

I componenti facoltativi vengono rilasciati negli aggiornamenti di DirectX SDK e includono D3DX, XACT, XAudio2, XINPUT, DirectX gestito e altri componenti di questo tipo. Molti dei componenti facoltativi vengono aggiornati regolarmente per integrare il feedback dei clienti ed esporre nuove funzionalità.

## <a name="directx-version-number"></a>Numero di versione di DirectX

Il numero di versione di DirectX, ad esempio 9.0c, fa riferimento solo alla versione dei componenti di base, ad esempio Direct3D, DirectInput o DirectSound. Questo numero non include le versioni dei vari componenti facoltativi rilasciati in DirectX SDK, ad esempio D3DX, XACT, XINPUT e così via.

In generale, il numero di versione di DirectX non è significativo se non come riferimento rapido ai bit di base della fase di esecuzione. Questo numero non deve essere usato per verificare se il runtime DirectX corretto è già installato, perché non prende in considerazione i componenti DirectX facoltativi.

## <a name="directx-libraries"></a>Librerie DirectX

In passato, i componenti facoltativi di DirectX SDK, incluso D3DX, venivano rilasciati come librerie statiche. Tuttavia, ora vengono rilasciate come librerie di tipo dinamico (DLL) a causa dell'aumento della richiesta di procedure di sicurezza migliori. Le DLL consentono la manutenzione di codice rilasciato in precedenza. Se questi componenti fossero distribuiti come librerie statiche, Microsoft non sarebbe in grado di risolvere i problemi di sicurezza rilevati dopo il rilascio.

Quando le funzionalità vengono aggiunte o modificate nei componenti facoltativi, vengono modificati anche i nomi delle DLL corrispondenti per garantire che non siano causate regressioni per i giochi esistenti che usano componenti rilasciati. Le DLL per ogni componente live side-by-side e gli sviluppatori di giochi possono scegliere esattamente la versione DLL utilizzata dal gioco collegando alla libreria di importazione corrispondente.

Anche se assicurarsi che le DLL siano installate in un sistema non è semplice come il semplice collegamento a librerie statiche, sono state apportate alcune modifiche a DirectX SDK per risolvere i problemi del modello dll:

-   Il componente ridistribuibile DirectX può essere configurato in modo da contenere solo i componenti necessari all'applicazione per ridurre al minimo la distribuzione e le dimensioni dei supporti.
-   La cartella ridistribuibile, Programmi DirectX SDK Redist, contiene ora un file CAB (.cab) per ogni possibile componente facoltativo, quindi non è necessario cercare un \\ \\ SDK \\ precedente.
-   L'installazione dell'SDK stesso installa tutti i possibili componenti facoltativi.
-   Un componente ridistribuibile DirectX che contiene tutti i componenti facoltativi è disponibile sia come programma di installazione basato sul Web che come pacchetto scaricabile. Per altre informazioni, vedere il Centro per sviluppatori DirectX ([DirectX](/previous-versions/windows/apps/hh452744(v=win.10))).

## <a name="installation-of-directx-by-the-games-installer"></a>Installazione di DirectX da parte del programma di installazione del gioco

> [!Note]  
> Vedere [Distribuzione di Direct3D 11 per sviluppatori di giochi.](/windows/desktop/direct3darticles/direct3d11-deployment)

 

Di seguito sono riportate le procedure consigliate per aggiungere l'installazione di DirectX al programma di installazione di un gioco:




| Termine | Descrizione | 
|------|-------------|
| <span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Installare i componenti ridistribuibili ogni volta. <br /> | Il processo di installazione di un gioco deve installare i componenti ridistribuibili DirectX durante ogni singola installazione senza consentire agli utenti di rifiutare esplicitamente il programma. Se si consente il rifiuto esplicito, alcuni utenti intuiranno che non sono necessari e, se effettivamente lo fanno, il gioco non verrà eseguito. <br /> | 
| <span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Consentire al programma di installazione di DirectX di verificare la presenza di componenti facoltativi. <br /> | Non presupporre che i componenti facoltativi più recenti siano già installati in un sistema, perché Windows Update e i Service Pack non forniscono alcun componente facoltativo di DirectX. È necessario installare il runtime DirectX eseguendo direttamente dxsetup.exe o chiamando DirectSetup. <br /> | 
| <span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Configurare in modo invisibile all'utente. <br /> | Avviare l'installazione in modalità invisibile all'utente in modo che gli utenti non eselevano accidentalmente l'aggiornamento del runtime DirectX. A tale scopo, avviare dxsetup.exe con il comando seguente: <br /><pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>o chiamando DirectSetup e non visualizzando alcuna interfaccia utente. <br /> | 
| <span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Combinare le accettazioni delle regole di licenza con l'utente finale. <br /> | Se si richiede all'utente di accettare un contratto di licenza, combinarlo con la richiesta di accettazione del contratto di licenza DirectX durante l'installazione in modalità invisibile all'utente, in modo che la richiesta di accettazione dei contratto di licenza venga eseguita una sola volta. La richiesta deve essere visualizzata prima di installare qualsiasi elemento in modo che, se l'utente non accetta, non si verifica un'installazione parziale e non riuscita. <br /> | 
| <span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>È sufficiente eseguire dxsetup o chiamare DirectSetup. <br /> | Poiché il numero di versione di DirectX non fa riferimento ad alcun elemento ad eccezione dei componenti DirectX principali, non controllare una versione installata prima di eseguire dxsetup.exe o chiamare DirectSetup. Inoltre, non verificare l'esistenza di un file per verificare se un componente facoltativo è già installato, perché in genere non determina correttamente quando un componente esiste ma richiede l'aggiornamento. Tuttavia, il pacchetto di installazione di DirectX determinerà rapidamente questo problema ed eseguirà l'azione appropriata. <br /> | 




 

## <a name="small-installation-packages"></a>Pacchetti di installazione di piccole dimensioni

È possibile creare pacchetti di installazione più piccoli per DirectX rimuovendo il contenuto della cartella ridistribuibile DirectX fino al set minimo di file necessari per il funzionamento del programma di installazione e mantenendo eventuali componenti aggiuntivi utilizzati dal gioco.

A seconda delle specifiche minime, potrebbe non essere necessario includere i file cab DirectX 9.0c di base nella cartella ridistribuibile del supporto di installazione. La maggior parte delle installazioni di Windows XP include Service Pack 2, che include i componenti di base di DirectX 9.0c, quindi l'operazione di installazione di DirectX sarà molto veloce e non richiederà un riavvio. Il pacchetto più piccolo che può essere creato è di circa 3 MB e può essere compresso a circa la metà di tale dimensione. Un pacchetto come questo contiene una versione della DLL D3DX e richiede che DirectX 9.0c sia già presente.

Il set minimo di file necessari per compilare un pacchetto ridistribuibile è il seguente, che si trova nella cartella Redist di DirectX SDK (Programmi \\ DirectX SDK \\ \) Redist:

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Aggiungere a questi file CAB per i componenti che si desidera installare. Se è necessario che gli utenti dell'applicazione abbia già DirectX 9.0c, non è necessario includere DirectX.cab o dxnt.cab, che costituiscono la maggior parte dei requisiti di spazio. DirectX.cab è necessario solo per Windows 98 e Windows ME; dxnt.cab è necessario solo per Windows 2000, Windows XP e Windows XP SP1; e dxdllregx86.cab sono necessari solo per \_ Windows 2000, Windows XP RTM, Windows XP SP1 e Windows Server 2003 RTM. Inoltre, se non si usa DirectShow o si presuppone che sia già installato, è possibile omettere BDA.cab, BDANT.cab e BDAXP.cab.

> [!Note]  
> È possibile presupporre che gli utenti dell'applicazione dispongono già di DirectX 9.0c se è stata installata da una versione precedente dell'applicazione, si forzano gli utenti a eseguire manualmente l'aggiornamento tramite il programma di installazione Web o si presuppone che abbia Windows XP SP2 o versione successiva.

 

Continuando con questo esempio, se si usa solo la versione a 32 bit di D3DX per aprile 2006, è possibile aggiungere Apr2006 \_ d3dx9 \_ 30 \_x86.cab. Se si usa la versione a 32 bit di XINPUT di agosto 2006 a 32 bit, aggiungere Aug2006 \_ xinput \_x86.cab.

Se si ha un'applicazione nativa a 64 bit, è necessario aggiungere le \_ versioni x64. Tuttavia, se si dispone di un'applicazione a 32 bit in esecuzione in un sistema operativo a 64 bit, le versioni a 32 bit delle DLL funzioneranno.

È quindi possibile distribuire questo pacchetto di file e avviare DirectSetup in modalità invisibile all'utente o dxsetup.exe nella shell dei comandi in modalità invisibile all'utente. Ricordarsi di non proteggere questo pacchetto con il controllo della versione dei file e assicurarsi che gli utenti non siano in grado di rifiutare esplicitamente l'esecuzione dell'installazione di DirectX. Uno di questi eventi crea un processo di installazione fallibile.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Distribuzione interna del runtime DirectX di debug

I runtime di debug dei componenti DirectX vengono installati durante l'installazione di DirectX SDK, ma l'installazione dell'SDK in ogni computer di test può essere difficile. È necessario progettare il processo di installazione per copiare le DLL di runtime di debug dall'architettura del runtime di sviluppo di Microsoft DirectX SDK per Programmi \\ \\ Windows \\ \\ \\ system32 \\ o nella cartella del gioco.

Tuttavia, è consigliabile non copiare semplicemente le DLL di run-time rilasciate perché è facile dimenticare di rimuoverle per il prodotto finale. Inserire invece i file di installazione di DirectX in una cartella condivisa ed eseguire il programma di installazione in modo invisibile all'utente dalla cartella condivisa.

## <a name="desktop-bridge-applications"></a>Desktop Bridge applicazioni 

Desktop Bridge applicazioni che usano D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 o XACT devono scaricare il framework [Microsoft.DirectX.x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) o [Microsoft.DirectX.x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) per distribuire questi componenti legacy di DirectX SDK side-by-side. In alternativa, è possibile rimuovere tutte queste dipendenze (vedere guida per gli sviluppatori per la versione ridistribuibile di &mdash; [XAudio 2.9](../xaudio2/xaudio2-redistributable.md)e i post di blog [Living without D3DX](https://walbourn.github.io/living-without-d3dx/) and [XINPUT and Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).
