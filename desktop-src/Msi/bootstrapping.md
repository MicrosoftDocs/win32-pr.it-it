---
description: Attualmente, ogni installazione che tenta di utilizzare il Windows Installer inizia controllando se il programma di installazione è presente nel computer dell'utente e, se non è presente, se l'utente e il computer sono pronti per l'installazione Windows Installer.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Bootstrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff743acbcd2dfc81b0e912e5be84c363f34614ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311010"
---
# <a name="bootstrapping"></a>Bootstrap

Attualmente, ogni installazione che tenta di utilizzare il Windows Installer inizia controllando se il programma di installazione è presente nel computer dell'utente e, se non è presente, se l'utente e il computer sono pronti per l'installazione Windows Installer. Un'applicazione di installazione [Instmsi.exe](instmsi-exe.md) è disponibile con Windows Installer SDK che contiene tutta la logica e le funzionalità per l'installazione di Windows Installer. Tuttavia, un'applicazione di bootstrap deve gestire questa installazione.

L'applicazione di bootstrap deve prima verificare se Windows Installer è attualmente installata. Le applicazioni possono ottenere la versione di Windows Installer attualmente installata usando [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc). Se Windows Installer non è attualmente installato, l'applicazione di bootstrap deve eseguire una query sul sistema operativo per determinare quale versione del Instmsi.exe è obbligatoria. Una volta avviata l'installazione di Windows Installer, l'applicazione di bootstrap deve gestire i codici restituiti dall'applicazione Instmsi.exe e gestire eventuali riavvii durante l'installazione del Windows Installer. Per ulteriori informazioni, vedere [determinazione della versione di Windows Installer](determining-the-windows-installer-version.md)

Nell'esempio seguente viene illustrato il modo in cui l'applicazione di installazione che installa Microsoft Office 2000 controlla il sistema dell'utente e configura l'installazione del Windows Installer. Questo esempio è stato scritto in modo specifico per installare Office 2000 e deve essere usato solo come riferimento generale.

Quando un utente inserisce un CD-ROM di Office 2000 nel computer, Setup.exe tenta di avviare la modalità di manutenzione, l'applicazione di installazione o non esegue alcuna operazione, in base alle esigenze dell'utente. Nella sezione seguente viene descritto il modo in cui l'applicazione di installazione di Office 2000, denominata Setup.exe, qualifica l'utente e il relativo computer, costruisce una riga di comando e installa Windows Installer utilizzando l'applicazione Msiexec.exe.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Setup.exe modalità di bootstrap del Windows Installer quando si installa Office 2000

1.  L'utente inserisce un CD-ROM di Office 2000 nel computer. Il sistema operativo Windows inizia Setup.exe usando l'opzione/autorun e il file Autorun. inf. Il file Autorun. inf si trova nella directory principale del CD-ROM di Office 2000 e contiene le sezioni seguenti:

    \[Autorun\]

     

    \[Funzionalità di Office\]

     

    \[Informazioni sul prodotto\]

     

    \[ServicePack \] .

    La \[ \] sezione Autorun contiene una riga di comando che esegue l'applicazione Setup.exe, esegue l'icona utilizzata per visualizzare il disco e contiene informazioni per aggiungere un'opzione "Install" e un'opzione "Configure" al menu di scelta rapida per il CD-ROM.

    La \[ sezione funzionalità \] di Office contiene un elenco di caratteristiche e coppie di nomi di funzionalità.

    Nella \[ sezione informazioni sul prodotto sono \] specificati il nome e la versione dell'applicazione.

    La \[ \] sezione ServicePack consente a un amministratore di rete di impostare il livello di Service Pack minimo necessario. L'amministratore di rete può utilizzare questa sezione per creare il testo di un messaggio di avviso visualizzato se il sistema operativo locale non dispone del Service Pack necessario.

    Di seguito è riportato un esempio di autorun. inf.

    ``` syntax
    [autorun] 
    OPEN=setup.EXE /AUTORUN /KEY:Software\Microsoft\Office\9.0\Common\General\InstallProductID
    ICON=setup.EXE,1
    shell\configure=&Configure
    shell\configure\command=setup.EXE
    shell\install=&Install
    shell\install\command=setup.EXE
    [OfficeFeatures]
    Feature1=ACCESSFiles
    Feature2=OfficeFiles
    Feature3=WORDFiles
    Feature4=EXCELFiles
    Feature5=PPTFiles
    [ProductInformation]
    DisplayName=Microsoft Office 9
    Version=9.0
    ProductCode={product guid}
    [ServicePack]
    MessageText="The operating system does not have a required service pack. Please download and install this from www.microsoft.com."
    SPLevel=3
    ```

2.  L'applicazione Setup.exe verifica il \_ mutex MsiPromptForCD. Windows Installer crea questo mutex quando viene richiesto all'utente di inserire il CD-ROM. La presenza del mutex indica che Windows Installer sta eseguendo un'installazione che ha richiesto il CD-ROM di Office 2000. In questo caso, l'applicazione Setup.exe si chiude immediatamente e consente l'installazione di Office 2000 per continuare. Se il mutex è assente, l'applicazione Setup.exe continua nel passaggio 3, in cui viene valutata una chiave del registro di sistema per determinare se Office 2000 è installato.
3.  L'applicazione Setup.exe controlla la presenza della chiave del registro di sistema office9:

    **HKCU/Software/Microsoft/Office/9.0/comune/generale/InstallProductID**

    Se questa chiave del registro di sistema non esiste, l'applicazione Setup.exe continua al passaggio 6 in cui viene verificato il sistema operativo per determinare se è idoneo per l'installazione di Office 2000.

4.  Se la chiave del registro di sistema di Office 2000 esiste, l'applicazione Setup.exe controlla lo stato di installazione corrente chiamando [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea). Uno stato di restituzione di InstallState \_ default indica che office 2000 è già installato e che l'applicazione Setup.exe continua nel passaggio 5, dove office 2000 viene controllato per l'esecuzione dall'origine.

    Se Office 2000 non è installato, l'applicazione Setup.exe continua con il passaggio 6 in cui viene verificato il sistema operativo per determinare se è idoneo per l'installazione di Office 2000.

5.  L'applicazione Setup.exe chiama [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) per ogni funzionalità della sezione **\[ OfficeFeatures \]** del file Autorun. inf. Se una di queste funzionalità restituisce \_ l'origine InstallState, questo indica che la funzionalità viene eseguita dall'origine e che l'applicazione Setup.exe termina immediatamente.

    Se nessuna delle funzionalità restituisce l' \_ origine InstallState, l'applicazione Setup.exe avvia l'applicazione del programma di installazione, Msiexec.exe e visualizza la modalità di manutenzione Windows Installer prima di uscire.

6.  L'applicazione Setup.exe determina se il sistema operativo è idoneo per un'installazione di Office 2000. Per installare Office 2000, è necessario Windows XP. Se il sistema operativo richiede un aggiornamento Service Pack per qualificarsi per Office 2000, l'applicazione Setup.exe Visualizza il testo specificato nel file Autorun. inf. Se il sistema operativo non è idoneo per Office 2000 o un aggiornamento di Office 2000, l'applicazione Setup.exe Visualizza un messaggio che impedisce all'utente di continuare.

    Se il sistema operativo è idoneo per Office 2000, l'applicazione Setup.exe continua al passaggio 7, che determina se Windows Installer è installato nel computer dell'utente.

7.  Se Windows Installer è presente nel computer dell'utente, l'applicazione Setup.exe avvia l'applicazione Msiexec.exe e passa al file Office 2000. msi.

    Se Windows Installer non è installato nel computer locale, l'applicazione Setup.exe prosegue con il passaggio 8, che determina se il sistema operativo deve avere Windows Installer installato.

8.  Se il computer locale è idoneo per l'installazione di Windows Installer, l'applicazione Setup.exe esegue la versione corretta dell'applicazione Instmsi.exe Installer per la piattaforma. Setup.exe possibile passare l'opzione della riga di comando "/q" per eliminare l'interfaccia utente e impedire all'utente di modificare le opzioni di configurazione dell'installazione.
9.  L'applicazione Setup.exe carica il file di Msi.dll appena installato ed esegue una chiamata alla funzione [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) per installare l'applicazione dell'utente.

## <a name="setupexe-command-line-parameters"></a>Parametri della riga di comando Setup.exe

L'applicazione Setup.exe consente agli amministratori e agli utenti di passare le opzioni della riga di comando all'applicazione Msiexec.exe. Per ulteriori informazioni, vedere [Opzioni della riga di comando](command-line-options.md). Nella tabella seguente sono elencate le opzioni di comando che è possibile utilizzare con Setup.exe.



| Opzione                       | Utilizzo                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /Autorun                     | setup.exe/Autorun                                                                                                                           | Esegue Autorun. inf descritto in precedenza.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Avvia un'installazione amministrativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[\| \] *pacchetto* u m o <br/> \[\|elenco di \] *trasformazioni* del *pacchetto* u m<br/> oppure <br/> \[\| \] *pacchetto* u m/g *LanguageID*<br/> | Annuncia un prodotto. Questa opzione Ignora tutti i valori di proprietà immessi nella riga di comando. u annuncia l'utente corrente.<br/> m annunciare a tutti gli utenti del computer.<br/> identificatore di lingua g<br/> t applica la trasformazione al pacchetto annunciato.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe/I Office9.msi/t ProgramMgmt. MST                                                                                                  | Specifica il file con estensione msi che Setup.exe è necessario installare. Se l'opzione/I non è inclusa, Setup.exe usa il file di Office9.msi.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o< = *valore* della proprietà> | setup.exe/o CDKEY = 111111-1111                                                                                                               | Imposta le proprietà nel file con estensione msi. Setup.exe li passa a msiexec come scritto.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe/q                                                                                                                                 | Impostare a livello di interfaccia utente l'installazione. /q nessuna interfaccia utente (/qn per msiexec.)/QB interfaccia utente Basic<br/> interfaccia utente/QR ridotta.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe/M4                                                                                                                                | Supporta più licenze in base ai contratti selezionati. Questa proprietà viene usata in dall'azione personalizzata di verifica della licenza per scrivere il certificato LV. L'opzione/m deve essere seguita dal numero di sbloccamenti consentiti. Il valore specificato dall'opzione/m deve essere impostato come proprietà "M" nel file Office9.msi. Se non viene specificato alcun valore, ma con il programma di installazione viene utilizzata l'opzione/m, è necessario impostare il valore 0. L'opzione/m è necessaria per supportare i clienti selezionati che usano un CD o una rete. |
| /Settings                    | setup.exe/Settings mysettings.ini                                                                                                           | Consente agli amministratori di specificare un file ini contenente tutte le impostazioni personalizzate da passare durante l'installazione di Office 2000. Vedere la descrizione del file con estensione INI riportata di seguito.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Uso di un file ini

La creazione di un file di inizializzazione può risultare più semplice rispetto alla creazione di una riga di comando lungo. Utilizzando l'opzione/Settings, l'applicazione Setup.exe legge il file ini specificato e crea una riga di comando da passare all'applicazione Msiexec.exe. Nel file ini sono supportate solo le proprietà supportate nella riga di comando. Se una proprietà o un valore viene trovato sia nel file ini che nella riga di comando, le impostazioni della riga di comando eseguono l'override delle impostazioni del file ini.

Il formato del file ini è il seguente:

\[MSI\]

 

\[MST\]

 

\[options\]

 

\[Schermo\]

La \[ \] sezione MSI del file ini specifica il percorso del pacchetto di installazione per l'installazione. Corrisponde all'opzione/I nella riga di comando.

La \[ \] sezione MST del file ini specifica il percorso delle trasformazioni utilizzate con questa installazione. Corrisponde all'opzione/j nella riga di comando. Ogni trasformazione è indicata in una riga diversa, usando la velocità effettiva MST1 (N). Quando viene analizzato nella riga di comando, l'elenco nel file ini viene trasformato da sinistra a destra. Si noti che il numero associato al titolo MST (N) è presente solo per gestire identificatori univoci e non ha un significato programmatico.

La \[ \] sezione Opzioni consente agli amministratori di rete di impostare ed eseguire l'override delle proprietà nei file con estensione msi o MST. Le opzioni impostate nel file ini vengono aggiunte alla riga di comando utilizzando l'opzione/o. Ogni opzione nella sezione Option deve avere un nome di proprietà e un valore.

La \[ \] sezione di visualizzazione viene utilizzata per impostare il livello di interfaccia utente utilizzato durante l'installazione. Corrisponde all'opzione/q nella riga di comando. I valori validi sono None, Basic, Reduced e Full.

File Sample. ini

\[Identità del servizio gestita\]

 

MSI = \\ \\ sourceshare \\ office2000 \\Office2000.msi

 

\[MST\]

 

MST1 = \\ \\ sourceshare \\ office2000 \\ trns1. MST

 

MST2 = \\ \\ sourceshare \\ office2000 \\ trns2. MST

 

\[Opzioni\]

 

PUBLICPROPERTY = valore

\[Schermo\]

 

Visualizzazione = nessuna

 

