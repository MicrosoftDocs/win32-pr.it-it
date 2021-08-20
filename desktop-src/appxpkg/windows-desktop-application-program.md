---
title: Programma per applicazioni desktop di Windows
description: È possibile ottenere dati di telemetria dettagliati e report di analisi che consentono di visualizzare le prestazioni delle applicazioni desktop Windows tramite il nuovo programma Windows Desktop Application Program.
ms.assetid: F1ED72A5-E1CD-4924-A81B-ED6FAF5E2AA3
ms.topic: article
ms.date: 11/02/2018
ms.openlocfilehash: 90483194654d5656060c57e3ad7593410a08660c2b8fc71bbbe9e42f08f17c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105729"
---
# <a name="windows-desktop-application-program"></a>Programma per applicazioni desktop di Windows

È possibile ottenere dati di telemetria dettagliati e report di analisi che consentono di visualizzare le prestazioni delle applicazioni desktop Windows tramite il nuovo programma Windows Desktop Application Program.

Non è necessario effettuare l'iscrizione e accettare [](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3deJsPaLaK4fU55nKvN21CjU6FsdJ0aPGfhsjGAZ0HR9bE6rgwHHX4izvRt_w-0VUlIF0ClCya4cVY6Uv4qTAqDrH8LTwFpjFGWVW2BAIJmAAuxBLZGTPS_DYy0wwgvTh1orWTCMvBdlOu_kF8vwNe4mjtk9JRMvYaETyspKrJi-s5Z2K7lKIPqnlFkwSU-aoot-3NxTeQ0wu6_RJ1nf_kLFatEkVAqokDSYTKkpv7zF6gA3YYriMFoC9_f2uxuXpI-STckg&nonce=637177463062493881.YjhiOTZjYTMtOTVhZS00OGM1LWI4MDItNWE5MThjMjA1ZjZmMTAyZDRiMGQtMDJhNC00ZDJmLWFkM2QtM2FjZDJkNjcxYWQy&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) il Contratto del programma per applicazioni desktop di [Windows,](https://go.microsoft.com/fwlink/?linkid=853677)quindi caricare un file firmato usando lo stesso certificato usato per firmare i file eseguibili dell'applicazione.

## <a name="join-the-windows-desktop-application-program"></a>Partecipare al programma Windows Desktop Application Program

Se l'azienda ha già un **account Partner Center:** accedere all'account Partner Center (usando il account Microsoft associato al proprietario  dell'account) e passare alla pagina Programmi (in **Impostazioni account** o selezionando **Tutti** nel menu di spostamento a sinistra). In **Windows Desktop Application Program** fare clic **Informazioni di base** per partecipare al programma senza costi aggiuntivi. Se si dispone di Azure AD tenant associato all'account Partner Center, gli utenti aggiunti potranno accedere al programma Windows Desktop Application Program. Presto disponibili, sarà possibile impostare un accesso più granulare per questo programma.

> [!Tip]  
> Se la società ha un account Partner Center, ma non si ha accesso ad esso, chiedere all'amministratore di aggiungere l'utente [come utente](/windows/uwp/publish/add-users-groups-and-azure-ad-applications). Si noti che solo il proprietario dell'account può partecipare al Windows applicazione desktop.

 

**Se l'azienda non ha** un account Partner Center: è possibile iscriversi al programma [Windows Desktop Application Program](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3dWc5R_wIKVD0EbOy2UUxS0_0GQJnIAbD-eisMn7Gb4cJL18fRdelvbtj5_R0zoGlsebcnAxIvwKS5kx4Ma4mLMbU4l9ULsE9ajiZU4wtchLJXyJGsPCjCBUNV7TY1SzwXAI-LepSoXkqa8xSywVb7JZ3Xed-Lcw-kwEShFOwt0SdSdc1nNevHbPOhotOeFQcqbo0HESVYXk6pZORJ_OYimG99onp_zSTyludOvvaTd9GYKUgX9exCU5IHReP7MzJDHOgqTg&nonce=637177463071243612.NDU4MjE2ZTMtNmVkMi00YWNiLWEzZGEtMjYyNDRkODI0M2FmOTM3MmE1NzgtMzQ1OC00M2ZkLWJhMDktYzI4YTNhNzdiYTk0&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) direttamente senza costi aggiuntivi. Presto disponibili, è possibile associare un [tenant Azure AD all'account](/windows/uwp/publish/add-users-groups-and-azure-ad-applications) in modo che anche altri utenti dell'azienda possano eseguire l'accesso.

## <a name="add-your-desktop-applications"></a>Aggiungere le applicazioni desktop

Dopo aver aggiunto il programma, è necessario aggiungere le applicazioni desktop Windows al dashboard in modo da poter iniziare a visualizzare i report di analisi.

La firma del codice viene utilizzata per stabilire l'identità dell'azienda e recuperare le analisi per le app pubblicate.

Verrà fornito un file e verrà chiesto di firmarlo con gli stessi certificati di firma del codice validi, non scaduti e non revocati che si usano per firmare le applicazioni desktop. Successivamente, il file firmato verrà caricato nel dashboard. In questo modo è possibile sapere che tutte le applicazioni desktop firmate con lo stesso certificato appartengono all'account. Le informazioni sul certificato non vengono usate per altri scopi.

> [!Important]  
> Non è necessario ripetere questo processo se si rilascia una nuova applicazione desktop. Dopo aver caricato il file firmato, verranno identificate automaticamente tutte le nuove applicazioni firmate con lo stesso certificato e verranno recuperate automaticamente le analisi per tali prodotti. Non è inoltre necessario distribuire il file fornito all'interno delle applicazioni o inviare alcun tipo di mapping per i prodotti

 

**Per aggiungere una o più applicazioni desktop**

1.  Nel dashboard selezionare Aggiungi **applicazioni desktop.**
2.  Nella pagina successiva scaricare il file firmabile selezionando **Scarica il file** e quindi salvare il file nel computer.
3.  Firmare il file appena scaricato usando lo stesso certificato di firma del codice che si usa per autenticare le applicazioni desktop. È possibile usare SignTool.exe (disponibile in Microsoft Visual Studio e come parte di [Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)) per firmare questo file. Altre informazioni su questo processo sono descritte di seguito.
4.  Upload il file appena firmato trascinandolo nel campo (oppure fare clic per sfogliare i file).
5.  Selezionare **Invia** per completare il processo.

![procedura per aggiungere applicazioni desktop](images/uploadcert.png)

Se si usano più certificati di firma del codice, è possibile ripetere i passaggi precedenti per ognuno dei certificati. È possibile scaricare, firmare e caricare un file per ogni certificato corrente utilizzato per firmare le applicazioni. Tuttavia, è possibile usare un solo certificato per ogni file scaricato.

Dopo aver completato questi passaggi, verranno identificate le applicazioni desktop Windows firmate con lo stesso certificato usato per firmare il file. Nella maggior parte dei casi, i report analitici verranno visualizzati entro 48 ore, anche se in alcuni casi può richiedere più tempo.

## <a name="use-signtoolexe-to-sign-the-downloaded-file"></a>Usare signtool.exe per firmare il file scaricato

Microsoft offre uno strumento per firmare file, SignTool.exe, con Visual Studio e in [Windows SDK.](https://developer.microsoft.com/windows/downloads/windows-10-sdk) È possibile usare questo strumento per eseguire e verificare il processo di firma del codice. Altre informazioni sui SignTool.exe sono disponibili [qui.](/dotnet/framework/tools/signtool-exe)

Ecco due dei modi più comuni per usare questo strumento per firmare il file firmabile.

-   Se si ha accesso al certificato di firma del codice come file [PFX (Personal Information Exchange):](/windows-hardware/drivers/install/personal-information-exchange---pfx--files)

    ``` syntax
    signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin
    ```

    ![Screenshot che mostra una finestra del prompt dei comandi che mostra il comando 'signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin'.](images/signtool2.png)

-   Se il certificato di firma del codice è disponibile nell'archivio certificati locale:

    ``` syntax
    Signtool sign /v /s MY /n CertSubjectName SignableFile.bin
    ```

    ![finestra del prompt dei comandi con questo comando](images/signtool.png)

Dopo aver firmato il file, è possibile verificare che sia stato firmato correttamente con un certificato valido con il codice seguente:

``` syntax
signtool verify /a SignableFile.bin
```

## <a name="viewing-your-analytic-data"></a>Visualizzazione dei dati analitici

Dopo aver caricato i file firmati e aver identificato le applicazioni desktop, il dashboard mostrerà una panoramica delle applicazioni insieme alle metriche chiave.

I dati di telemetria mostreranno informazioni sull'integrità, ad esempio arresti anomali per ogni applicazione associata al certificato. Il dashboard mostrerà una panoramica delle applicazioni insieme alle metriche chiave. È possibile selezionare qualsiasi applicazione per visualizzarne [il report sull'integrità,](#health-report) [il report](#installs-report)Installa e il [report](#application-blocks-report) Blocchi nel dashboard. È anche possibile [recuperare i dati analitici a livello di codice usando l'API Microsoft Store analytics](#retrieve-analytic-data-using-the-microsoft-store-analytics-api).

> [!Note]  
> Se si rileva che i metadati di un'applicazione sono stati aggiornati per l'uso di un nuovo nome, si inizierà a segnalare nuovi dati con il nuovo nome. I dati cronologici associati al nome precedente verranno conservati per 30 giorni.
> 
> Analisi non sarà disponibile per un'applicazione fino a quando non è stata installata in almeno 100 dispositivi.


### <a name="health-report"></a>Report Integrità

Il  report sull'integrità consente di ottenere dati relativi alle prestazioni e alla qualità dell'app, inclusi arresti anomali ed eventi che non rispondono. Se applicabile, è possibile visualizzare le analisi dello stack e/o i file CAB per un ulteriore debug.

![report di integrità - Programma per applicazioni desktop di Windows](images/health.png)

È possibile filtrare i dati in diversi modi, consentendo di:

-   Visualizzare un riepilogo di tutti i tipi di errore, ordinati in base al numero di riscontri
-   Eseguire il drill-down in un errore specifico e scaricare le analisi dello stack per eseguire più rapidamente il debug del problema
-   Confrontare una nuova versione dell'applicazione con le versioni precedenti
-   Visualizzare i dati di integrità in aggregazione o in base all'area, consentendo di isolare i problemi specifici di un'area
-   Confrontare le prestazioni delle applicazioni desktop Windows versioni precedenti o in una versione specifica, ad esempio la versione Windows 10 recente
-   Visualizzare le informazioni sull'integrità per un particolare file eseguibile incluso nell'applicazione

Selezionare **Upload simboli nella** parte superiore della tabella **Errori** per caricare un file .zip contenente i file di simboli [dell'applicazione.](/windows-hardware/drivers/debugger/symbols-and-symbol-files) Questi file di simboli verranno indicizzati e usati per produrre analisi dello stack più accurate. I tipi di file di simboli .zip devono essere pdb, .dll o .exe. Dopo aver caricato correttamente il file .zip, dovrebbe essere visualizzato un minor numero **di ! Valori** sconosciuti per i nuovi errori nell'elenco degli errori dell'applicazione in circa 5 giorni.

### <a name="installs-report"></a>Installa il report

Il report **Installazioni** consente di visualizzare il numero di dispositivi in cui è stata installata un'applicazione per un determinato giorno e il numero medio di dispositivi in cui è stata installata ogni versione dell'applicazione negli ultimi 30 giorni.

È possibile filtrare i dati in diversi modi, consentendo di:

-   Visualizzare un riepilogo delle installazioni, ordinate in base alla popolarità
-   Confrontare una nuova versione dell'applicazione con le versioni precedenti
-   Visualizzare i dati di installazione in aggregazione o per area
-   Confrontare le prestazioni delle applicazioni desktop Windows versioni di Windows o in una versione specifica, ad esempio la versione più recente Windows 10 o versioni Windows Circuito Insider veloce e le versioni lente

### <a name="application-blocks-report"></a>Report blocchi applicazione

Il report **Blocchi applicazione** consente di visualizzare informazioni sui dispositivi Windows 10 su cui l'applicazione influisce Windows 10 aggiornamenti. È possibile visualizzare il numero di dispositivi che sono stati influenzati in un determinato giorno insieme al numero medio di dispositivi negli ultimi 30 giorni.

I tipi di blocchi di aggiornamento inclusi sono i seguenti: 

<table>
<tr><th>Category</th><th>Problema</th><th>Descrizione</th><th>Indicazioni fornite agli utenti</th></tr>
<tr><td>Potenziale potenziale</td><td>Blocca l'aggiornamento</td><td>L'applicazione non funzionerà con la nuova versione del sistema operativo. L'azione dell'utente è necessaria durante l'installazione per procedere con l'aggiornamento.</td><td>Rimuovere l'applicazione prima dell'aggiornamento e verificare con lo sviluppatore se è disponibile una versione compatibile dell'applicazione.</td></tr>
<tr><td>Temporary temporaneo</td><td>Può bloccare l'aggiornamento. È necessario testare l'applicazione.</td><td>Microsoft sta esaminando i problemi di aggiornamento correlati a questa applicazione. L'aggiornamento non verrà eseguito per gli utenti che potrebbero essere influenzati.</td><td>Rimuovere l'applicazione prima dell'aggiornamento e verificare con lo sviluppatore se è disponibile una versione compatibile dell'applicazione.</td></tr>
<tr><td>Notifica di runtime</td><td>Potrebbe non funzionare correttamente nella nuova versione del sistema operativo, ma non blocerà l'aggiornamento</td><td>L'applicazione non impedirà l'aggiornamento, ma sono stati rilevati problemi che potrebbero impedirne il corretto funzionamento nella nuova versione del sistema operativo.</td><td>Non è necessaria alcuna azione per continuare l'aggiornamento, ma assicurarsi di testare l'applicazione nella nuova versione del sistema operativo e di verificare con lo sviluppatore una versione compatibile, se necessario.</td></tr>
</table>

### <a name="retrieve-analytic-data-using-the-microsoft-store-analytics-api"></a>Recuperare dati analitici usando l'API Microsoft Store analytics

L Microsoft Store API di analisi dei dati consente di recuperare a livello di codice i dati di analisi per le applicazioni aggiunte all'account.

Questa API offre i metodi seguenti specifici per il Windows applicazione desktop:

-   [Installa](/windows/uwp/monetize/get-desktop-app-installs)
-   [Riscontri di errore](/windows/uwp/monetize/get-desktop-application-error-reporting-data)
-   [Dettagli dell'errore](/windows/uwp/monetize/get-details-for-an-error-in-your-desktop-application)
-   [Analisi dello stack](/windows/uwp/monetize/get-the-stack-trace-for-an-error-in-your-desktop-application)
-   [File CAB](/windows/uwp/monetize/download-the-cab-file-for-an-error-in-your-desktop-application)
-   [Blocchi di aggiornamento](/windows/uwp/monetize/get-desktop-block-data)
-   [Dettagli del blocco di aggiornamento](/windows/uwp/monetize/get-desktop-block-data-details)


Per altre informazioni sull'uso di questa API, vedere [Accedere ai dati analitici usando i servizi dello Store.](/windows/uwp/monetize/access-analytics-data-using-windows-store-services)

## <a name="managing-your-desktop-application-metadata"></a>Gestione dei metadati dell'applicazione desktop

Per dedurre i raggruppamenti logici dei file eseguibili nelle applicazioni vengono utilizzati i metadati nome file, versione del file, nome del prodotto e versione del prodotto nei file eseguibili. Se i file eseguibili non hanno metadati accurati, possono essere visualizzati insieme in un nome di applicazione sconosciuto oppure il nome dell'applicazione verrà utilizzato per impostazione predefinita per il nome del singolo eseguibile. 

Mantenere aggiornati i metadati delle app e dei file consente di assicurarsi che siano rappresentati correttamente nel dashboard. Di seguito sono elencati alcuni suggerimenti:

-   Usare il certificato per firmare ogni file eseguibile che si vuole visualizzare nel report di analisi, non solo i file eseguibili di installazione.
-   Fornire informazioni coerenti sul nome del prodotto e sulla versione del prodotto per tutti i file eseguibili che appartengono alla stessa applicazione (ad esempio, *Applicazione ).* Se alcuni dei file eseguibili vengono distribuiti con più applicazioni, assegnare loro nomi univoci (ad *esempio,* Componenti condivisi ) in modo che sia possibile visualizzare l'analisi per tali file eseguibili separatamente dalle applicazioni con cui sono stati distribuiti.
-   Ogni volta che si apportano modifiche ai metadati, è possibile che nel dashboard venga visualizzata una nuova voce per l'applicazione. Se si apporta una modifica, i nuovi dati di telemetria in ingresso rifletteranno le modifiche, ma i dati di telemetria precedente verranno comunque visualizzati come **applicazione** sconosciuta.
-   Quando si rivede un file, assicurarsi di aggiornare la versione dell'applicazione e i numeri di versione del prodotto.
    > [!Tip]  
    > Usare [**le risorse VERSIONINFO**](/windows/desktop/menurc/versioninfo-resource) per impostare **FileDescription**, **FileVersion**, **ProductName** e **ProductVersion** per i file e le applicazioni. L'esempio seguente definisce una **risorsa VERSIONINFO:**
    >
    > ``` syntax
    > #define VER_PRODUCTNAME_STR      "Sample App"
    > #define VER_PRODUCTVERSION       3,10,349,0
    > #define VER_PRODUCTVERSION_STR   "3.10.349.0\0"
    > #define VER_FILEDESCRIPTION_STR  "Sample File"
    > #define VER_FILEVERSION          3,10,349,0
    > #define VER_FILEVERSION_STR      "3.10.349.0\0"
    > #define VER_COMPANYNAME_STR     "XYZ Corp."
    > #define VER_LEGALCOPYRIGHT_STR   "Copyright \251 XYZ Corp." 
    >  
    > VS_VERSION_INFO VERSIONINFO
    > FILEVERSION VER_FILEVERSION
    > PRODUCTVERSION VER_PRODUCTVERSION
    > FILEFLAGSMASK VER_FILEFLAGSMASK
    > FILEFLAGS VER_FILEFLAGS
    > FILEOS VER_FILEOS
    > FILETYPE VER_FILETYPE
    > FILESUBTYPE VER_FILESUBTYPE
    > BEGIN
    >     BLOCK "StringFileInfo"
    >     BEGIN
    >         BLOCK "040904E4"
    >         BEGIN
    >             VALUE "ProductName",      VER_PRODUCTNAME_STR
    >             VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
    >             VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
    >             VALUE "FileVersion",      VER_FILEVERSION_STR
    >             VALUE "CompanyName",      VER_COMPANYNAME_STR
    >             VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
    >         END
    >     END
    >      
    > END 
    > ```

     

## <a name="add-and-manage-account-users"></a>Aggiungere e gestire gli utenti dell'account

È possibile usare Azure Active Directory per aggiungere e gestire altri utenti nell'account Windows Desktop Application Program. È possibile aggiungere singoli utenti, gruppi di utenti o Azure AD applicazioni, offrendo a ognuno un ruolo predefinito (Manager o Sviluppatore).

### <a name="associate-azure-active-directory-with-your-account"></a>Associare Azure Active Directory all'account

Per aggiungere e gestire gli utenti dell'account, è prima necessario associare l'account all'account dell'Azure Active Directory. Se la tua organizzazione usa già Office 365 o altri servizi aziendali Microsoft, hai già Azure AD. In caso contrario, è possibile creare un nuovo tenant Azure AD senza costi aggiuntivi.

Per altre Azure Active Directory, vedere [Associare Azure Active Directory'account Partner Center personale.](/windows/uwp/publish/associate-azure-ad-with-dev-center) Anche se l'argomento è in Windows per sviluppatori di app, l'associazione di un tenant funziona allo stesso modo per il Windows di applicazioni desktop.

### <a name="add-users-groups-and-azure-ad-applications-to-your-account"></a>Aggiungere utenti, gruppi e Azure AD applicazioni all'account

Dopo aver configurato l'associazione Azure AD, è possibile aggiungere utenti selezionando la sezione Utenti in Impostazioni account. A ogni utente viene assegnato un ruolo che definisce l'accesso all'account. È anche possibile aggiungere gruppi di utenti e Azure AD applicazioni per concedere loro l'accesso all'account Partner Center personale. Per altre informazioni sull'aggiunta di utenti, vedere [Aggiungere utenti, gruppi Azure AD applicazioni](/windows/uwp/publish/add-users-groups-and-azure-ad-applications).

A ogni utente, gruppo o Azure AD'applicazione aggiunta all'account deve essere assegnato un ruolo. Questo processo è descritto in [Impostare ruoli o autorizzazioni personalizzate per gli utenti dell'account.](/windows/uwp/publish/set-custom-permissions-for-account-users) Si noti tuttavia che per il programma Windows Desktop Application Program, non è possibile assegnare autorizzazioni personalizzate o limitare l'accesso in base al prodotto. A ogni utente deve invece essere assegnato uno dei ruoli standard seguenti.



| Ruolo      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manager   | Può caricare e rimuovere certificati e può visualizzare tutti i dati analitici. Ha accesso completo all'account, ad eccezione della modifica delle informazioni finanziarie. Ciò include la gestione degli utenti, ma si noti che la possibilità di creare ed eliminare utenti nel tenant di Azure AD dipende dall'autorizzazione dell'account in Azure AD. Ovvero, se a un utente è assegnato il ruolo Manager, ma non dispone delle autorizzazioni di amministratore globale nell'Azure AD dell'organizzazione, non sarà in grado di creare nuovi utenti o eliminare utenti dalla directory (anche se possono modificare il ruolo account di un utente).<br/> Si noti che se l'account è associato a più tenant di Azure AD, un manager non può visualizzare i dettagli completi per un utente (inclusi nome, cognome, indirizzo di posta elettronica per il ripristino della password e se è un amministratore globale di Azure AD) a meno che non abbia eseguito l'accesso allo stesso tenant dell'utente con un account con autorizzazioni di amministratore globale per tale tenant. Tuttavia, possono aggiungere e rimuovere utenti in qualsiasi tenant associato all'account. <br/> |
| Sviluppatore | Può visualizzare le applicazioni e i dettagli del certificato associati all'account e può visualizzare il report **Integrità** **e installazioni.** Non è possibile visualizzare le informazioni finanziarie o le impostazioni dell'account.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="faq"></a>Domande frequenti

-   **Perché non vengono visualizzati dati per un'applicazione?** I dati non vengono visualizzati finché non viene rilevato un numero sufficiente di utenti per raccogliere informazioni significative. Se l'applicazione è stata appena rilasciata, potrebbe essere necessario del tempo per raggiungere questa soglia minima di adozione. Un altro motivo per cui i dati potrebbero non essere visualizzati è se non è stato firmato un file con il certificato per una determinata applicazione. Assicurarsi di caricare i file firmati con ogni certificato utilizzato per firmare le applicazioni.
-   **È possibile accedere a questi dati tramite un'API?** Sì, i dati verranno resi disponibili tramite un'API pubblica quando il programma sarà disponibile per tutti gli sviluppatori.
-   **E per quanto riguarda le applicazioni con certificati meno recenti?** Sfortunatamente, microsoft non supporta l'invio di certificati scaduti o revocati, anche se vengono rinnovati con la stessa chiave.
-   **Perché viene visualizzata un'applicazione non riconosciuta?** Se il certificato usato per firmare i file nell'applicazione viene usato anche da un altro utente dell'azienda per firmare un'altra applicazione, verranno visualizzati anche i dati di telemetria per tale applicazione. In futuro, sarà disponibile un'opzione per nascondere le applicazioni dal dashboard. Se l'account aziendale è collegato a un tenant Azure AD, è possibile richiedere all'amministratore di modificare le autorizzazioni utente in modo che siano visibili all'utente solo applicazioni specifiche.
-   **Come è possibile inviare commenti e suggerimenti sull'esperienza o ottenere supporto?** Se è necessaria assistenza, è possibile creare una richiesta di supporto [qui](https://developer.microsoft.com/windows/support/). Per condividere il feedback, usare il **collegamento Commenti e** suggerimenti (in Impostazioni **account)** e selezionare l'area  Analisi per inviare commenti e suggerimenti. 
 

