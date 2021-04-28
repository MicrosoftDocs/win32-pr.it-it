---
description: Manifesto dell'applicazione
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifesto dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088589"
---
# <a name="application-manifest"></a>Manifesto dell'applicazione

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

Windows 7 introduce una nuova sezione nel manifesto dell'applicazione denominata "Compatibilità". Questa sezione consente a Windows di determinare le versioni di Windows destinate a un'applicazione e consente a Windows di fornire il comportamento previsto dall'applicazione in base alla versione di Windows di destinazione dell'applicazione.

La sezione Compatibilità consente a Windows di fornire un nuovo comportamento al nuovo software creato dallo sviluppatore mantenendo al tempo stesso la compatibilità per il software esistente. Questa sezione consente anche a Windows di offrire maggiore compatibilità anche nelle versioni future di Windows. Ad esempio, un'applicazione che dichiara il supporto solo per Windows 7 nella sezione Compatibilità continuerà a ricevere il comportamento di Windows 7 nella versione futura di Windows.

## <a name="manifestation-of-change"></a>Modifica apportata

Le applicazioni senza una sezione Compatibility nel manifesto riceveranno il comportamento di Windows Vista per impostazione predefinita in Windows 7 e versioni future di Windows. Si noti che Windows XP e Windows Vista ignorano questa sezione del manifesto e non influiscono su di esse.

I componenti di Windows seguenti offrono un comportamento divergente in base alla sezione Compatibilità in Windows 7:

**Pool di thread predefinito RPC**

-   **Windows 7:** Per migliorare la scalabilità e ridurre il numero di thread, RPC è passata al pool di thread NT (pool predefinito). Per Windows Vista, RPC usa un pool di thread privato.
    -   Per i file binari compilati per Win7 viene usato il pool predefinito
    -   Se I RpcMgmtEnableDedicatedThreadPool viene chiamato prima di qualsiasi API RPC, viene usato il pool di thread privato \_ (comportamento vista)
    -   Se I RpcMgmtEnableDedicatedThreadPool viene chiamato dopo una chiamata RPC, viene usato il \_ pool predefinito, I RpcMgmtEnableDedicatedThreadPool restituisce l'errore 1764 e l'operazione richiesta non è \_ supportata
-   **Windows Vista (impostazione predefinita):** Per i file binari compilati per Windows Vista e versioni seguenti, viene usato il pool privato.

**Blocco DirectDraw**

-   **Windows 7:** Le applicazioni manifeste per Windows 7 non possono chiamare l'API Lock in DDRAW per bloccare il buffer video desktop primario. In questo modo verrà restituito un errore e verrà restituito **il puntatore NULL** per il database primario. Questo comportamento viene applicato anche se Gestione finestre desktop composizione non è attivata. Le applicazioni compatibili con Windows 7 non devono bloccare il buffer video primario per il rendering.
-   **Windows Vista (impostazione predefinita):** Le applicazioni saranno in grado di acquisire un blocco sul buffer video primario, in quanto le applicazioni legacy dipendono da questo comportamento. L'esecuzione dell'applicazione Gestione finestre desktop.

**Trasferimento del blocco di bit DirectDraw (Blt) a primario senza finestra di ritaglio**

-   **Windows 7:** Alle applicazioni manifeste per Windows 7 non è consentito eseguire Blt nel buffer video desktop primario senza una finestra di ritaglio. In questo modo verrà generato un errore e non verrà eseguito il rendering dell'area Blt. Windows applica questo comportamento anche se non si attiva Gestione finestre desktop composizione. Le applicazioni compatibili con Windows 7 devono essere distribuite in una finestra di ritaglio.
-   **Windows Vista (impostazione predefinita):** Le applicazioni devono essere in grado di eseguire il Blt nel database primario senza una finestra di ritaglio, in quanto le applicazioni legacy dipendono da questo comportamento. L'esecuzione di questa applicazione disattiva la Gestione finestre desktop.

**GetOverlappedResult API**

-   **Windows 7:** Risolve un race condition in cui un'app multithreading che usa GetOverlappedResult può restituire senza reimpostare l'evento nella struttura sovrapposta, causando la restituzione prematura della chiamata successiva a questa funzione.
-   **Windows Vista (impostazione predefinita):** Fornisce il comportamento con il race condition da cui le applicazioni possono avere una dipendenza. Le applicazioni che vogliono evitare questa race prima del comportamento di Windows 7 devono attendere l'evento sovrapposto e, quando viene segnalato, chiamare GetOverlappedResult con bWait == **FALSE.**

**Program Compatibility Assistant (PCA)**

-   **Windows 7:** La sezione Applicazioni con compatibilità non riceverà la mitigazione PCA.
-   **Windows Vista (impostazione predefinita):** Le applicazioni che non vengono installate correttamente o si arresteranno in modo anomalo durante il runtime in determinate circostanze otterrà la mitigazione PCA. Per altri dettagli, vedere la sezione di riferimento.

## <a name="leveraging-feature-capabilities"></a>Uso delle funzionalità

Aggiornare il manifesto dell'applicazione con le informazioni di compatibilità più recenti per il supporto del sistema operativo. La sezione descrive le aggiunte al manifesto:

-   **Spazio dei nomi:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)

-   **Nome sezione:** Compatibilità (nuova sezione)

-   **SupportedOS:** GUID del sistema operativo supportato: i GUID mappati ai sistemi operativi supportati sono:

    -   {e2011457-1546-43c5-a5fe-008dee3d3f0} per Windows Vista: questo è il valore predefinito per il contesto di switchback.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} per Windows 7: le applicazioni che impostano questo valore nel manifesto dell'applicazione ottengono il comportamento di Windows 7.

    > [!Note]  
    > Microsoft genererà e inviare GUID per le versioni future di Windows in base alle esigenze.

     

Di seguito è riportato un esempio di manifesto aggiornato.

> [!Note]  
> I nomi di attributo e tag nel manifesto dell'applicazione fa distinzione tra maiuscole e minuscole.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



Il valore dell'aggiunta di GUID per entrambi i sistemi operativi nell'esempio precedente è fornire supporto di livello inferiore. Le applicazioni che supportano entrambe le piattaforme non necessitano di manifesti separati per ogni piattaforma.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

1.  Testare l'applicazione con la nuova sezione relativa alla compatibilità e assicurarsi che l'applicazione funzioni `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` correttamente usando il comportamento più recente di Windows 7
2.  Testare l'applicazione con la nuova sezione di compatibilità e (o senza questa sezione) per assicurarsi che l'applicazione funzioni correttamente usando i comportamenti di `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` Windows Vista in Windows 7

## <a name="known-issues"></a>Problemi noti

**Mancata corrispondenza del contesto** Un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer che esegue un'edizione x64 di Windows 7 o Windows Server 2008 R2.

**Soluzione** Sono disponibili aggiornamenti per risolvere questo problema per tutte le versioni supportate basate su x64 di Windows 7 e Windows Server 2008 R2, nonché per tutte le versioni supportate basate su Itanium di Windows Server 2008 R2. Passare alla pagina Supporto tecnico Microsoft per KB 978637: un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer che esegue [un'edizione x64 di Windows 7 o Windows Server 2008 R2](https://support.microsoft.com/kb/978637) per altri dettagli e per scaricare la versione corretta per il sistema.

**Diagnosi di dump di arresto anomalo del sistema bloccata**

**Soluzione** Passare alla pagina Supporto tecnico Microsoft [kb 976038:](https://support.microsoft.com/kb/976038) le eccezioni generate da un'applicazione eseguita in una versione a 64 bit di Windows vengono ignorate per altri dettagli.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [**Funzione QueryActCtxW**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [Manifesto del controllo dell'account utente](/previous-versions/bb756929(v=msdn.10))
-   [Manifesti dell'applicazione per le applicazioni Windows](../sbscs/application-manifests.md)
-   [Gestione finestre desktop (DWM)](../dwm/dwm-overview.md)
-   [Aggiornamento della mancata corrispondenza del contesto](https://support.microsoft.com/kb/978637)

 

 
