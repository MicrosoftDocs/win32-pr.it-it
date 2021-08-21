---
title: Come creare un certificato di firma per pacchetti app
description: Informazioni su come usare MakeCert.exe e Pvk2Pfx.exe per creare un certificato di firma del codice di test, in modo da poter firmare i pacchetti Windows'app.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc495c27e63dc4ee3a42db1b2763f4f59f7647a3a98d20193d8049dcfad965c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049069"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>Come creare un certificato di firma per pacchetti app

> [!IMPORTANT]
> MakeCert.exe è deprecato. Per indicazioni correnti sulla creazione di un certificato, vedere [Creare un certificato per la firma del pacchetto.](/windows/msix/package/create-certificate-package-signing)

 

Informazioni su come [**usare**](/windows-hardware/drivers/devtest/makecert)MakeCert.exee [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) per creare un certificato di firma del codice di test, in modo da poter firmare i pacchetti Windows'app.

È necessario firmare digitalmente le app Windows pacchetti prima di distribuirle. Se non si usa Microsoft Visual Studio 2012 per creare e firmare i pacchetti dell'app, è necessario creare e gestire i propri certificati di firma del codice. È possibile creare certificati [**usando**](/windows-hardware/drivers/devtest/makecert)MakeCert.exee [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) da Windows Driver Kit (WDK). È quindi possibile usare i certificati per firmare i pacchetti dell'app, in modo che possano essere distribuiti in locale per il test.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Pacchetti di app e distribuzione](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Strumenti per la firma dei driver](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Prerequisiti

-   [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) strumenti dal WDK

## <a name="instructions"></a>Istruzioni

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Passaggio 1: Determinare il nome dell'autore del pacchetto

Per rendere utilizzabile il certificato di firma creato con il pacchetto dell'app da firmare, il nome soggetto del certificato di firma deve corrispondere all'attributo **Publisher** dell'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) nel AppxManifest.xml per tale app. Si supponga, ad esempio, AppxManifest.xml contiene:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Per il *parametro publisherName* specificato con l'utilità [**MakeCert**](/windows-hardware/drivers/devtest/makecert) nel passaggio successivo, usare "CN=Contoso Software, O=Contoso Corporation, C=US".

> [!Note]  
> Questa stringa di parametro viene specificata tra virgolette e fa distinzione tra maiuscole e minuscole e spazi vuoti.

 

La **Publisher** di attributo definita per l'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) nel AppxManifest.xml deve essere identica alla stringa specificata con il [**parametro MakeCert**](/windows-hardware/drivers/devtest/makecert) /n per il nome soggetto del certificato. Copiare e incollare la stringa, se possibile.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Passaggio 2: Creare una chiave privata usando MakeCert.exe

Usare [**l'utilità MakeCert**](/windows-hardware/drivers/devtest/makecert) per creare un certificato di test autofirmato e una chiave privata:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Questo comando richiede di specificare una password per il file con estensione pvk. È consigliabile scegliere una [password complessa](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) e mantenere la chiave privata in una posizione sicura.

È consigliabile usare i parametri suggeriti nell'esempio precedente per i motivi seguenti:

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Crea un certificato radice autofirmato. In questo modo si semplifica la gestione del certificato di test.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Contrassegna il vincolo di base per il certificato come entità finale. Ciò impedisce l'uso del certificato come autorità di certificazione (CA) che può rilasciare altri certificati.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Imposta i valori EKU (Enhanced Key Usage) per il certificato.

> [!Note]  
> Non inserire uno spazio tra i due valori delimitati da virgole.

 

-   1.3.6.1.5.5.7.3.3 indica che il certificato è valido per la firma del codice. Specificare sempre questo valore per limitare l'utilizzo previsto per il certificato.
-   1.3.6.1.4.1.311.10.3.13 indica che il certificato rispetta la firma della durata. In genere, se una firma è contrassegnata con timestamp, purché il certificato sia valido nel momento in cui è stato contrassegnato come timestamp, la firma rimane valida anche se il certificato scade. Questo EKU forza la scadenza della firma indipendentemente dal fatto che la firma sia contrassegnata con timestamp.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Imposta la data di scadenza del certificato. Specificare un valore per il *parametro expirationDate* nel formato mm/gg/aaaaa. È consigliabile scegliere una data di scadenza solo se necessario a scopo di test, in genere inferiore a un anno. Questa data di scadenza insieme all'EKU di firma della durata consente di limitare la finestra in cui il certificato può essere compromesso e usato in modo improprio.

</dd> </dl>

Per altre informazioni sulle altre opzioni, vedere [**MakeCert.**](/windows-hardware/drivers/devtest/makecert)

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Passaggio 3: Creare un file Exchange (con estensione pfx) di informazioni personali usando Pvk2Pfx.exe

Usare l'utilità [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) per convertire i file con estensione pvk e cer creati da [**MakeCert**](/windows-hardware/drivers/devtest/makecert) in un file con estensione pfx che è possibile usare con [SignTool](/windows/desktop/SecCrypto/signtool) per firmare un pacchetto dell'app:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

I *file MyKey.pvk* e *MyKey.cer* [](/windows-hardware/drivers/devtest/makecert) sono gli stessiMakeCert.execreati nel passaggio precedente. Usando il parametro facoltativo /po, è possibile specificare una password diversa per il file PFX risultante. in caso contrario, pfx ha la stessa password di *MyKey.pvk*.

Per altre informazioni sulle altre opzioni, vedere [**Pvk2Pfx.**](/windows-hardware/drivers/devtest/pvk2pfx)

## <a name="remarks"></a>Commenti

Dopo aver creato il file con estensione pfx, è possibile usare il file con [SignTool](/windows/desktop/SecCrypto/signtool) per firmare un pacchetto dell'app. Per altre informazioni, vedere [Come firmare un pacchetto dell'app usando SignTool.](how-to-sign-a-package-using-signtool.md) Tuttavia, il certificato non è ancora considerato attendibile dal computer locale per la distribuzione dei pacchetti di app fino a quando non viene installato nell'archivio certificati attendibili del computer locale. È possibile usare [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), che viene fornito con Windows.

**Per installare i certificati con WindowsCertutil.exe**

1.  Eseguire **Cmd.exe** come amministratore.
2.  Eseguire questo comando:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

È consigliabile rimuovere i certificati se non sono più in uso. Dallo stesso prompt dei comandi amministratore eseguire questo comando:

``` syntax
Certutil -delStore TrustedPeople certID
```

**certID è** il numero di serie del certificato. Eseguire questo comando per determinare il numero di serie del certificato:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'aggiunta di un certificato [agli archivi certificati del computer](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)locale influisce sull'attendibilità del certificato di tutti gli utenti del computer. È consigliabile installare i certificati di firma del codice desiderati per testare i pacchetti dell'app nell'archivio certificati Persone attendibili. Rimuovere tempestivamente tali certificati quando non sono più necessari, per impedire che vengano usati per compromettere l'attendibilità del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Esempi**
</dt> <dt>

[Creare un esempio di pacchetto dell'app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Concetti**
</dt> <dt>

[Procedure consigliate per la firma del codice](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Come firmare un pacchetto di app con SignTool](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

[Firma di un pacchetto di app](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 