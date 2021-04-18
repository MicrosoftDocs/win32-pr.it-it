---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifesto dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318888"
---
# <a name="application-manifest"></a>Manifesto dell'applicazione

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

In Windows 7 è stata introdotta una nuova sezione nel manifesto dell'applicazione denominata "compatibilità". Questa sezione consente a Windows di determinare le versioni di Windows per cui un'applicazione è stata progettata come destinazione e consente a Windows di fornire il comportamento previsto dall'applicazione in base alla versione di Windows di destinazione dell'applicazione.

La sezione compatibilità consente a Windows di fornire nuovo comportamento al nuovo software creato dagli sviluppatori, mantenendo al tempo stesso la compatibilità per il software esistente. Questa sezione consente inoltre a Windows di garantire una maggiore compatibilità nelle versioni future di Windows. Ad esempio, un'applicazione che dichiara il supporto solo per Windows 7 nella sezione compatibilità continuerà a ricevere il comportamento di Windows 7 nella versione futura di Windows.

## <a name="manifestation-of-change"></a>Manifesto della modifica

Le applicazioni prive di una sezione di compatibilità nel manifesto riceveranno il comportamento di Windows Vista per impostazione predefinita in Windows 7 e nelle versioni future di Windows. Si noti che Windows XP e Windows Vista ignorano questa sezione del manifesto e non hanno alcun effetto su di essi.

I componenti di Windows seguenti forniscono un comportamento divergente basato sulla sezione compatibilità di Windows 7:

**Pool di thread predefinito RPC**

-   **Windows 7:** Per migliorare la scalabilità e ridurre i conteggi dei thread, RPC passa al pool di thread NT (pool predefinito). Per Windows Vista, RPC usava un pool di thread privato.
    -   Per i binari compilati per Win7 viene usato il pool predefinito
    -   Se si \_ chiama RpcMgmtEnableDedicatedThreadPool prima che venga chiamata un'API RPC, viene usato il pool di thread privati (comportamento di vista)
    -   Se I \_ RpcMgmtEnableDedicatedThreadPool vengono chiamati dopo una chiamata RPC, viene usato il pool predefinito, \_ RpcMgmtEnableDedicatedThreadPool restituisce l'errore 1764 e l'operazione richiesta non è supportata
-   **Windows Vista (impostazione predefinita):** Per i file binari compilati per Windows Vista e versioni precedenti, viene usato il pool privato.

**Blocco DirectDraw**

-   **Windows 7:** Le applicazioni manifeste per Windows 7 non possono chiamare l'API Lock in DDRAW per bloccare il buffer video del desktop primario. Questa operazione genera un errore e viene restituito un puntatore **null** per il database primario. Questo comportamento viene applicato anche se Gestione finestre desktop composizione non è attivata. Le applicazioni compatibili con Windows 7 non devono bloccare il rendering del buffer video primario.
-   **Windows Vista (impostazione predefinita):** Le applicazioni potranno acquisire un blocco sul buffer video primario perché le applicazioni legacy dipendono da questo comportamento. L'esecuzione dell'applicazione disattiva Gestione finestre desktop.

**Il trasferimento di blocchi di bit (BLT) a database primario senza finestra di ridimensionamento**

-   **Windows 7:** Le applicazioni manifeste per Windows 7 non sono in grado di eseguire BLT nel buffer video del desktop primario senza una finestra di ridimensionamento. In caso contrario, verrà generato un errore e non verrà eseguito il rendering dell'area BLT. Windows applica questo comportamento anche se non si attiva Gestione finestre desktop composizione. Le applicazioni compatibili con Windows 7 devono essere BLT in una finestra di ridimensionamento.
-   **Windows Vista (impostazione predefinita):** Le applicazioni devono essere in grado di eseguire il BLT nel database primario senza una finestra di ridimensionamento poiché le applicazioni legacy dipendono da questo comportamento. L'esecuzione di questa applicazione disattiva la Gestione finestre desktop.

**API GetOverlappedResult**

-   **Windows 7:** Risolve un race condition in cui un'app multithreading che usa GetOverlappedResult può restituire senza reimpostare l'evento nella struttura sovrapposta, causando la restituzione anticipata della chiamata successiva a questa funzione.
-   **Windows Vista (impostazione predefinita):** Fornisce il comportamento con il race condition cui le applicazioni possono avere una dipendenza. Le applicazioni che desiderano evitare questa corsa prima del comportamento di Windows 7 devono attendere l'evento sovrapposto e, quando segnalato, chiamare GetOverlappedResult con bWait = = **false**.

**Assistente compatibilità programmi (PCA)**

-   **Windows 7:** La sezione applicazioni con compatibilità non otterrà la mitigazione PCA.
-   **Windows Vista (impostazione predefinita):** Le applicazioni che non vengono installate correttamente o si arrestano in modo anomalo in fase di esecuzione in alcune circostanze specifiche otterranno la mitigazione PCA. Per ulteriori informazioni, vedere la sezione di riferimento.

## <a name="leveraging-feature-capabilities"></a>Sfruttando le funzionalità

Aggiornare il manifesto dell'applicazione con le informazioni di compatibilità più recenti per il supporto del sistema operativo. La sezione descrive le aggiunte al manifesto:

-   **Spazio dei nomi:** Compatibility. V1 (xmlns = "urn: schemas-microsoft-com: Compatibility. V1" >)

-   **Nome della sezione:** Compatibilità (nuova sezione)

-   **Supportato:** GUID del sistema operativo supportato: i GUID che eseguono il mapping ai sistemi operativi supportati sono:

    -   {e2011457-1546-43C5-a5fe-008deee3d3f0} per Windows Vista: si tratta del valore predefinito per il contesto Switchback.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} per Windows 7: le applicazioni che impostano questo valore nel manifesto dell'applicazione ottengono il comportamento di Windows 7.

    > [!Note]  
    > Microsoft genererà e pubblicherà i GUID per le versioni future di Windows in base alle esigenze.

     

Di seguito è riportato un esempio di un manifesto aggiornato.

> [!Note]  
> I nomi di attributo e tag nel manifesto dell'applicazione fanno distinzione tra maiuscole e minuscole.

 


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



Il valore di aggiunta di GUID per entrambi i sistemi operativi nell'esempio precedente consiste nel fornire supporto di livello inferiore. Le applicazioni che supportano entrambe le piattaforme non necessitano di manifesti distinti per ogni piattaforma.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

1.  Testare l'applicazione con la nuova sezione compatibilità e `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` verificare che l'applicazione funzioni correttamente usando il comportamento più recente di Windows 7
2.  Testare l'applicazione con la nuova sezione di compatibilità e `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (o senza questa sezione) per assicurarsi che l'applicazione funzioni correttamente utilizzando i comportamenti di Windows Vista in Windows 7

## <a name="known-issues"></a>Problemi noti

**Mancata corrispondenza del contesto** Un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer in cui è in esecuzione un'edizione x64 di Windows 7 o Windows Server 2008 R2.

**Soluzione** di Sono disponibili aggiornamenti per correggere questa operazione per tutte le versioni supportate di Windows 7 e Windows Server 2008 R2, nonché per tutte le versioni basate su Itanium supportate di Windows Server 2008 R2. Passare alla pagina supporto tecnico Microsoft per [KB 978637: un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer in cui è in esecuzione un'edizione x64 di Windows 7 o Windows Server 2008 R2](https://support.microsoft.com/kb/978637) per ulteriori dettagli e per scaricare la versione corretta per il sistema.

**Diagnosi del dump di arresto anomalo bloccata**

**Soluzione** di Passare alla pagina supporto tecnico Microsoft per [KB 976038: le eccezioni generate da un'applicazione in esecuzione in una versione di Windows a 64 bit vengono ignorate](https://support.microsoft.com/kb/976038) per ulteriori dettagli.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [**QueryActCtxW (funzione)**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [Manifesto UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifesti dell'applicazione per applicazioni Windows](../sbscs/application-manifests.md)
-   [Gestione finestre desktop (DWM)](../dwm/dwm-overview.md)
-   [Aggiornamento del contesto non corrispondente](https://support.microsoft.com/kb/978637)

 

 
