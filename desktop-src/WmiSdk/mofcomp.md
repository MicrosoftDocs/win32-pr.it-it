---
description: Il compilatore Managed Object Format (MOF) analizza un file contenente istruzioni MOF e aggiunge le classi e le istanze di classe definite nel file al repository WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879969"
---
# <a name="mofcomp"></a>mofcomp

Il compilatore [*Managed Object Format (MOF)*](gloss-m.md) analizza un file contenente istruzioni MOF e aggiunge le classi e le istanze di classe definite nel file al repository WMI. I file MOF vengono in genere compilati automaticamente durante l'installazione dei sistemi con cui vengono forniti, ma è anche possibile compilare file MOF utilizzando questo strumento.

Per ulteriori informazioni sull'individuazione e sull'utilizzo di mofcomp.exe, vedere [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)). Per informazioni sulla rimozione di classi e istanze dal repository WMI, vedere il comando per il preprocessore [**pragma deleteclass**](pragma-deleteclass.md) .

Nell'esempio di codice seguente viene illustrato come eseguire il compilatore MOF in un file.

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a>Commutatori

<dl> <dt>

<span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-recupero automatico**
</dt> <dd>

Aggiunge il file MOF denominato all'elenco di file compilati durante il ripristino del repository. L'elenco dei file MOF di recupero automatico è archiviato nella chiave del registro di sistema:

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**

I file MOF elencati in questa voce del registro di sistema devono trovarsi nel computer locale perché i file MOF che usano il comando **autocover** non possono ripristinare i file MOF presenti in un computer remoto.

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e viene riavviato, usare l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) nel file [*Managed Object Format*](gloss-m.md) (MOF).

 

</dd> <dt>

<span id="-check"></span><span id="-CHECK"></span>**-controllo**
</dt> <dd>

Richiede che il compilatore esegua solo una verifica della sintassi e visualizzi i messaggi di errore appropriati. Non è possibile usare altre opzioni con questa opzione. Quando si utilizza questa opzione, non viene stabilita alcuna connessione a Strumentazione gestione Windows (WMI) e non vengono apportate modifiche al repository WMI.

</dd> <dt>

<span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _namespacePath_*_>_*
</dt> <dd>Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacePath*. Il file MOF compilato viene caricato nello spazio dei nomi mofcomp predefinito, \\ valore predefinito radice, a meno che non venga usata questa opzione. È anche possibile inserire lo **\# spazio dei nomi pragma** del comando per il preprocessore ("_percorso dello spazio dei nomi_*_")_* nel file MOF per ottenere lo stesso effetto. Se vengono usati sia l'opzione **-N:** che il \# comando <a href="pragma-namespace.md">pragma namespace</a> , il \# **pragma namespace** **autocover** ha la priorità. In questo caso, l'unico modo per compilare il file MOF in un altro spazio dei nomi consiste nel modificare il file MOF e modificare il \# comando **pragma namespace** . È possibile specificare un computer remoto utilizzando \\ \\ MachineName \\ root \\ default.</dd> <dt>

<span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Classe: createonly**
</dt> <dd>

Richiede che il compilatore non modifichi le classi esistenti. Quando si utilizza questa opzione, l'operazione di compilazione termina se esiste già una classe specificata nel file MOF.

</dd> <dt>

<span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Classe: ForceUpdate**
</dt> <dd>

Forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto. Si supponga, ad esempio, che un qualificatore di classe venga definito in una classe figlio e che la classe base tenti di aggiungere lo stesso qualificatore. In **-Class: ForceUpdate** Mode, il compilatore MOF risolve il conflitto eliminando il qualificatore in conflitto nella classe figlio. Se la classe figlio dispone di istanze, l'aggiornamento forzato avrà esito negativo.

</dd> <dt>

<span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-Classe: safeupdate**
</dt> <dd>

Consente di aggiornare le classi anche se sono presenti classi figlio, purché la modifica non causi conflitti con le classi figlio. Questo flag, ad esempio, consente di aggiungere una nuova proprietà alla classe di base non citata in precedenza nelle classi figlio. Se le classi figlio hanno istanze, l'aggiornamento avrà esito negativo.

</dd> <dt>

<span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-Classe: updateonly**
</dt> <dd>

Richiede che il compilatore non crei nuove classi. Quando si utilizza questa opzione, l'operazione di compilazione termina se non esiste una classe specificata nel file MOF.

</dd> <dt>

<span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-istanza: updateonly**
</dt> <dd>

Richiede che il compilatore non crei nuove istanze. Quando si utilizza questa opzione, l'operazione di compilazione termina se non esiste un'istanza specificata nel file MOF.

</dd> <dt>

<span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-istanza: createonly**
</dt> <dd>

Richiede che il compilatore non modifichi le istanze esistenti. Quando si utilizza questa opzione, l'operazione di compilazione termina se un'istanza specificata nel file MOF esiste già.

</dd> <dt>

<span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _filename_*_>_*
</dt> <dd>

Richiede che il compilatore crei una versione binaria del file MOF con il nome *filename* senza apportare alcuna modifica al repository WMI.

Se si usa l'opzione **-B: <** _filename_ *_>_* per creare un file MOF binario, solo le versioni dei qualificatori predefinite vengono archiviate nel repository WMI.

Il formato MOF binario è il formato intermedio per combinare un driver WDM con il file MOF come risorsa. Il MOF binario rappresenta le classi e le istanze come un file MOF di testo e viene compresso prima di essere archiviato su disco.

</dd> <dt>

<span id="-WMI"></span><span id="-wmi"></span>**-WMI**
</dt> <dd>

Richiede che il compilatore esegua un controllo della sintassi WMI. Con questa opzione è necessario usare l'opzione **-B:** . L'opzione **-WMI** viene utilizzata solo per la compilazione di file MOF binari per l'utilizzo da parte dei driver di dispositivo WDM. Questa opzione richiama un controllo file MOF binario separato, che viene eseguito dopo la creazione del file MOF binario.

</dd> <dt>

<span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: <** _password_*_>_*
</dt> <dd>

Specifica *la password per* l'utente del computer da immettere al momento dell'accesso.

</dd> <dt>

<span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:** _nome utente_ <*_>_*
</dt> <dd>

Specifica *username* come nome dell'utente che ha effettuato l'accesso.

</dd> <dt>

<span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: <** _autorità_*_>_*
</dt> <dd>

Specifica l' *autorità* come autorità (nome di dominio) da usare per l'accesso a WMI.

</dd> <dt>

<span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:** _percorso_ <*_>_*
</dt> <dd>

Nome dell'output indipendente dalla lingua. Utilizzato con l'opzione **-emendamento** per specificare il nome del file MOF indipendente dalla lingua che verrà generato.

</dd> <dt>

<span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:** _percorso_ <*_>_*
</dt> <dd>

Nome dell'output specifico del linguaggio. Utilizzato con l'opzione **-emendamento** per specificare il nome del file MOF specifico della lingua che verrà generato.

</dd> <dt>

<span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Modifica:** _impostazioni locali_ <*_>_*
</dt> <dd>

Suddivide il file MOF in versioni specifiche della lingua e indipendenti dalla lingua. Il compilatore MOF crea una forma indipendente dal linguaggio del file MOF con tutti i qualificatori modificati rimossi. Viene creata anche una versione localizzata del file MOF con un'estensione di file MFL. Il parametro *locale* specifica il nome dello spazio dei nomi figlio che contiene le definizioni di classe localizzate. Il formato del parametro delle *impostazioni locali* è MS \_ xxx, dove xxx è il valore esadecimale dell'LCID di Windows. Ad esempio, le impostazioni locali per l'inglese americano sono MS \_ 409.

</dd> <dt>

<span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _resourceName_*_>_*
</dt> <dd>

Estrae MOF binario da una risorsa denominata. Questa opzione ottiene il file MOF binario dalla classe nel repository WMI mentre l'opzione-B crea il formato MOF binario da un file MOF.

</dd> <dt>

<span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _ResourceLocale_*_>_*
</dt> <dd>

facoltativo. Estrae le descrizioni MOF localizzate dal MOF binario quando viene usato con l'opzione-ER.

</dd> <dt>

<span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*
</dt> <dd>

Nome del file da analizzare.

</dd> </dl>

## <a name="return-values"></a>Valori restituiti

Come prima operazione, il compilatore MOF esegue un controllo della sintassi sul file MOF. Se il compilatore rileva errori, viene stampato un messaggio di errore e il processo viene terminato.

Il compilatore MOF può restituire i valori seguenti:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Operazione di compilazione MOF completata.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Il compilatore MOF non è riuscito a connettersi al server WMI. Questo problema si verifica a causa di un errore semantico, ad esempio un'incompatibilità con il repository WMI esistente, oppure un errore effettivo, ad esempio l'avvio del server WMI.

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Una o più opzioni della riga di comando non sono valide.

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

Si è verificato un errore di sintassi MOF.

</dd> </dl>

Se il file MOF viene analizzato correttamente, ma viene effettuato un tentativo di eseguire un'operazione non consentita da un'opzione della riga di comando, il compilatore restituisce un codice di errore generato da WMI anziché uno dei codici restituiti elencati nell'elenco precedente. Ad esempio, viene restituito un codice di errore WMI quando viene specificata l'opzione **-instance: updateonly** e il file MOF tenta di creare un'istanza.

Se l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) non è presente nel file, viene restituito l'avviso seguente:

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a>Commenti

Il compilatore MOF è disponibile nella directory% windir% \\ system32 \\ WBEM. È necessario specificare il file MOF come parametro del compilatore MOF. È anche possibile specificare un'opzione di recupero automatico se si vuole che il file MOF venga ricompilato automaticamente se il repository CIM deve essere recuperato automaticamente. Per ulteriori informazioni, digitare **mofcomp/?** al prompt dei comandi.

Un file MOF che utilizza il set di caratteri Unicode contiene una firma come i primi due byte del file. Questa firma è U + FFFE o U + FEFF, a seconda dell'ordine dei byte del file.

Quando non si verificano errori nel processo di analisi, il compilatore MOF si connette al server WMI in esecuzione nel computer locale, a meno che non sia stata specificata l'opzione **-Check** . Le classi e le istanze definite nel file MOF vengono aggiunte al repository WMI.

Quando si verifica un errore durante l'aggiornamento del repository WMI, il compilatore non esegue alcun tentativo di riportare il repository allo stato precedente all'inizio dell'elaborazione del compilatore.

**Windows 8:** Quando si installa un provider, mofcomp considera la \[ chiave \] e i \[ \] qualificatori statici come true se sono presenti, indipendentemente dai valori effettivi. Altri qualificatori vengono considerati false se sono presenti ma non sono impostati in modo esplicito su true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**spazio dei nomi pragma**](pragma-namespace.md)
</dt> <dt>

[Compilazione di file MOF](compiling-mof-files.md)
</dt> <dt>

[Compilazione di file MOF localizzati](compiling-localized-mof-files.md)
</dt> <dt>

[Registrazione di un provider](registering-a-provider.md)
</dt> <dt>

[**IMOFCompiler:: CompileFile**](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

