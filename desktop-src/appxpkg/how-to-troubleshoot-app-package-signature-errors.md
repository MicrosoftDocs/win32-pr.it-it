---
title: Come risolvere gli errori di firma del pacchetto dell'app
description: Un errore di distribuzione dell'app può essere causato da un errore di convalida della firma digitale del pacchetto dell'app. Informazioni su come riconoscere questi errori e su come eseguirli.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0afe77ebfd478be5c652604ea575fc90b5d3ef
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104398836"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Come risolvere gli errori di firma del pacchetto dell'app

Un errore di distribuzione dell'app può essere causato da un errore di convalida della firma digitale del pacchetto dell'app. Informazioni su come riconoscere questi errori e su come eseguirli.

Quando si distribuisce un'app di Windows in pacchetto, Windows tenta sempre di convalidare la firma digitale nel pacchetto dell'app. Errori durante la convalida della firma del pacchetto. Ma perché il pacchetto non è stato convalidato potrebbe non essere ovvio. In particolare, se si firmano i pacchetti con certificati privati per i test locali, è spesso necessario gestire anche il trust per tali certificati. Una configurazione di attendibilità del certificato non corretta può causare errori di convalida della firma.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Creazione di pacchetti, distribuzione e query delle app di Windows](appx-portal.md)
-   [Verifica dell'attendibilità del certificato](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Prerequisiti

-   [Registro eventi di Windows](/windows/desktop/WES/windows-event-log) per diagnosticare gli errori di installazione.
-   [Attività certutil per la gestione di certificati](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) per la manipolazione dell'archivio certificati durante la risoluzione dei problemi

## <a name="instructions"></a>Istruzioni

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Passaggio 1: esaminare i registri eventi per informazioni di diagnostica

A seconda di come si è tentato di distribuire l'app, è possibile che non sia stato ricevuto un codice di errore significativo per l'errore di distribuzione. In questo caso, in genere è possibile ottenere il codice di errore direttamente dai registri eventi.

**Per ottenere il codice di errore dai registri eventi**

1.  Eseguire **eventvwr. msc**.
2.  Passare a **Visualizzatore eventi (local)**  >  **registri applicazioni e servizi**  >  **Microsoft**  >  **Windows**.
3.  Il primo log da controllare è **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**.
4.  Gli errori relativi alla distribuzione vengono registrati in **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**.

    Per gli errori di distribuzione, cercare l'evento di errore più recente 404. Questo evento di errore fornisce il codice di errore e una descrizione del motivo per cui la distribuzione non è riuscita. Se un evento di errore 465 precede l'evento 404, si è verificato un problema durante l'apertura del pacchetto.

Se non si è verificato l'errore 465, vedere la sezione relativa alla [risoluzione dei problemi generali di creazione di pacchetti, distribuzione e query delle app di Windows](troubleshooting.md). In caso contrario, fare riferimento a questa tabella per i codici di errore comuni che possono essere visualizzati nella stringa di errore per l'evento di errore 465:

| Codice di errore | Errore                                 | Descrizione                                                                                                          | Suggerimento                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | ERRORE di \_ installazione del \_ \_ pacchetto aperto \_ non riuscito | Non è stato possibile aprire il pacchetto dell'app.                                                                                 | Questo errore indica in genere un problema con il pacchetto. È necessario compilare e firmare nuovamente il pacchetto. Per altre informazioni, vedere [uso del pacchetto di app](make-appx-package--makeappx-exe-.md). |
| 0x80080205 | APPX \_ E \_ BLOCKMAP non validi \_            | Il pacchetto dell'app è stato alterato o contiene una mappa di blocco non valida.                                                  | Il pacchetto è danneggiato. È necessario compilare e firmare nuovamente il pacchetto. Per altre informazioni, vedere [uso del pacchetto di app](make-appx-package--makeappx-exe-.md).                                  |
| 0x800B0004 | ATTENDIBILità \_ E \_ oggetto \_ non \_ attendibile       | Il pacchetto dell'app è stato manomesso.                                                                              | Il contenuto del pacchetto non corrisponde più alla firma digitale. È necessario firmare nuovamente il pacchetto. Per altre informazioni, vedere [come firmare un pacchetto dell'app usando SignTool](how-to-sign-a-package-using-signtool.md).  |
| 0x800B0100 | TRUST \_ E \_ NoSignature                 | Il pacchetto dell'app non è firmato.                                                                                         | È possibile distribuire solo i pacchetti dell'app Windows firmati. Per informazioni sulla firma di un pacchetto dell'app, vedere [come firmare un pacchetto dell'app con SignTool](how-to-sign-a-package-using-signtool.md).                  |
| 0x800B0109 | CERTIFICATO \_ E \_ radice non attendibile \_              | La catena di certificati usata per firmare il pacchetto dell'applicazione termina con un certificato radice non attendibile.           | Continuare con il passaggio 2 per risolvere i problemi relativi all'attendibilità del certificato.                                                                                                                                                  |
| 0x800B010A | concatenamento di CERT \_ E \_                     | Non è stato possibile creare una catena di certificati per un'autorità radice attendibile dal certificato usato per firmare il pacchetto dell'app. | Continuare con il passaggio 2 per risolvere i problemi relativi all'attendibilità del certificato.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Passaggio 2: determinare la catena di certificati usata per firmare il pacchetto dell'app

Per individuare i certificati che il computer locale deve considerare attendibile, è possibile esaminare la catena di certificati per la firma digitale nel pacchetto dell'app.

**Per determinare la catena di certificati**

1.  In Esplora file fare clic con il pulsante destro del mouse sul pacchetto dell'app e scegliere **Proprietà**.
2.  Nella finestra di dialogo **Proprietà** selezionare la scheda **firme digitali** , che indica anche se la firma può essere convalidata.
3.  Nell'elenco firma selezionare la firma e quindi fare clic sul pulsante **Dettagli** .
4.  Nella finestra di dialogo **Dettagli firma digitale** fare clic sul pulsante **Visualizza certificato** .
5.  Nella finestra di dialogo **certificato** selezionare la scheda **percorso certificazione** .

Il certificato superiore nella catena è il certificato radice e il certificato inferiore è il certificato di firma. Se nella catena è presente un solo certificato, il certificato di firma è anche il proprio certificato radice. È possibile determinare il numero di serie per ogni certificato usato successivamente con [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)):

**Per determinare il numero di serie per ogni certificato**

1.  Nel riquadro Percorso certificazione selezionare il certificato e quindi fare clic su **Visualizza certificato**.
2.  Nella finestra di dialogo certificato selezionare la scheda **Dettagli** , che consente di visualizzare il numero di serie e altre proprietà utili del certificato.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Passaggio 3: determinare i certificati considerati attendibili dal computer locale

Per poter distribuire un pacchetto dell'app, questo non deve essere considerato attendibile solo nel contesto dell'utente, ma anche nel contesto del computer locale. Di conseguenza, la firma digitale può apparire valida quando viene visualizzata nella scheda firme digitali del passaggio precedente, ma non viene ancora eseguita la convalida durante la distribuzione del pacchetto dell'app.

**Per determinare se la catena di certificati usata per firmare il pacchetto dell'app è ritenuta attendibile in modo specifico dal computer locale**

1.  Eseguire questo comando:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Eseguire questo comando:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Se non si specifica il numero di serie del certificato, [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) elenca tutti i certificati considerati attendibili dal computer locale per tale archivio.

Potrebbe non essere possibile installare il pacchetto a causa di errori di concatenamento del certificato, anche se il certificato di firma non è autofirmato e il certificato radice si trova nell'archivio radice del computer locale. In questo caso, è possibile che si verifichi un problema di attendibilità per le autorità di certificazione intermedie. Per ulteriori informazioni su questo problema, vedere [utilizzo dei certificati](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Commenti

Se è stato determinato che non è stato possibile distribuire il pacchetto perché il certificato di firma non è attendibile, non installare il pacchetto a meno che non si sappia dove è stato originato e lo si considera attendibile.

Per considerare attendibile manualmente l'app per l'installazione, ad esempio per installare il pacchetto dell'app firmato da test personalizzato, è possibile aggiungere manualmente il certificato all'attendibilità del certificato del computer locale dal pacchetto dell'app.

**Per aggiungere manualmente il certificato all'attendibilità del certificato del computer locale**

1.  In Esplora file fare clic con il pulsante destro del mouse sul pacchetto dell'app e nel menu di scelta rapida popup selezionare **Proprietà**.
2.  Nella finestra di dialogo **Proprietà** selezionare la scheda **firme digitali** .
3.  Nell'elenco firma selezionare la firma e quindi fare clic sul pulsante **Dettagli** .
4.  Nella finestra di dialogo **Dettagli firma digitale** fare clic sul pulsante **Visualizza certificato** .
5.  Nella finestra di dialogo **certificato** fare clic su **Installa certificato...** .
6.  Nell'importazione guidata certificati selezionare **computer locale** e quindi fare clic su **Avanti**. È necessario concedere i privilegi di amministratore per continuare.
7.  Selezionare **colloca tutti i certificati nel seguente archivio** e passare all'archivio **persone attendibili** .
8.  Fare clic su **Avanti**, quindi su **fine** per completare la procedura guidata.

Dopo questa aggiunta manuale, è possibile osservare che il certificato è ora attendibile nella finestra di dialogo **certificato** .

È possibile rimuovere il certificato dopo che non è più necessario.

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

Si consiglia di evitare di aggiungere manualmente i certificati radice all' [archivio certificati delle autorità di certificazione radice attendibili](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)del computer locale. La presenza di più applicazioni firmate con certificati concatenati allo stesso certificato radice, ad esempio le applicazioni line-of-business, può essere più efficiente rispetto all'installazione dei singoli certificati nell'archivio persone attendibili. L'archivio persone attendibili contiene certificati considerati attendibili per impostazione predefinita, pertanto non vengono verificati da autorità o elenchi di attendibilità o catene di certificati. Per considerazioni sull'aggiunta di certificati all'archivio certificati delle autorità di certificazione radice attendibili, vedere [procedure consigliate](/previous-versions/windows/hardware/design/dn653556(v=vs.85))per la firma del codice.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Aggiungendo un certificato agli [archivi certificati del computer locale](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), si influisce sull'attendibilità del certificato di tutti gli utenti del computer. Si consiglia di installare i certificati di firma del codice desiderati per testare i pacchetti dell'applicazione nell'archivio certificati persone attendibili. Rimuovere tempestivamente questi certificati quando non sono più necessari, per impedire che vengano usati per compromettere l'attendibilità del sistema. Se si creano certificati di test personalizzati per la firma dei pacchetti dell'app, è anche consigliabile limitare i privilegi associati al certificato di test. Per informazioni sulla creazione di certificati di test per la firma dei pacchetti dell'app, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Esempi**
</dt> <dt>

[Creare un pacchetto dell'app di esempio]https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Concetti**
</dt> <dt>

[Risoluzione dei problemi di creazione pacchetti, distribuzione e query delle app Windows](troubleshooting.md)
</dt> <dt>

[Attività certutil per la gestione dei certificati](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 