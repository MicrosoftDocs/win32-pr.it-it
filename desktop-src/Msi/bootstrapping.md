---
description: Attualmente ogni installazione che tenta di usare il programma di installazione di Windows inizia verificando se il programma di installazione è presente nel computer dell'utente e, se non è presente, se l'utente e il computer sono pronti per installare Windows Installer.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Bootstrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c590d00fa9d6ac63f93caa287f34b9f2bf25357bd36ab9ea3fb9ce87e81291d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145714"
---
# <a name="bootstrapping"></a>Bootstrap

Attualmente ogni installazione che tenta di usare il programma di installazione di Windows inizia verificando se il programma di installazione è presente nel computer dell'utente e, se non è presente, se l'utente e il computer sono pronti per installare Windows Installer. Un'applicazione [diInstmsi.exe](instmsi-exe.md) è disponibile con Windows Installer SDK che contiene tutta la logica e tutte le funzionalità per installare Windows programma di installazione. Tuttavia, un'applicazione di bootstrap deve gestire questa installazione.

L'applicazione di bootstrap deve prima verificare se il Windows è attualmente installato. Le applicazioni possono ottenere la versione di Windows di installazione attualmente installata usando [**DllGetVersion.**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc) Se Windows programma di installazione non è attualmente installato, l'applicazione di bootstrap deve eseguire una query sul sistema operativo per determinare la versione del Instmsi.exe richiesta. Dopo l'avvio dell'installazione di Windows Installer, l'applicazione di bootstrap deve gestire i codici restituiti dall'applicazione Instmsi.exe e gestire eventuali riavvii che si verificano durante l'installazione del programma di Windows. Per altre informazioni, vedere [Determining the Windows Installer Version](determining-the-windows-installer-version.md)

L'esempio seguente illustra come l'applicazione di installazione che installa Microsoft Office 2000 controlla il sistema dell'utente e configura l'installazione Windows programma di installazione. Questo esempio è scritto specificamente per installare Office 2000 e deve essere usato solo come riferimento generale.

Quando un utente inserisce un CD-ROM di Office 2000 nel computer, Setup.exe tenta di avviare la modalità di manutenzione, l'applicazione di installazione o non esegue alcuna operazione, in base alle esigenze dell'utente. La sezione seguente descrive come l'applicazione di installazione di Office 2000, denominata Setup.exe, qualifica l'utente e il relativo computer, costruisce una riga di comando e installa il programma di installazione di Windows usando l'applicazione Msiexec.exe.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Come Setup.exe bootstrap del programma Windows durante l'installazione Office 2000

1.  L'utente inserisce Office CD-ROM 2000 nel computer. Il Windows operativo avvia Setup.exe usando l'opzione /autorun e il file Autorun.inf. Il file Autorun.inf si trova nella radice del CD-ROM Office 2000 e contiene le sezioni seguenti:

    \[Autorun\]

     

    \[Office Caratteristiche\]

     

    \[Informazioni sul prodotto\]

     

    \[ServicePack \] .

    La sezione Esecuzione automatica contiene una riga di comando che esegue l'applicazione Setup.exe, esegue l'icona usata per visualizzare il disco e contiene informazioni per aggiungere un'opzione "Installa" e un'opzione "Configura" al menu di scelta rapida per il \[ \] CD-ROM.

    La Office funzionalità contiene un elenco di caratteristiche \[ e coppie di nomi di \] funzionalità.

    La \[ sezione Product Information specifica il nome e la versione \] dell'applicazione.

    La \[ sezione ServicePack \] consente a un amministratore di rete di impostare il livello minimo di Service Pack richiesto. L'amministratore di rete può utilizzare questa sezione per creare il testo di un messaggio di avviso visualizzato se il sistema operativo locale non dispone del Service Pack richiesto.

    Di seguito è riportato un esempio di Autorun.inf.

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

2.  Il Setup.exe verifica la presenza del \_ mutex MsiPromptForCD. Windows Il programma di installazione crea questo mutex quando richiede all'utente di inserire il CD-ROM. La presenza del mutex indica che Windows installer sta eseguendo un'installazione che ha richiesto il CD-ROM Office 2000. In questo caso, l'Setup.exe viene chiusa immediatamente e consente al Office 2000 di continuare l'installazione. Se il mutex è assente, l'applicazione Setup.exe continua al passaggio 3 in cui viene valutata una chiave del Registro di sistema per determinare se Office 2000 è installato.
3.  L'Setup.exe verifica la presenza della chiave del Registro di sistema di Office9:

    **HKCU/Software/Microsoft/Office/9.0/Common/General/InstallProductID**

    Se questa chiave del Registro di sistema non esiste, l'applicazione Setup.exe continua al passaggio 6 in cui viene controllato il sistema operativo per determinare se è qualificata per l'installazione di Office 2000.

4.  Se la chiave Office 2000 esiste, l'applicazione Setup.exe controlla lo stato di installazione corrente chiamando [**MsiQueryProductState.**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) Lo stato restituito InstallState Default indica che Office 2000 è già installato e che l'applicazione Setup.exe continua al passaggio 5 in cui viene verificata l'esecuzione di \_ Office 2000 dall'origine.

    Se Office 2000 non è installato, l'applicazione Setup.exe continua al passaggio 6 in cui viene controllato il sistema operativo per determinare se è qualificata per l'installazione di Office 2000.

5.  LSetup.exe appliazione chiama [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) per ognuna delle funzionalità nella sezione **\[ OfficeFeatures \]** del file Autorun.inf. Se una di queste funzionalità restituisce INSTALLSTATE SOURCE, significa che la funzionalità viene eseguita dall'origine e che \_ lSetup.exe appliazione viene chiusa immediatamente.

    Se nessuna delle funzionalità restituisce INSTALLSTATE SOURCE, l'applicazione Setup.exe avvia l'applicazione del programma di installazione Msiexec.exe e presenta la modalità di manutenzione Windows Installer prima di \_ uscire.

6.  LSetup.exe app applicazione determina se il sistema operativo è qualificato per un'installazione di Office 2000. Windows XP è necessario per installare Office 2000. Se il sistema operativo richiede un aggiornamento del Service Pack per qualificarsi per Office 2000, l'applicazione Setup.exe visualizza il testo specificato nel file Autorun.inf. Se il sistema operativo non è idoneo per Office 2000 o per un aggiornamento di Office 2000, l'applicazione Setup.exe visualizza un messaggio che impedisce all'utente di continuare.

    Se il sistema operativo è qualificato per Office 2000, l'applicazione Setup.exe continua al passaggio 7, che determina se il programma di installazione di Windows è installato nel computer dell'utente.

7.  Se Windows Installer esiste nel computer dell'utente, l'applicazione Setup.exe avvia l'applicazione Msiexec.exe e vi passa il file .msi Office 2000.

    Se Windows non è installato nel computer locale, l'applicazione Setup.exe continua al passaggio 8, determinando se il sistema operativo è qualificato per l'installazione Windows installato.

8.  Se il computer locale è idoneo per l'installazione di Windows, l'applicazione Setup.exe esegue la versione corretta dell'applicazione del programma di installazione Instmsi.exe per la piattaforma. Setup.exe possibile passare l'opzione della riga di comando "/q" per eliminare l'interfaccia utente e impedire all'utente di modificare le opzioni di configurazione dell'installazione.
9.  L'Setup.exe carica il file Msi.dll appena installato ed esegue una chiamata alla funzione [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) per installare l'applicazione dell'utente.

## <a name="setupexe-command-line-parameters"></a>Setup.exe della riga di comando

LSetup.exe app applicazione consente agli amministratori e agli utenti di passare le opzioni della riga di comando allMsiexec.exe app Msiexec.exe applicazione. Per altre informazioni, vedere [Opzioni della riga di comando.](command-line-options.md) Nella tabella seguente sono elencate le opzioni di comando che è possibile usare con Setup.exe.



| Opzione                       | Utilizzo                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe /autorun                                                                                                                           | Esegue il file Autorun.inf descritto in precedenza.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Avvia un'installazione amministrativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[u \| m \] *Pacchetto* o <br/> \[u \| m \] *Package* /t *Transform List*<br/> oppure <br/> \[u \| m \] *Package* /g *LanguageID*<br/> | Annuncia un prodotto. Questa opzione ignora tutti i valori delle proprietà immessi nella riga di comando. u Annunciare all'utente corrente.<br/> m Annunciare a tutti gli utenti del computer.<br/> g Identificatore di lingua<br/> t Applica la trasformazione al pacchetto annunciato.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe /I Office9.msi /t ProgramMgmt.mst                                                                                                  | Specifica il .msi file da Setup.exe installare. Se l'opzione /I non è inclusa, Setup.exe il file Office9.msi.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o<*valore della* = *proprietà*> | setup.exe /o CDKEY=111111-1111                                                                                                               | Imposta le proprietà nel file .msi. Setup.exe li passa a msiexec come scritto.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe /q                                                                                                                                 | Impostare il livello dell'interfaccia utente per l'installazione. /q nessuna interfaccia utente (/qn per msiexec.) /qb interfaccia utente di base<br/> /qr ha ridotto l'interfaccia utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe /m4                                                                                                                                | Supporta più licenze in base ai contratti Select. Questa proprietà viene usata in dall'azione personalizzata Verifica licenza per scrivere il certificato LV. L'opzione /m deve essere seguita dal numero di sblocci consentiti. Il valore specificato dall'opzione /m deve essere impostato come proprietà "M" nel file Office9.msi. Se non viene specificato alcun valore, ma l'opzione /m viene usata con il programma di installazione, è necessario impostare il valore 0. L'opzione /m è necessaria per supportare Selezionare i clienti che usano un CD o una rete. |
| /settings                    | setup.exe /settings mysettings.ini                                                                                                           | Consente agli amministratori di specificare .ini file contenente tutte le impostazioni personalizzate da passare durante Office 2000. Vedere la descrizione del file .ini seguente.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Uso di un .ini file

La creazione di un file di inizializzazione può essere più semplice rispetto alla creazione di una lunga riga di comando. Usando l'opzione /settings, l'applicazione Setup.exe legge il file .ini specificato e costruisce una riga di comando da passare all'applicazione Msiexec.exe specificata. Solo le proprietà supportate nella riga di comando sono supportate nel file .ini. Se viene trovata una proprietà o un valore sia nel file .ini che nella riga di comando, le impostazioni della riga di comando sostituiscono le impostazioni .ini file.

Il formato del file .ini è il seguente:

\[Msi\]

 

\[Mst\]

 

\[options\]

 

\[Schermo\]

La \[ sezione msi del file .ini specifica il percorso del pacchetto di installazione per \] l'installazione. Corrisponde all'opzione /I nella riga di comando.

La \[ sezione mst \] del file .ini specifica il percorso delle trasformazioni usate con questa installazione. Corrisponde all'opzione /j nella riga di comando. Più trasformazioni sono indicate ognuna su una riga diversa, usando MST1 MST(N). Quando viene analizzato nella riga di comando, l'elenco nel file .ini viene trasformato da sinistra a destra. Si noti che il numero associato al titolo MST(N) è presente solo per mantenere identificatori univoci e non ha alcun significato a livello di codice.

La sezione options consente agli amministratori di rete di impostare ed eseguire l'override delle proprietà \[ nei file .msi o \] mst. Le opzioni impostate nel file .ini vengono aggiunte alla riga di comando usando l'opzione /o. Ogni opzione nella sezione option deve avere un nome di proprietà e un valore.

La \[ sezione Display viene usata per impostare il livello \] dell'interfaccia utente usato durante l'installazione. Corrisponde all'opzione /q nella riga di comando. I valori validi sono none, basic, reduced e full.

File di .ini di esempio

\[Identità del servizio gestita\]

 

MSI= \\ \\ condivisione di origine \\ Office2000 \\Office2000.msi

 

\[Mst\]

 

MST1= \\ \\ sourceshare \\ Office2000 \\ trns1.mst

 

MST2= \\ \\ sourceshare \\ Office2000 \\ trns2.mst

 

\[Opzioni\]

 

PUBLICPROPERTY=valore

\[Schermo\]

 

Display=None

 

