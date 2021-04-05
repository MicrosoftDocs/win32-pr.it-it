---
title: Strumento per la creazione di pacchetti di app (MakeAppx.exe)
description: App Packager (MakeAppx.exe) crea un pacchetto dell'app da file su disco o estrae i file da un pacchetto dell'app su disco.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117578"
---
# <a name="app-packager-makeappxexe"></a>Strumento per la creazione di pacchetti di app (MakeAppx.exe)

> [!Note]  
> Per indicazioni su UWP sull'uso di questo strumento, vedere [creare un pacchetto dell'app con lo strumento MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).

 

App Packager (MakeAppx.exe) crea un pacchetto dell'app da file su disco o estrae i file da un pacchetto dell'app su disco. A partire da Windows 8.1, app Packager crea anche un bundle del pacchetto dell'app dai pacchetti dell'app su disco o estrae i pacchetti dell'app da un bundle del pacchetto dell'app su disco. È incluso in Microsoft Visual Studio e Windows Software Development Kit (SDK) per Windows 8 o Windows Software Development Kit (SDK) per Windows 8.1. Visitare [i download per gli sviluppatori]( https://msdn.microsoft.com/windows/apps/br229516.aspx) .

Lo strumento MakeAppx.exe si trova in genere in questi percorsi:

-   In x86: C: \\ Program Files (x86) \\ windows Kit \\ 8,0 \\ bin \\ x86 \\makeappx.exe o C: \\ program files (x86) \\ Windows Kit \\ 8,1 \\ bin \\ x86 \\makeappx.exe
-   In x64 in due posizioni:
    -   C: \\ programmi (x86) \\ windows Kit \\ 8,0 \\ bin \\ x86 \\makeappx.exe o c: \\ program files (x86) \\ Windows Kit \\ 8,1 \\ bin \\ x86 \\makeappx.exe
    -   C: \\ programmi (x86) \\ windows Kit \\ 8,0 \\ bin \\ x64 \\makeappx.exe o c: \\ programmi (x86) \\ Windows Kit \\ 8,1 \\ bin \\ x64 \\makeappx.exe

Non è disponibile alcuna versione ARM dello strumento.

-   [Per creare un pacchetto utilizzando una struttura di directory](#to-create-a-package-using-a-directory-structure)
-   [Per creare un pacchetto usando un file di mapping](#to-create-a-package-using-a-mapping-file)
-   [Per firmare il pacchetto con SignTool](#to-sign-the-package-using-signtool)
-   [Per estrarre i file da un pacchetto](#to-extract-files-from-a-package)
-   [Per creare un bundle di pacchetti usando una struttura di directory](#to-create-a-package-bundle-using-a-directory-structure)
-   [Per creare un bundle di pacchetti usando un file di mapping](#to-create-a-package-bundle-using-a-mapping-file)
-   [Per estrarre i pacchetti da un bundle](#to-extract-packages-from-a-bundle)
-   [Per crittografare un pacchetto con un file di chiave](#to-encrypt-a-package-with-a-key-file)
-   [Per crittografare un pacchetto con una chiave di test globale](#to-encrypt-a-package-with-a-global-test-key)
-   [Per decrittografare un pacchetto con un file di chiave](#to-decrypt-a-package-with-a-key-file)
-   [Per decrittografare un pacchetto con una chiave di test globale](#to-decrypt-a-package-with-a-global-test-key)
-   [Utilizzo](#usage)

## <a name="using-app-packager"></a>Uso del pacchetto di app

> [!Note]  
> I percorsi relativi sono supportati in tutto lo strumento.

 

### <a name="to-create-a-package-using-a-directory-structure"></a>Per creare un pacchetto utilizzando una struttura di directory

Inserire il AppxManifest.xml nella radice di una directory contenente tutti i file di payload per l'app. Viene creata una struttura di directory identica per il pacchetto dell'app e sarà disponibile quando il pacchetto viene estratto in fase di distribuzione.

1.  Inserire tutti i file in un'unica struttura di directory, creando sottodirectory come desiderato.

2.  Creare un manifesto del pacchetto valido, AppxManifest.xml e inserirlo nella directory radice.

3.  Eseguire questo comando:

    **MakeAppx Pack/d** *input \_ DirectoryPath* **/p** _filePath_**. appx**

### <a name="to-create-a-package-using-a-mapping-file"></a>Per creare un pacchetto usando un file di mapping

1.  Creare un manifesto del pacchetto valido, AppxManifest.xml.

2.  Creare un file di mapping. La prima riga contiene i **\[ file \]** di stringa e le righe che seguono specificano i percorsi di origine (disco) e di destinazione (pacchetto) nelle stringhe tra virgolette.

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  Eseguire questo comando:

    **MakeAppx Pack/f** *mapping \_ filePath* **/p** _filePath_**. appx**

### <a name="to-sign-the-package-using-signtool"></a>Per firmare il pacchetto con SignTool

1.  Creare il certificato. Il server di pubblicazione elencato nel manifesto deve corrispondere alle informazioni sul soggetto dell'editore del certificato di firma. Per altre informazioni sulla creazione di un certificato di firma, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).

2.  Eseguire SignTool.exe per firmare il pacchetto:

    **Segno di SignTool/a/v/FD** *HashAlgorithm* **/f** *certFileName* _filePath_**. appx**

    *HashAlgorithm* deve corrispondere all'algoritmo hash usato per creare il BlockMap quando l'app è stata assemblata. Con l'utilità di creazione pacchetti MakeAppx, l'algoritmo hash predefinito appx BlockMap è **SHA256**. Eseguire SignTool.exe specificando **SHA256** come algoritmo/FD (file digest):

    **Signtool sign/a/v/FD SHA256/F** *certFileName* _filePath_**. appx**

    Per altre informazioni su come firmare i pacchetti, vedere [come firmare un pacchetto dell'app con SignTool](how-to-sign-a-package-using-signtool.md).

### <a name="to-extract-files-from-a-package"></a>Per estrarre i file da un pacchetto

1.  Eseguire questo comando:

    **MakeAppx decomprimere/p** _file_**. appx/d** *\_ directory di output*

2.  Il pacchetto decompresso ha la stessa struttura del pacchetto installato.

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a>Per creare un bundle di pacchetti usando una struttura di directory

Viene usato il comando **bundle** per creare un bundle dell'app in <output bundle name> aggiungendo tutti i pacchetti da <content directory> (incluse le sottocartelle). Se <content directory> contiene un manifesto del bundle, AppxBundleManifest.xml, viene ignorato.

1.  Inserire tutti i pacchetti in un'unica struttura di directory, creando sottodirectory nel modo desiderato.

2.  Eseguire questo comando:

    **MakeAppx bundle/d** *input \_ DirectoryPath* **/p** _filePath_**. appxbundle**

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a>Per creare un bundle di pacchetti usando un file di mapping

Viene usato il comando **bundle** per creare un bundle dell'app in <output bundle name> aggiungendo tutti i pacchetti da un elenco di pacchetti in <mapping file> . Se <mapping file> contiene un manifesto del bundle, AppxBundleManifest.xml, viene ignorato.

1.  Creare un oggetto <mapping file>. La prima riga contiene i **\[ file \]** di stringa e le righe che seguono specificano i pacchetti da aggiungere al bundle. Ogni pacchetto è descritto da una coppia di percorsi tra virgolette, separate da spazi o tabulazioni. La coppia di percorsi rappresenta l'origine (su disco) e la destinazione (in bundle) del pacchetto. Tutti i nomi dei pacchetti di destinazione devono avere l'estensione appx.

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  Eseguire questo comando:

    **MakeAppx bundle/f** *mapping \_ filePath* **/p** _filePath_**. appxbundle**

### <a name="to-extract-packages-from-a-bundle"></a>Per estrarre i pacchetti da un bundle

1.  Eseguire questo comando:

    **MakeAppx Unbundle/p** _\_ nome bundle_**. appxbundle/d** *\_ directory di output*

2.  Il bundle decompresso ha la stessa struttura del bundle del pacchetto installato.

### <a name="to-encrypt-a-package-with-a-key-file"></a>Per crittografare un pacchetto con un file di chiave

1.  Creazione di un file di chiave. I file di chiave devono iniziare con una riga contenente la stringa " \[ Keys \] " seguita da righe che descrivono le chiavi per la crittografia del pacchetto. Ogni chiave viene descritta da una coppia di stringhe racchiuse tra virgolette, separate da spazi o tabulazioni. La prima stringa rappresenta l'ID chiave e la seconda stringa rappresenta la chiave di crittografia in formato esadecimale.

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  Eseguire questo comando:

    **MakeAppx.exe crittografare/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto crittografato_**. eappx/KF** _\_ nome file_**. txt**

3.  Il pacchetto di input verrà crittografato nel pacchetto crittografato specificato utilizzando il file di chiave fornito.

### <a name="to-encrypt-a-package-with-a-global-test-key"></a>Per crittografare un pacchetto con una chiave di test globale

1.  Eseguire questo comando:

    **MakeAppx.exe crittografare/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto crittografato_**. eappx/KT**

2.  Il pacchetto di input verrà crittografato nel pacchetto crittografato specificato usando la chiave di test globale.

### <a name="to-decrypt-a-package-with-a-key-file"></a>Per decrittografare un pacchetto con un file di chiave

1.  Creazione di un file di chiave. I file di chiave devono iniziare con una riga contenente la stringa " \[ Keys \] " seguita da righe che descrivono le chiavi per la crittografia del pacchetto. Ogni chiave viene descritta da una coppia di stringhe racchiuse tra virgolette, separate da spazi o tabulazioni. La prima stringa rappresenta l'ID chiave a 32 byte con codifica Base64 e la seconda stringa rappresenta la chiave di crittografia 32 byte con codifica Base64.

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  Eseguire questo comando:

    **MakeAppx.exe Decrypt/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto non crittografato_**. eappx/KF** _\_ nome file_**. txt**

3.  Il pacchetto di input verrà decrittografato nel pacchetto non crittografato specificato utilizzando il file di chiave fornito.

### <a name="to-decrypt-a-package-with-a-global-test-key"></a>Per decrittografare un pacchetto con una chiave di test globale

1.  Eseguire questo comando:

    **MakeAppx.exe Decrypt/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto non crittografato_**. eappx/KT**

2.  Il pacchetto di input verrà decrittografato nel pacchetto non crittografato specificato utilizzando la chiave di test globale.

## <a name="usage"></a>Utilizzo

L'argomento della riga di comando **/p** è sempre obbligatorio, con **/d**, **/f** o **/EP**. Si noti che **/d**, **/f** e **/EP** si escludono a vicenda.

**\[ Opzioni \] MakeAppx Pack** **/p** *\<output package name\>* **/d***\<content directory\>*

**\[ Opzioni \] MakeAppx Pack** **/p** *\<output package name\>* **/f***\<mapping file\>*

**MakeAppx Decomprimi \[ Opzioni \]** **/p** *\<input package name\>* **/d***\<output directory\>*

**\[ Opzioni \] bundle MakeAppx** **/p** *\<output bundle name\>* **/d***\<content directory\>*

**\[ Opzioni \] bundle MakeAppx** **/p** *\<output bundle name\>* **/f***\<mapping file\>*

**MakeAppx Unbundle \[ Options \]** **/p** *\<input bundle name\>* **/d***\<output directory\>*

**\[ Opzioni \] di crittografia MakeAppx** **/p** *\<input package name\>* **/EP***\<output package name\>*

**\[ Opzioni \] di decrittografia MakeAppx** **/p** *\<input package name\>* **/EP***\<output package name\>*

## <a name="command-line-syntax"></a>Sintassi della riga di comando

Di seguito è illustrata la sintassi di utilizzo comune da riga di comando per MakeAppx.

**MakeAppx \[ pack \| unpack \| bundle \| Unbundle \| Encrypt \| Decrypt \]** \[ **/h** **/KF** **/KT** **/l** **/o** **/No** **/NV** **/v** **/PFN** **/?**\]

**MakeAppx** comprime o decomprime i file in un pacchetto, aggrega o decomprime i pacchetti in un bundle oppure crittografa o decrittografa il pacchetto o il bundle dell'applicazione nella directory di input o nel file di mapping specificato. Di seguito è riportato l'elenco dei parametri che si applicano a **MakeAppx Pack**, **MakeAppx decomprimete**, **MakeAppx bundle**, **MakeAppx Unbundle**, **MakeAppx Encrypt** o **MakeAppx Decrypt**.

<dl> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Questa opzione viene utilizzata per i pacchetti localizzati. La convalida predefinita può comportare problemi se applicata ai pacchetti localizzati. Questa opzione disattiva solo la convalida specifica, senza che sia necessario disabilitare la convalida.

</dd> <dt>

<span id="_o"></span><span id="_O"></span>**/o**
</dt> <dd>

Sovrascrivere il file di output se esistente. Se non si specifica questa opzione o l'opzione **/No** , all'utente viene chiesto se desidera sovrascrivere il file.

Non è possibile usare questa opzione con **/No**.

</dd> <dt>

<span id="_no"></span><span id="_NO"></span>**/No**
</dt> <dd>

Impedisce la sovrascrittura del file di output, se presente. Se non si specifica questa opzione o l'opzione **/o** , viene chiesto all'utente se desidera sovrascrivere il file.

Non è possibile usare questa opzione con **/o**.

</dd> <dt>

<span id="_nv"></span><span id="_NV"></span>**/nv**
</dt> <dd>

Ignorare la convalida semantica. Se non specifichi questa opzione, lo strumento esegue una convalida completa del pacchetto.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Abilitare l'output di registrazione dettagliata alla console.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Visualizzare il testo della guida.

</dd> </dl>

**MakeAppx Pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx Unbundle**, **MakeAppx Encrypt** e **MakeAppx Decrypt** sono comandi che si escludono a vicenda. Ecco i parametri della riga di comando che si applicano in modo specifico a ogni comando:

**MakeAppx Pack** \[ **h**\]

Crea un pacchetto.

<dl> <dt>

<span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** ( *algoritmo* )
</dt> <dd>

Specifica l'algoritmo hash da usare per la creazione della mappa dei blocchi. Di seguito sono riportati i valori validi per *Algorithm*:

<dl> <dd>SHA256 (impostazione predefinita)</dd> <dd>SHA384</dd> <dd>SHA512</dd> </dl>

Non è possibile usare questa opzione con il comando **unpack** .

</dd> </dl>

**Decompressione MakeAppx** \[ **PFN**\]

Estrae tutti i file dal pacchetto specificato nella directory di output indicata. L'output ha la stessa struttura di directory del pacchetto.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Specifica una directory denominata con il nome completo del pacchetto. Questa directory viene creata nel percorso di output specificato. Non è possibile usare questa opzione con il comando **Pack** .

</dd> </dl>

**MakeAppx Unbundle** \[ **PFN**\]

Decomprime tutti i pacchetti in una sottodirectory nel percorso di output specificato, con il nome completo del bundle. L'output ha la stessa struttura di directory del bundle di pacchetti installato.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Specifica una directory denominata con il nome completo del bundle del pacchetto. Questa directory viene creata nel percorso di output specificato. Non è possibile usare questa opzione con il comando **bundle** .

</dd> </dl>

**Crittografia MakeAppx** \[ **KF**, **KT**\]

Crea un pacchetto dell'app crittografato dal pacchetto dell'app di input specificato nel pacchetto di output specificato.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Esegue la crittografia del pacchetto o del bundle usando la chiave dal file di chiave specificato. Non è possibile usare questa opzione con **KT**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Crittografa il pacchetto o il bundle usando la chiave di test globale. Non è possibile usare questa opzione con **KF**.

</dd> </dl>

**Decrittografia MakeAppx** \[ **KF**, **KT**\]

Crea un pacchetto dell'app non crittografato dal pacchetto dell'app di input specificato nel pacchetto di output specificato.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Decrittografa il pacchetto o il bundle usando la chiave dal file di chiave specificato. Non è possibile usare questa opzione con **KT**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Decrittografa il pacchetto o il bundle usando la chiave di test globale. Non è possibile usare questa opzione con **KF**.

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a>Convalida semantica eseguita da MakeAppx

MakeAppx esegue una convalida semantica limitata progettata per intercettare gli errori di distribuzione più comuni e garantire la validità del pacchetto dell'app.

La convalida assicura che:

-   Tutti i file a cui si fa riferimento nel manifesto del pacchetto siano inclusi nel pacchetto dell'app.
-   Un'applicazione non abbia due chiavi identiche.
-   Un'applicazione non esegue la registrazione per un protocollo non consentito da questo elenco: SMB, FILE, MS-WWA-WEB, MS-WWA.

Questa convalida semantica non è completa e non è garantito che i pacchetti compilati da MakeAppx siano installabili.

 

 