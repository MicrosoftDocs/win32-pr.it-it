---
title: Installazione di DirectX per sviluppatori di giochi
description: Questo articolo ha lo scopo di risolvere alcune delle domande comuni sul runtime di DirectX e di usare DirectSetup per installare DirectX.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c0faf346bd8793e61a89128ce573e29b7a8267
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047222"
---
# <a name="directx-installation-for-game-developers"></a>Installazione di DirectX per sviluppatori di giochi

Questo articolo ha lo scopo di risolvere alcune delle domande comuni sul runtime di DirectX e di usare DirectSetup per installare DirectX.

-   [Runtime di DirectX](#directx-runtime)
-   [Numero di versione di DirectX](#directx-version-number)
-   [Librerie DirectX](#directx-libraries)
-   [Installazione di DirectX dal programma di installazione del gioco](#installation-of-directx-by-the-games-installer)
-   [Pacchetti di installazione di piccole dimensioni](#small-installation-packages)
-   [Distribuzione interna del runtime DirectX di debug](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> Legacy DirectX SDK è alla fine del ciclo di vita, ma è ancora disponibile per supportare i vecchi giochi, le esercitazioni e i progetti. I nuovi progetti non devono utilizzarlo. L'uso di DirectX SDK legacy richiede l'uso di DirectSetup deprecati per i componenti quali D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 e XACT. Per altri dettagli sullo stato corrente di DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md)e il post di Blog [non è così diretto](https://walbourn.github.io/not-so-direct-setup/).

## <a name="directx-runtime"></a>Runtime di DirectX

Il runtime di DirectX è costituito da componenti di base e componenti facoltativi.

I componenti principali, ad esempio Direct3D e DirectInput, sono considerati parte del sistema operativo. I componenti di base per DirectX 9.0 c non sono stati modificati rispetto all'aggiornamento dell'estate 2004 di DirectX SDK e corrispondono a quelli rilasciati con Microsoft Windows XP SP2, Windows XP Pro x64 Edition e Windows Server 2003 SP1. Windows Vista include DirectX 10, che supporta Windows Display Driver Model (WDDM) e Direct3D 10. x. Windows 7 e Windows Vista (vedere [KB971644](https://support.microsoft.com/kb/971644)) supportano DirectX 11, che supporta Direct3D 11, Direct2D, DirectWrite, il dispositivo di rendering del software WARP10 e i livelli di funzionalità 10level9. Per altri dettagli, vedere [API grafiche in Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) .

I componenti facoltativi vengono rilasciati negli aggiornamenti di DirectX SDK e includono D3DX, XACT, XAudio2, XINPUT, Managed DirectX e altri componenti di questo tipo. Molti dei componenti facoltativi vengono aggiornati regolarmente per integrare i commenti dei clienti ed esporre le nuove funzionalità.

## <a name="directx-version-number"></a>Numero di versione di DirectX

Il numero di versione di DirectX, ad esempio 9.0 c, si riferisce solo alla versione dei componenti di base, ad esempio Direct3D, DirectInput o DirectSound. Questo numero non copre le versioni dei diversi componenti facoltativi rilasciati in DirectX SDK, ad esempio D3DX, XACT, XINPUT e così via.

In generale, il numero di versione di DirectX non è significativo, eccetto come riferimento rapido ai bit di runtime di base. Questo numero non deve essere usato per verificare se è già installato il runtime DirectX corretto, perché non prende in considerazione i componenti facoltativi di DirectX.

## <a name="directx-libraries"></a>Librerie DirectX

In passato, i componenti facoltativi di DirectX SDK, incluso D3DX, venivano rilasciati come librerie statiche. Tuttavia, sono ora rilasciate come librerie di tipo dinamico (DLL) a causa della maggiore richiesta di procedure di sicurezza migliori. Le DLL consentono la manutenzione del codice rilasciato in precedenza. Se questi componenti sono stati distribuiti come librerie statiche, non esiste alcun modo per Microsoft per risolvere i problemi di sicurezza rilevati dopo il rilascio.

Quando le funzionalità vengono aggiunte o modificate ai componenti facoltativi, vengono modificati anche i nomi delle DLL corrispondenti per assicurarsi che non siano presenti regressioni a giochi esistenti che utilizzano componenti rilasciati. Le dll per ogni componente sono Live Side-by-side e gli sviluppatori di giochi possono scegliere esattamente la versione DLL utilizzata dal gioco collegandosi alla libreria di importazione corrispondente.

Assicurandosi che le dll siano installate in un sistema non sia semplice quanto semplicemente il collegamento alle librerie statiche, sono state apportate alcune modifiche a DirectX SDK per risolvere i problemi del modello di DLL:

-   DirectX Redistributable può essere configurato in modo da contenere solo i componenti richiesti dall'applicazione per ridurre al minimo la distribuzione e le dimensioni dei supporti.
-   La cartella Redistributable, programmi \\ DirectX SDK \\ Redist \\ , contiene ora un file CAB (con estensione cab) per ogni possibile componente facoltativo, quindi non è necessario approfondire un SDK precedente per trovarli.
-   Con l'installazione dell'SDK viene installato ogni possibile componente facoltativo.
-   Un pacchetto ridistribuibile DirectX che contiene tutti i componenti facoltativi è disponibile sia come programma di installazione basato sul Web che come pacchetto scaricabile. Per ulteriori informazioni, vedere il centro per sviluppatori[DirectX (DirectX](/previous-versions/windows/apps/hh452744(v=win.10))).

## <a name="installation-of-directx-by-the-games-installer"></a>Installazione di DirectX dal programma di installazione del gioco

> [!Note]  
> Vedere [la pagina relativa alla distribuzione di Direct3D 11 per sviluppatori di giochi](/windows/desktop/direct3darticles/direct3d11-deployment).

 

Di seguito sono riportate le procedure consigliate per aggiungere l'installazione di DirectX al programma di installazione di un gioco:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Termine</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Installare i componenti ridistribuibili ogni volta. <br/></td>
<td>Il processo di installazione di un gioco deve installare i componenti ridistribuibili di DirectX durante ogni singola installazione senza consentire agli utenti di rifiutare esplicitamente l'installazione. Se si consente la disattivazione, alcuni utenti indovinano che non sono necessari e, in caso affermativo, il gioco non verrà eseguito. <br/></td>
</tr>
<tr class="even">
<td><span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Consentire al programma di installazione di DirectX di verificare la presenza di componenti facoltativi. <br/></td>
<td>Non presupporre che i componenti facoltativi più recenti siano già installati in un sistema, perché Windows Update e i Service Pack non forniscono i componenti facoltativi di DirectX. È necessario installare il runtime di DirectX eseguendo direttamente dxsetup.exe o chiamando DirectSetup. <br/></td>
</tr>
<tr class="odd">
<td><span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Configurare in modo invisibile all'utente. <br/></td>
<td>Avviare il programma di installazione in modalità invisibile all'utente in modo che gli utenti non ignorino accidentalmente l'aggiornamento di DirectX Runtime. Questa operazione può essere eseguita avviando dxsetup.exe con il comando seguente: <br/>
<pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>
oppure chiamando DirectSetup e non mostrando alcuna interfaccia utente. <br/></td>
</tr>
<tr class="even">
<td><span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Combinare le accettazioni EULA. <br/></td>
<td>Se si richiede all'utente di accettare un contratto di licenza, combinarlo con la richiesta di accettazione del contratto di licenza DirectX quando si installa in modalità invisibile all'utente, in modo che la richiesta di accettazione delle EULA avvenga una sola volta. La richiesta di conferma deve essere eseguita prima di installare qualsiasi elemento, in modo che se l'utente non accetta, non si verificherà un'installazione non riuscita e parziale. <br/></td>
</tr>
<tr class="odd">
<td><span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>È sufficiente eseguire Dxsetup o chiamare DirectSetup. <br/></td>
<td>Poiché il numero di versione di DirectX non fa riferimento ad alcun componente principale di DirectX, non controllare una versione installata prima di eseguire dxsetup.exe o chiamare DirectSetup. Inoltre, non verificare l'esistenza di un file per verificare se è già installato un componente facoltativo, poiché questo in genere non determina correttamente quando un componente esiste, ma deve essere aggiornato. Tuttavia, il pacchetto di installazione di DirectX determinerà rapidamente questa operazione ed eseguirà l'azione appropriata. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="small-installation-packages"></a>Pacchetti di installazione di piccole dimensioni

È possibile creare pacchetti di installazione di dimensioni ridotte per DirectX rimuovendo il contenuto della cartella DirectX Redistributable fino al set minimo di file necessari per il funzionamento del programma di installazione e mantenendo i componenti aggiuntivi usati dal gioco.

A seconda delle specifiche minime, potrebbe non essere necessario includere i file CAB DirectX 9.0 c principali nella cartella ridistribuibile del supporto di installazione. Per la maggior parte delle installazioni di Windows XP è disponibile il Service Pack 2, che include i componenti di base di DirectX 9.0 c, quindi l'operazione di installazione di DirectX sarà molto rapida e non sarà necessario riavviare il computer. Il pacchetto più piccolo che è possibile creare è di circa 3 MB e può essere compresso fino a metà delle dimensioni. Un pacchetto di questo tipo contiene una versione della DLL di D3DX e richiede che sia già presente DirectX 9.0 c.

Il set minimo di file necessari per compilare un pacchetto ridistribuibile è costituito dai file seguenti, che si trovano nella cartella DirectX SDK Redist (Program Files \\ DirectX SDK \\ Redist \) :

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Aggiungere a questi file CAB i componenti che si desidera installare. Se è necessario che gli utenti dell'applicazione dispongano già di DirectX 9.0 c, non è necessario includere DirectX.cab o dxnt.cab, che costituiscono la maggior parte del requisito di spazio. DirectX.cab è necessario solo per Windows 98 e Windows ME; dxnt.cab è necessario solo per Windows 2000, Windows XP e Windows XP SP1; e dxdllreg \_x86.cab è necessario solo per windows 2000, Windows XP RTM, Windows XP SP1 e Windows Server 2003 RTM. Inoltre, se non si utilizza DirectShow o si presuppone che sia già installato, è possibile omettere BDA.cab, BDANT.cab e BDAXP.cab.

> [!Note]  
> Si può presupporre che gli utenti dell'applicazione dispongano già di DirectX 9.0 c se è stato installato da una versione precedente dell'applicazione, si impone agli utenti di eseguire manualmente l'aggiornamento tramite il programma di installazione Web o si presuppone che dispongano di Windows XP SP2 o versione successiva.

 

Continuando con questo esempio, se si usa solo la versione a 32 bit di D3DX per il 2006 aprile, è possibile aggiungere Apr2006 \_ d3dx9 \_ 30 \_x86.cab. Se si usa la versione di XINPUT a 32 bit di agosto 2006 32, è necessario aggiungere Aug2006 \_ XINPUT \_x86.cab.

Se si dispone di un'applicazione nativa a 64 bit, è necessario aggiungere le \_ versioni x64. Tuttavia, se si dispone di un'applicazione a 32 bit in esecuzione su un sistema operativo a 64 bit, le versioni a 32 bit delle dll funzioneranno.

È quindi possibile distribuire questo pacchetto di file e avviare DirectSetup in modalità invisibile all'utente o eseguire dxsetup.exe nella shell dei comandi in modalità invisibile all'utente. Ricordarsi di non sorvegliare il pacchetto con il controllo della versione dei file e verificare che gli utenti non possano rifiutare esplicitamente l'esecuzione dell'installazione di DirectX. Uno di questi eventi crea un processo di installazione fallibile.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Distribuzione interna del runtime DirectX di debug

I runtime di debug dei componenti DirectX vengono installati quando si installa DirectX SDK, ma l'installazione dell'SDK su ogni computer di test può essere un'eccezione. È necessario progettare il processo di installazione per copiare le DLL di runtime di debug da programmi \\ Microsoft DirectX SDK \\ Developer Runtime \\ Architecture \\ a Windows \\ system32 \\ o alla cartella del gioco.

Tuttavia, si consiglia di non copiare semplicemente le DLL di runtime rilasciate poiché è facile dimenticare di rimuoverle per il prodotto finale. In alternativa, inserire i file di installazione di DirectX in una cartella condivisa ed eseguire il programma di installazione automaticamente dalla cartella condivisa.

## <a name="desktop-bridge-applications"></a>Applicazioni desktop Bridge 

Le applicazioni desktop Bridge che usano D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 o XACT devono scaricare il Framework [Microsoft. DirectX. x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) o [Microsoft. DirectX. x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) per distribuire questi componenti side-by-side legacy di DirectX SDK. In alternativa, è possibile rimuovere tutte le dipendenze &mdash; (vedere la [Guida per gli sviluppatori per la versione ridistribuibile di xaudio 2,9](../xaudio2/xaudio2-redistributable.md)e i post di Blog che [vivono senza D3DX](https://walbourn.github.io/living-without-d3dx/) e [XINPUT e Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).