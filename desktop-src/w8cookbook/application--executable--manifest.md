---
title: Manifesto app (eseguibile)
description: Manifesto app (eseguibile)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047489"
---
# <a name="app-executable-manifest"></a>Manifesto app (eseguibile)

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

La sezione relativa alla compatibilità del manifesto dell'app (eseguibile) introdotta in Windows consente al sistema operativo di determinare le versioni di Windows per cui è stata progettata la destinazione di un'app. Il manifesto dell'app consente inoltre a Windows di fornire il comportamento previsto dall'app in base alla versione di Windows di destinazione dell'app.

La sezione compatibilità del manifesto consente a Windows di fornire nuovo comportamento al software appena creato, mantenendo al tempo stesso la compatibilità per il software esistente. Questa sezione aiuta Windows a offrire una maggiore compatibilità anche nelle versioni future di Windows. Ad esempio, un'app che dichiara il supporto per solo Windows 8 nella sezione compatibilità continuerà a ricevere il comportamento di Windows 8 nelle versioni future di Windows.

## <a name="manifestation"></a>Manifestazione

Le app senza una sezione di compatibilità nel manifesto avranno il comportamento di Windows Vista per impostazione predefinita in Windows 7 e Windows 8 e nelle versioni successive di Windows. Tenere presente che Windows XP e Windows Vista ignorano questa sezione del manifesto e non hanno alcun effetto su di essi.

Questi componenti di Windows forniscono un comportamento divergente basato sulla sezione compatibilità:

**Pool di thread predefinito RPC (Remote Procedure Call)**

-   Windows 8 e Windows 7: per migliorare la scalabilità e ridurre i conteggi dei thread, RPC passa al pool di thread NT (pool predefinito). Per Windows Vista, RPC usava un pool di thread privato:

    -   Per i file binari compilati per Windows 7 e versioni successive di Windows, viene usato il pool predefinito.
    -   Se I \_ RpcMgmtEnableDedicatedThreadPool vengono chiamati prima della chiamata di qualsiasi API RPC, viene usato il pool di thread privati (comportamento di vista).
    -   Se I \_ RpcMgmtEnableDedicatedThreadPool vengono chiamati dopo una chiamata RPC, viene usato il pool predefinito, \_ RpcMgmtEnableDedicatedThreadPool restituisce l'errore 1764 e l'operazione richiesta non è supportata.

-   Windows Vista (impostazione predefinita): per i file binari compilati per Windows Vista e le versioni precedenti di Windows, viene usato il pool privato.

**Blocco DirectDraw**

-   Windows 8 e Windows 7: le app manifestate per Windows 7 e versioni successive del sistema operativo non possono chiamare l'API Lock in DDRAW per bloccare il buffer video del desktop primario. in questo modo si otterrà un errore e viene restituito un puntatore NULL per il database primario. Questo comportamento viene applicato anche se Gestione finestre desktop composizione non è attivata. Le app con compatibilità dichiarata per Windows 7 e versioni successive non devono bloccare il rendering del buffer video primario.
-   Windows Vista (impostazione predefinita): le app possono acquisire un blocco sul buffer video primario, perché le app legacy dipendono da questo comportamento. l'esecuzione dell'app disattiva Gestione finestre desktop.

**Trasferimento a blocchi di bit DirectDraw (BitBlt) a primario senza finestra di ridimensionamento**

-   Windows 8 e Windows 7: le app manifestate per Windows 7 e versioni successive di Windows non possono eseguire un BitBlt al buffer video del desktop primario senza una finestra di ridimensionamento. in questo modo si verifica un errore e non viene eseguito il rendering dell'area BitBlt. Windows applica questo comportamento anche se non si attiva Gestione finestre desktop composizione. Le app con compatibilità dichiarata per Windows 7 e versioni successive devono eseguire un BitBlt in una finestra di ridimensionamento.
-   Windows Vista (impostazione predefinita): le app devono essere in grado di eseguire un BitBlt nel database primario senza una finestra di ridimensionamento, perché le app legacy dipendono da questo comportamento. l'esecuzione di questa app disattiva la Gestione finestre desktop.

**API GetOverlappedResult**

-   Windows 8 e Windows 7: risolve un race condition in cui un'app multithreading che usa **GetOverlappedResult** può restituire senza reimpostare l'evento nella struttura sovrapposta, causando la restituzione anticipata della chiamata successiva a questa funzione.
-   Windows Vista (impostazione predefinita): fornisce il comportamento con il race condition cui le app possono avere una dipendenza. Le app che devono evitare questa corsa prima del comportamento di Windows 7 devono attendere l'evento sovrapposto e, quando segnalate, chiamare GetOverlappedResult con bWait = = FALSE.

**Stato temi Shell in modalità a contrasto elevato**

-   Windows 8: restituisce lo stato del tema reale per in modalità a contrasto elevato.
-   Windows 7: i temi non sono disponibili quando si è in modalità a contrasto elevato perché DWM è ancora in funzione.
-   Windows Vista (impostazione predefinita): restituisce un tema non disponibile in modalità a contrasto elevato perché DWM è ancora acceso.

**Metodo Shell iPersistFile:: Save**

-   Windows 8: CShellLink:: Save ora determina se il gestore IPersistFile viene chiamato con un argomento di percorso relativo e non riesce a chiamare se è.

    La [documentazione pubblica](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) che descrive questo comportamento indica che l'argomento path deve essere un percorso assoluto:

-   Windows 7 e versioni precedenti (impostazione predefinita): CShellLink:: Save non determina se il gestore iPersistFile Invia un controllo del percorso relativo e consente alle app di continuare a usare percorsi assoluti o relativi.

**Assistente compatibilità programmi (PCA)**

-   Windows 8: le app con la sezione compatibilità non ottengono la mitigazione PCA.
-   Windows 7: le app con la sezione compatibilità vengono registrate per i potenziali problemi di compatibilità per le modifiche apportate a Windows 8 (descritte in questo documento).
-   Windows Vista (impostazione predefinita): le app che non vengono installate correttamente o arrestano in modo anomalo in fase di esecuzione in alcune circostanze specifiche ottengono la mitigazione PCA. Per altre informazioni, vedere la sezione Resources (risorse).

## <a name="leveraging-feature-capabilities"></a>Sfruttando le funzionalità

Aggiornare il manifesto dell'applicazione con le ultime informazioni sulla compatibilità per il supporto del sistema operativo. In questa sezione vengono descritte le aggiunte al manifesto:

**Spazio dei nomi:** Compatibility. V1 (xmlns = "urn: schemas-microsoft-com: Compatibility. V1" >)

**Nome della sezione:** Compatibilità (nuova sezione)

**Supportato:** GUID del sistema operativo supportato: i GUID che eseguono il mapping ai sistemi operativi supportati sono:

-   {e2011457-1546-43c5-a5fe-008deee3d3f0}

    per **Windows Vista**: si tratta del valore predefinito per il contesto Switchback

-   {35138b9a-5d96-4fbd-8e2d-a2440225f93a}

    per **Windows 7**: le app che impostano questo valore nel manifesto dell'app ottengono il comportamento di Windows 7

-   {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}

    per **Windows 8**: le app che impostano questo valore nel manifesto dell'applicazione ottengono il comportamento di Windows 8

Microsoft genererà e pubblicherà i GUID per le versioni future di Windows in base alle esigenze.

Esempio XML di un manifesto aggiornato:

> [!Note]  
> I nomi di attributo e tag nel manifesto dell'applicazione fanno distinzione tra maiuscole e minuscole.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



I GUID per tutti i sistemi operativi nell'esempio precedente forniscono supporto di livello inferiore. Le app che supportano più piattaforme non necessitano di manifesti distinti per ogni piattaforma.

## <a name="tests"></a>Test

Un'app può specificare più ID del sistema operativo supportati. È necessario aggiungere un ID sistema operativo supportato se è stato testato o si sta eseguendo il test dell'app nel sistema operativo. Windows Vista e le versioni precedenti del sistema operativo non prestano attenzione a queste voci. A partire da Windows 7, Windows sceglierà il GUID della versione più recente nel manifesto fino alla versione di Windows in esecuzione e fornirà il supporto dell'app a tale livello. Per verificare che l'app funzioni con la nuova sezione compatibilità del manifesto dell'applicazione:

1.  Testare l'app con la nuova sezione relativa alla compatibilità e ID supportati = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} per assicurarsi che l'app funzioni correttamente usando il comportamento più recente di Windows 8.
2.  Testare l'app con la nuova sezione relativa alla compatibilità e ID supportati = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} per assicurarsi che l'app funzioni correttamente usando il comportamento di Windows 7.
3.  Testare l'app con la nuova sezione relativa alla compatibilità e ID supportati = {e2011457-1546-43C5-a5fe-008deee3d3f0} per assicurarsi che l'app funzioni correttamente usando il comportamento di Windows Vista.

## <a name="resources"></a>Risorse

-   [QueryActCtxW (funzione)](../sbscs/application-manifests.md)
-   [Manifesto UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifesti dell'applicazione per applicazioni Windows](../sbscs/application-manifests.md)
-   [Gestione finestre desktop (DWM)](../dwm/dwm-overview.md)
-   [Aggiornamento del contesto non corrispondente](https://support.microsoft.com/kb/978637)
-   [Assistente compatibilità programmi](/previous-versions/bb756937(v=msdn.10))

 

 