---
title: Programma per applicazioni desktop di Windows
description: È possibile ottenere dati di telemetria dettagliati e report di analisi che consentono di vedere come le applicazioni desktop di Windows eseguono il nuovo programma applicazione desktop di Windows.
ms.assetid: F1ED72A5-E1CD-4924-A81B-ED6FAF5E2AA3
ms.topic: article
ms.date: 11/02/2018
ms.openlocfilehash: 2dc255c9c8696bd57198f50fc2c570f59c4ae603
ms.sourcegitcommit: 0bfbb2324081644171495734f0609335173745ef
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/25/2021
ms.locfileid: "106333995"
---
# <a name="windows-desktop-application-program"></a>Programma per applicazioni desktop di Windows

È possibile ottenere dati di telemetria dettagliati e report di analisi che consentono di vedere come le applicazioni desktop di Windows eseguono il nuovo programma applicazione desktop di Windows.

Non sono previsti addebiti per accedere a questi dati, ma è sufficiente [iscriversi](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3deJsPaLaK4fU55nKvN21CjU6FsdJ0aPGfhsjGAZ0HR9bE6rgwHHX4izvRt_w-0VUlIF0ClCya4cVY6Uv4qTAqDrH8LTwFpjFGWVW2BAIJmAAuxBLZGTPS_DYy0wwgvTh1orWTCMvBdlOu_kF8vwNe4mjtk9JRMvYaETyspKrJi-s5Z2K7lKIPqnlFkwSU-aoot-3NxTeQ0wu6_RJ1nf_kLFatEkVAqokDSYTKkpv7zF6gA3YYriMFoC9_f2uxuXpI-STckg&nonce=637177463062493881.YjhiOTZjYTMtOTVhZS00OGM1LWI4MDItNWE5MThjMjA1ZjZmMTAyZDRiMGQtMDJhNC00ZDJmLWFkM2QtM2FjZDJkNjcxYWQy&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) e accettare il [contratto del programma applicativo desktop di Windows](https://go.microsoft.com/fwlink/?linkid=853677), quindi caricare un file firmato usando lo stesso certificato usato per firmare i file eseguibili dell'applicazione.

## <a name="join-the-windows-desktop-application-program"></a>Partecipa al programma applicazione desktop di Windows

**Se la società ha già un account del centro** per i partner: accedere all'account del centro per i partner (usando il account Microsoft associato al proprietario dell'account) e passare alla pagina **programmi** (in **Impostazioni account** o selezionando **tutto** nel menu di spostamento a sinistra). In **programma applicazione desktop di Windows** fare **clic su inizia a** partecipare al programma senza costi aggiuntivi. Se si dispone di un tenant di Azure AD associato all'account del centro per i partner, gli utenti aggiunti saranno in grado di accedere al programma applicazione desktop di Windows. Presto sarà possibile impostare un accesso più granulare per questo programma.

> [!Tip]  
> Se la società dispone di un account del centro per i partner, ma non è possibile accedervi, chiedere all'amministratore di [aggiungerlo come utente](/windows/uwp/publish/add-users-groups-and-azure-ad-applications). Si noti che solo il proprietario dell'account può partecipare al programma applicazione desktop di Windows.

 

**Se la società non dispone di un account del centro** per i partner, è possibile [iscriversi gratuitamente al programma applicazioni desktop di Windows](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3dWc5R_wIKVD0EbOy2UUxS0_0GQJnIAbD-eisMn7Gb4cJL18fRdelvbtj5_R0zoGlsebcnAxIvwKS5kx4Ma4mLMbU4l9ULsE9ajiZU4wtchLJXyJGsPCjCBUNV7TY1SzwXAI-LepSoXkqa8xSywVb7JZ3Xed-Lcw-kwEShFOwt0SdSdc1nNevHbPOhotOeFQcqbo0HESVYXk6pZORJ_OYimG99onp_zSTyludOvvaTd9GYKUgX9exCU5IHReP7MzJDHOgqTg&nonce=637177463071243612.NDU4MjE2ZTMtNmVkMi00YWNiLWEzZGEtMjYyNDRkODI0M2FmOTM3MmE1NzgtMzQ1OC00M2ZkLWJhMDktYzI4YTNhNzdiYTk0&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) . Presto sarà disponibile l'opzione per [associare un tenant Azure ad al proprio account](/windows/uwp/publish/add-users-groups-and-azure-ad-applications) , in modo che anche altri utenti dell'azienda possano effettuare l'accesso.

## <a name="add-your-desktop-applications"></a>Aggiungere le applicazioni desktop

Una volta aggiunto il programma, è necessario aggiungere le applicazioni desktop di Windows al dashboard in modo che sia possibile iniziare a visualizzare i report di analisi.

Usiamo la firma del codice per stabilire l'identità aziendale e recuperare le analisi per le app pubblicate.

Verrà fornito un file e verrà chiesto di firmarlo con gli stessi certificati di firma del codice non revocati, validi e non scaduti, usati per firmare le applicazioni desktop. Successivamente, si caricherà il file firmato nel dashboard. In questo modo è possibile verificare che le applicazioni desktop firmate con lo stesso certificato appartengano al proprio account. Le informazioni sul certificato non vengono utilizzate per altri scopi.

> [!Important]  
> Non è necessario ripetere questo processo se si rilascia una nuova applicazione desktop. Una volta caricato il file firmato, verranno automaticamente identificate tutte le nuove applicazioni firmate con lo stesso certificato e verranno recuperate automaticamente le analisi per tali prodotti. Non è inoltre necessario distribuire il file specificato all'interno delle applicazioni o inviare qualsiasi tipo di mapping per i prodotti

 

**Per aggiungere una o più applicazioni desktop**

1.  Dal Dashboard selezionare **Aggiungi applicazioni desktop**.
2.  Nella pagina successiva scaricare il file firmabile selezionando **Scarica il file** e quindi salvare il file nel computer.
3.  Firmare il file appena scaricato usando lo stesso certificato di firma codice usato per autenticare le applicazioni desktop. Per firmare il file, è possibile usare SignTool.exe (disponibile in Microsoft Visual Studio e come parte del [Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)). Altre informazioni su questo processo sono descritte di seguito.
4.  Caricare il file appena firmato trascinandolo nel campo oppure fare clic per sfogliare i file.
5.  Selezionare **Submit (Invia** ) per completare il processo.

![passaggi per l'aggiunta di applicazioni desktop](images/uploadcert.png)

Se si usa più di un certificato di firma codice, è possibile ripetere i passaggi precedenti per ogni certificato. È possibile scaricare, firmare e caricare un file per ogni certificato corrente usato per firmare le applicazioni. Tuttavia, è possibile utilizzare un solo certificato per ogni file scaricato.

Dopo aver completato questi passaggi, si identificherà quali applicazioni desktop di Windows sono firmate con lo stesso certificato usato per firmare il file. Nella maggior parte dei casi, si inizierà a visualizzare i report analitici entro 48 ore, anche se talvolta può richiedere un po' più di tempo.

## <a name="use-signtoolexe-to-sign-the-downloaded-file"></a>Usare signtool.exe per firmare il file scaricato

Microsoft fornisce uno strumento per la firma di file, SignTool.exe con Visual Studio e nel [Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk). È possibile utilizzare questo strumento per eseguire e verificare il processo di firma del codice. Altre informazioni su SignTool.exe sono disponibili [qui](/dotnet/framework/tools/signtool-exe).

Ecco due dei modi più comuni per usare questo strumento per firmare il file firmabile.

-   Se si dispone dell'accesso al certificato di firma codice come file [pfx (Personal Information Exchange)](/windows-hardware/drivers/install/personal-information-exchange---pfx--files) :

    ``` syntax
    signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin
    ```

    ![Screenshot che mostra una finestra del prompt dei comandi che mostra il comando ' signtool sign/f My cert. pfx/p MyCertPassword/v SignableFile. bin '.](images/signtool2.png)

-   Se il certificato di firma codice è disponibile nell'archivio certificati locale:

    ``` syntax
    Signtool sign /v /s MY /n CertSubjectName SignableFile.bin
    ```

    ![finestra del prompt dei comandi che mostra questo comando](images/signtool.png)

Dopo aver firmato il file, è possibile verificare che sia stato firmato correttamente con un certificato valido con il codice seguente:

``` syntax
signtool verify /a SignableFile.bin
```

## <a name="viewing-your-analytic-data"></a>Visualizzazione dei dati analitici

Dopo aver caricato i file firmati e aver identificato le applicazioni desktop, il dashboard visualizzerà una panoramica delle applicazioni insieme alle metriche chiave.

I dati di telemetria mostreranno informazioni di integrità, ad esempio arresti anomali per ogni applicazione associata al certificato. Il dashboard visualizzerà una panoramica delle applicazioni insieme alle metriche chiave. È possibile selezionare qualsiasi applicazione per visualizzare il [rapporto di stato](#health-report), [installare il report](#installs-report)e [bloccare il report](#application-blocks-report) nel dashboard. È anche possibile [recuperare i dati analitici a livello di codice usando l'API Microsoft Store Analytics](#retrieve-analytic-data-using-the-microsoft-store-analytics-api).

> [!Note]  
> Se si rileva che i metadati di un'applicazione sono stati aggiornati per usare un nuovo nome, si inizierà a segnalare nuovi dati con il nuovo nome. I dati cronologici associati al nome precedente verranno conservati per 30 giorni.
> 
> Analytics non sarà disponibile per un'applicazione fino a quando non sarà installato in almeno 100 dispositivi.


### <a name="health-report"></a>Report Integrità

Il report sull' **integrità** consente di ottenere i dati relativi alle prestazioni e alla qualità dell'applicazione, inclusi gli arresti anomali e gli eventi che non rispondono. Se applicabile, è possibile visualizzare le tracce dello stack e/o i file CAB per eseguire ulteriori operazioni di debug.

![rapporto di stato-programma applicazione desktop di Windows](images/health.png)

È possibile filtrare i dati in diversi modi, consentendo di:

-   Visualizza un riepilogo di tutti i tipi di errore, ordinati in base al numero di riscontri
-   Eseguire il drill-down in un particolare errore e scaricare le analisi dello stack per eseguire il debug del problema più velocemente
-   Confrontare una nuova versione dell'applicazione con le versioni precedenti
-   Visualizzare i dati di integrità in aggregazione o in base all'area, consentendo di isolare i problemi specifici di un'area
-   Confrontare le prestazioni delle applicazioni desktop nelle versioni di Windows o in una versione specifica, ad esempio la versione più recente di Windows 10
-   Visualizza le informazioni sull'integrità per un file eseguibile specifico incluso nell'applicazione

Selezionare **carica i simboli** nella parte superiore della tabella degli **errori** per caricare un file con estensione zip contenente i [file di simboli](http:/docs.microsoft.com/windows-hardware/drivers/debugger/symbols-and-symbol-files)dell'applicazione. Questi file di simboli verranno indicizzati e utilizzati per produrre tracce dello stack più accurate. I tipi di file di simboli nel file con estensione zip devono essere PDB, dll o exe. Al termine del caricamento del file con estensione zip, verrà **visualizzato un numero minore. Valori sconosciuti** per i nuovi errori nell'elenco degli errori dell'applicazione in circa 5 giorni.

### <a name="installs-report"></a>Installa il report

Il report **installazioni** consente di visualizzare il numero di dispositivi in cui un'applicazione è stata installata per un determinato giorno e il numero medio di dispositivi in cui è stata installata la versione di ogni applicazione negli ultimi 30 giorni.

È possibile filtrare i dati in diversi modi, consentendo di:

-   Visualizza un riepilogo delle installazioni, ordinate in base alla popolarità
-   Confrontare una nuova versione dell'applicazione con le versioni precedenti
-   Visualizza i dati di installazione in aggregazione o in base all'area
-   Confrontare le prestazioni delle applicazioni desktop nelle versioni di Windows o in una versione specifica, ad esempio la versione più recente di Windows 10 o Windows Insider Fast and Slow

### <a name="application-blocks-report"></a>Report blocchi applicazione

Il report **blocchi applicazione** consente di visualizzare informazioni sui dispositivi Windows 10 in cui l'applicazione influisca sugli aggiornamenti di Windows 10. È possibile visualizzare il numero di dispositivi interessati da un determinato giorno insieme al numero medio di dispositivi negli ultimi 30 giorni.

I tipi di blocchi di aggiornamento inclusi sono i seguenti: 

<table>
<tr><th>Category</th><th>Problema</th><th>Descrizione</th><th>Informazioni aggiuntive fornite agli utenti</th></tr>
<tr><td>Sedi potenziali</td><td>Bloccherà l'aggiornamento</td><td>L'applicazione non funzionerà sulla nuova versione di rilascio del sistema operativo. L'azione dell'utente è necessaria durante l'installazione per procedere con l'aggiornamento.</td><td>Rimuovere l'applicazione prima di eseguire l'aggiornamento e verificare con lo sviluppatore una versione compatibile dell'applicazione.</td></tr>
<tr><td>Sedimentazione temporanea</td><td>Può bloccare l'aggiornamento. È necessario testare l'applicazione.</td><td>Microsoft sta esaminando i problemi di aggiornamento correlati a questa applicazione. L'aggiornamento non verrà implementato per gli utenti che potrebbero essere interessati.</td><td>Rimuovere l'applicazione prima di eseguire l'aggiornamento e verificare con lo sviluppatore una versione compatibile dell'applicazione.</td></tr>
<tr><td>Notifica di runtime</td><td>Potrebbe non funzionare correttamente nella nuova versione di rilascio del sistema operativo, ma l'aggiornamento non viene bloccato</td><td>L'applicazione non impedirà l'aggiornamento, ma sono stati rilevati problemi che potrebbero impedire il corretto funzionamento della nuova versione del sistema operativo.</td><td>Per continuare l'aggiornamento, non è necessaria alcuna azione, ma assicurarsi di testare l'applicazione nella nuova versione di rilascio del sistema operativo e di verificare con lo sviluppatore una versione compatibile, se necessario.</td></tr>
</table>

### <a name="retrieve-analytic-data-using-the-microsoft-store-analytics-api"></a>Recuperare i dati analitici usando l'API Microsoft Store Analytics

L'API Microsoft Store Analytics consente di recuperare a livello di codice i dati di analisi per le applicazioni aggiunte al proprio account.

Questa API offre i seguenti metodi specifici per il programma applicazione desktop di Windows:

-   [Installa](/windows/uwp/monetize/get-desktop-app-installs)
-   [Riscontri errori](/windows/uwp/monetize/get-desktop-application-error-reporting-data)
-   [Dettagli errore](/windows/uwp/monetize/get-details-for-an-error-in-your-desktop-application)
-   [Analisi dello stack](/windows/uwp/monetize/get-the-stack-trace-for-an-error-in-your-desktop-application)
-   [File CAB](/windows/uwp/monetize/download-the-cab-file-for-an-error-in-your-desktop-application)
-   [Blocchi di aggiornamento](/windows/uwp/monetize/get-desktop-block-data)
-   [Dettagli blocco aggiornamento](/windows/uwp/monetize/get-desktop-block-data-details)


Per altre informazioni sull'uso di questa API, vedere [accedere ai dati analitici usando i servizi di archiviazione](/windows/uwp/monetize/access-analytics-data-using-windows-store-services).

## <a name="managing-your-desktop-application-metadata"></a>Gestione dei metadati dell'applicazione desktop

Il nome file, la versione del file, il nome del prodotto e i metadati della versione del prodotto nei file eseguibili vengono utilizzati per dedurre i raggruppamenti logici di file eseguibili in applicazioni. Se i file eseguibili non hanno metadati accurati, possono essere visualizzati insieme con un nome di applicazione **sconosciuto** oppure il nome dell'applicazione verrà utilizzato per impostazione predefinita per il singolo nome eseguibile.

Mantenere aggiornati i metadati delle app e dei file consente di verificare che siano rappresentati correttamente nel dashboard. Di seguito sono elencati alcuni suggerimenti:

-   Usare il certificato per firmare tutti i file eseguibili che si desidera visualizzare nel report di analisi, non solo i file eseguibili di installazione.
-   Fornire informazioni sul nome del prodotto e sulla versione del prodotto coerenti per tutti i file eseguibili che appartengono alla stessa applicazione, ad esempio l' *applicazione*. Se alcuni file eseguibili sono distribuiti con più applicazioni, assegnare loro nomi univoci (ad esempio, *componenti condivisi*), in modo che sia possibile visualizzare le analisi per tali eseguibili separatamente dalle applicazioni con cui sono state distribuite.
-   Ogni volta che si apportano modifiche ai metadati, potrebbe essere visualizzata una nuova voce per l'applicazione nel dashboard. In caso di modifica, i nuovi dati di telemetria in ingresso rifletteranno le modifiche, ma i dati di telemetria precedenti verranno comunque visualizzati come applicazione **sconosciuta** .
-   Quando si modifica un file, assicurarsi di aggiornare la versione dell'applicazione e i numeri di versione del prodotto.
    > [!Tip]  
    > Usare le risorse di [**VERSIONINFO**](/windows/desktop/menurc/versioninfo-resource) per impostare **FileDescription**, **fileversion**, **ProductName** e **ProductVersion** per i file e le applicazioni. Nell'esempio seguente viene definita una risorsa **VERSIONINFO** :
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

È possibile utilizzare Azure Active Directory per aggiungere e gestire altri utenti nell'account del programma applicativo desktop di Windows. È possibile aggiungere singoli utenti, gruppi di utenti o applicazioni Azure AD, assegnando a ognuno un ruolo predefinito (responsabile o sviluppatore).

### <a name="associate-azure-active-directory-with-your-account"></a>Associa Azure Active Directory al tuo account

Per aggiungere e gestire gli utenti degli account, è innanzitutto necessario associare l'account all'Azure Active Directory dell'organizzazione. Se la tua organizzazione usa già Office 365 o altri servizi aziendali Microsoft, hai già Azure AD. In caso contrario, è possibile creare un nuovo tenant Azure AD senza costi aggiuntivi.

Per altre informazioni, vedere [associare Azure Active Directory all'account del centro per i partner](/windows/uwp/publish/associate-azure-ad-with-dev-center) . Mentre l'argomento è incentrato sul programma per sviluppatori di applicazioni Windows, l'associazione di un tenant funziona allo stesso modo per il programma applicazione desktop di Windows.

### <a name="add-users-groups-and-azure-ad-applications-to-your-account"></a>Aggiungere utenti, gruppi e applicazioni Azure AD all'account

Dopo aver configurato l'associazione di Azure AD, è possibile aggiungere utenti selezionando la sezione utenti in Impostazioni account. A ogni utente viene assegnato un ruolo che definisce l'accesso all'account. È anche possibile aggiungere gruppi di utenti e Azure AD applicazioni per concedere loro l'accesso all'account del centro per i partner. Per altre informazioni sull'aggiunta di utenti, vedere [aggiungere utenti, gruppi e applicazioni Azure ad](/windows/uwp/publish/add-users-groups-and-azure-ad-applications).

A ogni utente, gruppo o applicazione Azure AD aggiunta all'account deve essere assegnato un ruolo. Questo processo è descritto in [impostare i ruoli o le autorizzazioni personalizzate per gli utenti dell'account](/windows/uwp/publish/set-custom-permissions-for-account-users). Si noti, tuttavia, che per il programma applicazione desktop di Windows non è possibile assegnare autorizzazioni personalizzate o limitare l'accesso in base al prodotto. Al contrario, è necessario assegnare a ogni utente uno dei seguenti ruoli standard.



| Ruolo      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manager   | Consente di caricare e rimuovere i certificati e di visualizzare tutti i dati analitici. Ha accesso completo all'account, tranne che per modificare le informazioni finanziarie. Ciò include la gestione degli utenti, ma si noti che la possibilità di creare ed eliminare gli utenti nel tenant di Azure AD dipende dall'autorizzazione dell'account nella Azure AD. Ovvero, se a un utente viene assegnato il ruolo di Manager, ma non dispone delle autorizzazioni di amministratore globale nel Azure AD dell'organizzazione, non sarà in grado di creare nuovi utenti o eliminare utenti dalla directory (sebbene possano modificare il ruolo di un account utente).<br/> Si noti che se l'account è associato a più di un tenant di Azure AD, un responsabile non può visualizzare i dettagli completi per un utente (inclusi nome, cognome, posta elettronica di ripristino della password e se si tratta di un amministratore globale Azure AD), a meno che non abbiano eseguito l'accesso allo stesso tenant dell'utente con un account con autorizzazioni di amministratore globale per il tenant. Tuttavia, possono aggiungere e rimuovere utenti in qualsiasi tenant associato all'account. <br/> |
| Sviluppatore | Consente di visualizzare le applicazioni e i dettagli del certificato associati all'account e di visualizzare l' **integrità** e di **installare** il report. Non è possibile visualizzare le informazioni finanziarie o le impostazioni dell'account.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="faq"></a>Domande frequenti

-   **Perché non vengono visualizzati i dati per un'applicazione?** I dati non verranno visualizzati fino a quando non viene rilevato un numero sufficiente di utenti per raccogliere informazioni significative. Se l'applicazione è stata appena rilasciata, il raggiungimento di questa soglia minima di adozione potrebbe richiedere del tempo. Un altro motivo per cui i dati potrebbero non essere visualizzati è se non è stato firmato un file con il certificato per una determinata applicazione. Assicurarsi di caricare i file firmati con ogni certificato usato per firmare le applicazioni.
-   **È possibile accedere a questi dati tramite un'API?** Sì, i dati saranno resi disponibili tramite un'API pubblica quando il programma è disponibile per tutti gli sviluppatori.
-   **Quali sono le applicazioni con certificati meno recenti?** Sfortunatamente, non è supportato l'invio di certificati scaduti o revocati, anche se vengono rinnovati con la stessa chiave.
-   **Perché viene visualizzata un'applicazione non riconosciuta?** Se il certificato usato per firmare i file nell'applicazione viene usato anche da un altro utente dell'azienda per firmare un'altra applicazione, si vedranno anche i dati di telemetria per l'applicazione. In futuro, verrà fornita un'opzione per nascondere le applicazioni dal dashboard. Se l'account aziendale è associato a un tenant di Azure AD, è possibile richiedere all'amministratore di modificare le autorizzazioni utente in modo che siano visibili solo le applicazioni specifiche.
-   **Come è possibile inviare commenti e suggerimenti sull'esperienza o ottenere assistenza?** Se è necessaria assistenza, è possibile creare una richiesta di supporto [qui](https://developer.microsoft.com/windows/support/). Per condividere i commenti e suggerimenti, usare il collegamento per il **feedback** (in **Impostazioni account**) e selezionare l'area **Analytics** per farci sapere cosa ne pensate. 
 

