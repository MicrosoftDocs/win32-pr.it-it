---
title: Come risolvere gli errori di firma del pacchetto dell'app
description: Un errore di distribuzione dell'app può essere causato da un errore di convalida della firma digitale del pacchetto dell'app. Informazioni su come riconoscere questi errori e su come procedere.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdec41d2d058a48153d6126fea534c1efaf16e16ccabef5d5e940daa73e839a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048949"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Come risolvere gli errori di firma del pacchetto dell'app

Un errore di distribuzione dell'app può essere causato da un errore di convalida della firma digitale del pacchetto dell'app. Informazioni su come riconoscere questi errori e su come procedere.

Quando si distribuisce un'app Windows pacchetto, Windows tenta sempre di convalidare la firma digitale nel pacchetto dell'app. Errori durante la distribuzione del pacchetto del blocco di convalida della firma. Ma il motivo per cui il pacchetto non è stato convalidato potrebbe non essere ovvio. In particolare, se si firmano i pacchetti con certificati privati per i test locali, spesso è necessario gestire anche il trust per tali certificati. Una configurazione non corretta dell'attendibilità del certificato può causare errori di convalida della firma.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Creazione di pacchetti, distribuzione ed query di Windows app](appx-portal.md)
-   [Verifica dell'attendibilità del certificato](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Prerequisiti

-   [Windows registro eventi per diagnosticare](/windows/desktop/WES/windows-event-log) gli errori di installazione.
-   [Attività Certutil per la gestione dei certificati per la](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) manipolazione dell'archivio certificati durante la risoluzione dei problemi

## <a name="instructions"></a>Istruzioni

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Passaggio 1: Esaminare i log eventi per informazioni di diagnostica

A seconda di come si è tentato di distribuire l'app, è possibile che non sia stato ricevuto un codice di errore significativo per l'errore di distribuzione. In questo caso, è in genere possibile ottenere il codice di errore direttamente dai log eventi.

**Per ottenere il codice di errore dai log eventi**

1.  Eseguire **eventvwr.msc**.
2.  Passare a Visualizzatore eventi registri di applicazioni e servizi   >    >    >  **(locali)** Microsoft Windows .
3.  Il primo log da controllare è **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational.**
4.  Gli errori relativi alla distribuzione vengono registrati in **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational.**

    Per gli errori di distribuzione, cercare l'evento di errore più recente 404. Questo evento di errore fornisce il codice di errore e una descrizione del motivo per cui la distribuzione non è riuscita. Se un evento di errore 465 ha preceduto l'evento 404, si è verificato un problema durante l'apertura del pacchetto.

Se non si è verificato l'errore 465, vedere Risoluzione dei problemi generali relativi alla creazione di [pacchetti,](troubleshooting.md)alla distribuzione e alle query Windows applicazioni . In caso contrario, fare riferimento a questa tabella per i codici di errore comuni che possono essere visualizzati nella stringa di errore per l'evento di errore 465:

| Codice di errore | Errore                                 | Descrizione                                                                                                          | Suggerimento                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | ERRORE DURANTE \_ \_ L'INSTALLAZIONE DEL PACCHETTO APERTO NON \_ \_ RIUSCITO | Impossibile aprire il pacchetto dell'app.                                                                                 | Questo errore indica in genere un problema con il pacchetto. È necessario compilare e firmare di nuovo il pacchetto. Per altre informazioni, vedere [Uso di App Packager.](make-appx-package--makeappx-exe-.md) |
| 0x80080205 | APPX \_ E \_ \_ BLOCKMAP NON VALIDO            | Il pacchetto dell'app è stato manomesso o ha una mappa a blocchi non valida.                                                  | Il pacchetto è danneggiato. È necessario compilare e firmare di nuovo il pacchetto. Per altre informazioni, vedere [Uso di App Packager.](make-appx-package--makeappx-exe-.md)                                  |
| 0x800B0004 | ATTENDIBILITÀ \_ E SOGGETTO \_ NON \_ \_ ATTENDIBILE       | Il pacchetto dell'app è stato manomesso.                                                                              | Il contenuto del pacchetto non corrisponde più alla firma digitale. È necessario firmare di nuovo il pacchetto. Per altre informazioni, vedere [Come firmare un pacchetto dell'app usando SignTool.](how-to-sign-a-package-using-signtool.md)  |
| 0x800B0100 | TRUST \_ E \_ NOSIGNATURE                 | Il pacchetto dell'app non è firmato.                                                                                         | È possibile distribuire Windows solo pacchetti di app firmati. Per informazioni sulla firma di un pacchetto dell'app, vedere [Come firmare un pacchetto dell'app usando SignTool.](how-to-sign-a-package-using-signtool.md)                  |
| 0x800B0109 | CERT \_ E RADICE NON \_ \_ ATTENDIBILE              | La catena di certificati usata per firmare il pacchetto dell'app termina con un certificato radice non attendibile.           | Continuare con il passaggio 2 per risolvere i problemi relativi all'attendibilità del certificato.                                                                                                                                                  |
| 0x800B010A | CONCATENAMENTO \_ CERT E \_                     | Non è stato possibile creare alcuna catena di certificati per un'autorità radice attendibile dal certificato usato per firmare il pacchetto dell'app. | Continuare con il passaggio 2 per risolvere i problemi relativi all'attendibilità del certificato.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Passaggio 2: Determinare la catena di certificati usata per firmare il pacchetto dell'app

Per trovare i certificati che il computer locale deve considerare attendibili, è possibile esaminare la catena di certificati per la firma digitale nel pacchetto dell'app.

**Per determinare la catena di certificati**

1.  In Esplora file fare clic con il pulsante destro del mouse sul pacchetto dell'app e scegliere **Proprietà**.
2.  Nella finestra **di** dialogo Proprietà selezionare la **scheda Firme** digitali, che indica anche se la firma può essere convalidata.
3.  Nell'elenco Firma selezionare la firma e quindi fare clic sul **pulsante** Dettagli.
4.  Nella finestra **di dialogo Dettagli firma** digitale fare clic sul pulsante **Visualizza** certificato.
5.  Nella finestra **di dialogo** Certificato selezionare la scheda **Percorso di** certificazione.

Il certificato principale nella catena è il certificato radice e il certificato inferiore è il certificato di firma. Se nella catena è presente un solo certificato, anche il certificato di firma è il proprio certificato radice. È possibile determinare il numero di serie per ogni certificato che viene quindi utilizzato con [Certutil:](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))

**Per determinare il numero di serie per ogni certificato**

1.  Nel riquadro Percorso certificazione selezionare il certificato e quindi fare clic **su Visualizza certificato**.
2.  Nella finestra di dialogo Certificato selezionare la **scheda Dettagli** che visualizza il numero di serie e altre proprietà utili del certificato.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Passaggio 3: Determinare i certificati attendibili dal computer locale

Per poter distribuire un pacchetto dell'app, non deve essere considerato attendibile solo nel contesto dell'utente, ma anche nel contesto del computer locale. Di conseguenza, la firma digitale può risultare valida quando viene visualizzata nella scheda Firme digitali del passaggio precedente, ma ha comunque esito negativo durante la distribuzione del pacchetto dell'app.

**Per determinare se la catena di certificati usata per firmare il pacchetto dell'app è specificatamente attendibile dal computer locale**

1.  Eseguire questo comando:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Eseguire questo comando:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Se non si specifica il numero di serie del certificato, [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) elenca tutti i certificati considerati attendibili dal computer locale per tale archivio.

L'installazione del pacchetto potrebbe non riuscire a causa di errori di concatenamento dei certificati, anche se il certificato di firma non è autofirmato e il certificato radice si trova nell'archivio radice del computer locale. In questo caso, potrebbe verificarsi un problema di attendibilità per le autorità di certificazione intermedie. Per altre informazioni su questo problema, vedere [Uso dei certificati](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Commenti

Se si è determinato che non è stato possibile distribuire il pacchetto perché il certificato di firma non è attendibile, non installare il pacchetto a meno che non si sappia dove ha avuto origine e non si considera attendibile.

Se si vuole considerare manualmente attendibile l'app per l'installazione, ad esempio per installare il proprio pacchetto di app firmato con test, è possibile aggiungere manualmente il certificato all'attendibilità del certificato del computer locale dal pacchetto dell'app.

**Per aggiungere manualmente il certificato all'attendibilità del certificato del computer locale**

1.  In Esplora file fare clic con il pulsante destro del mouse sul pacchetto dell'app e scegliere Proprietà dal menu di scelta **rapida.**
2.  Nella finestra **di** dialogo Proprietà selezionare la **scheda Firme** digitali .
3.  Nell'elenco Firma selezionare la firma e quindi fare clic sul **pulsante** Dettagli.
4.  Nella finestra **di dialogo Dettagli firma** digitale fare clic sul pulsante **Visualizza** certificato.
5.  Nella finestra **di dialogo** Certificato fare clic su **Installa certificato.** .
6.  Nell'Importazione guidata certificati selezionare **Computer locale** e quindi fare clic su **Avanti.** Per continuare, è necessario concedere privilegi di amministratore.
7.  Selezionare **Inserisci tutti i certificati nell'archivio seguente** e passare all'archivio **Persone** attendibili.
8.  Fare **clic su Avanti** e quindi su **Fine** per completare la procedura guidata.

Dopo questa aggiunta manuale, è possibile vedere che il certificato è ora considerato attendibile nella **finestra di dialogo** Certificato.

È possibile rimuovere il certificato quando non è più necessario.

**Per rimuovere il certificato**

1.  Eseguire **Cmd.exe** come amministratore.
2.  Al prompt dei comandi dell'amministratore eseguire questo comando:

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Cercare il numero di serie del certificato installato. Questo numero è *certID*.
4.  Eseguire questo comando:

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

È consigliabile evitare di aggiungere manualmente i certificati radice al computer locale Autorità di certificazione radice disponibile nell'elenco locale [certificati](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store). La presenza di diverse applicazioni firmate con certificati concatenati allo stesso certificato radice, ad esempio applicazioni line-of-business, può essere più efficiente rispetto all'installazione di singoli certificati nell'archivio Persone attendibili. L'archivio Persone attendibili contiene certificati considerati attendibili per impostazione predefinita e pertanto non vengono verificati da autorità superiori o elenchi o catene di certificati attendibili. Per considerazioni sull'aggiunta di certificati all'Autorità di certificazione radice disponibile nell'elenco locale certificati, vedere Procedure consigliate per la [firma del codice](/previous-versions/windows/hardware/design/dn653556(v=vs.85)).

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'aggiunta di un certificato [agli archivi certificati del computer](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)locale influisce sull'attendibilità del certificato di tutti gli utenti del computer. È consigliabile installare i certificati di firma del codice desiderati per testare i pacchetti dell'app nell'archivio certificati Persone attendibili. Rimuovere tempestivamente tali certificati quando non sono più necessari, per impedire che vengano usati per compromettere l'attendibilità del sistema. Se si creano certificati di test personalizzati per la firma di pacchetti di app, è anche consigliabile limitare i privilegi associati al certificato di test. Per informazioni sulla creazione di certificati di test per la firma di pacchetti di app, vedere [Come creare un certificato di firma del pacchetto dell'app.](how-to-create-a-package-signing-certificate.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Esempi**
</dt> <dt>

[Creare un esempio di pacchetto dell'app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Concetti**
</dt> <dt>

[Risoluzione dei problemi di creazione pacchetti, distribuzione e query delle app Windows](troubleshooting.md)
</dt> <dt>

[Attività Certutil per la gestione dei certificati](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 
