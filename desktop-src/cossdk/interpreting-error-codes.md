---
description: Interpretazione dei codici di errore
ms.assetid: df2fe03b-2f5f-4958-926f-17e3a025a9b5
title: Interpretazione dei codici di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659ee7def9feff50d375a07ab201e1cca25bffd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304824"
---
# <a name="interpreting-error-codes"></a>Interpretazione dei codici di errore

Dopo aver individuato l'applicazione che rappresenta l'origine di un problema, è necessario individuare l'errore che si è verificato. Gli errori vengono generati e segnalati in formati diversi, a seconda del linguaggio usato dall'applicazione.

In Microsoft Visual C++ i valori di esito positivo, avviso e errore vengono restituiti utilizzando un numero a 32 bit noto come **HRESULT**. Per un elenco di valori **HRESULT** definiti dal sistema, vedere il file di intestazione Winerror. h incluso nel Windows SDK. Questo file include tutti i codici di errore e le descrizioni di COM+. Per ulteriori informazioni sui valori **HRESULT** , vedere [gestione degli errori](/windows/desktop/com/error-handling-in-com).

Nel linguaggio Java viene generata un'istanza di com. ms. com. ComFailException per indicare un errore, in cui l'oggetto ComFailException specifica un valore **HRESULT**. Un'istanza di com. ms. com. ComSuccessException indica l'esito positivo con un valore restituito false. Per informazioni sull'interpretazione di queste eccezioni, vedere la documentazione di Microsoft Visual J++.

> [!Note]  
> I processi del server applicazioni COM+ che ospitano oggetti Visual J++ non verranno inattivi (anche con zero oggetti attivi), a meno che non si spenga il debug JIT nell'IDE di VJ6. Per informazioni su come eseguire questa operazione, vedere la documentazione di Visual J++.

 

In Visual Basic, è possibile recuperare i valori **HRESULT** esaminando la proprietà Err. Number. Una descrizione dell'errore può essere recuperata con la proprietà Err. Description.

È anche possibile usare l'utilità ERRLOOK in Microsoft Visual Studio per recuperare un messaggio di errore di sistema o un messaggio di errore del modulo. ERRLOOK recupera automaticamente il testo del messaggio di errore se si trascina un valore esadecimale o decimale dal debugger di Visual Studio o da un'altra applicazione abilitata per l'automazione. È anche possibile immettere un valore digitando o incollando il valore dagli Appunti dell'IDE e facendo clic sull'opzione **Cerca** .

Il metodo C++ seguente stampa una descrizione dell'errore, in base all' **HRESULT** di input.


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>

void ErrorDescription(HRESULT hr) 
{ 
     if(FACILITY_WINDOWS == HRESULT_FACILITY(hr)) 
         hr = HRESULT_CODE(hr); 
     TCHAR* szErrMsg; 

     if(FormatMessage( 
       FORMAT_MESSAGE_ALLOCATE_BUFFER|FORMAT_MESSAGE_FROM_SYSTEM, 
       NULL, hr, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), 
       (LPTSTR)&szErrMsg, 0, NULL) != 0) 
     { 
         _tprintf(TEXT("%s"), szErrMsg); 
         LocalFree(szErrMsg); 
     } else 
         _tprintf( TEXT("[Could not find a description for error # %#x.]\n"), hr); 
}
```



Nella tabella seguente vengono fornite le descrizioni dei codici di errore comuni in COM+.



| Codici di errore                                                   | Definizioni                                                                                                                                                                                                      |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMAdmin \_ E \_ ALREADYINSTALLED<br/>                      | L'oggetto è già registrato.<br/>                                                                                                                                                                     |
| \_file app COMAdmin E \_ \_ \_ READFAIL<br/>                   | Errore durante la lettura del file dell'applicazione.<br/>                                                                                                                                                          |
| versione del \_ \_ file dell'app E \_ del COMAdmin \_<br/>                    | Numero di versione non valido nel file dell'applicazione.<br/>                                                                                                                                                           |
| \_file app COMAdmin E \_ \_ \_ WRITEFAIL<br/>                  | Si è verificato un errore durante la scrittura nel file dell'applicazione.<br/>                                                                                                                                                       |
| COMAdmin \_ E \_ APPDIRNOTFOUND<br/>                        | Impossibile trovare la directory di installazione dell'applicazione.<br/>                                                                                                                                                          |
| \_applicazione COMQC \_ E \_ non \_ accodata<br/>                 | È possibile creare solo le applicazioni COM+ contrassegnate come "in coda" utilizzando il moniker "Queue".<br/>                                                                                                                      |
| COMAdmin \_ E \_ APPLICATIONEXISTS<br/>                     | L'applicazione è già installata.<br/>                                                                                                                                                                 |
| COMAdmin \_ E \_ applicato \_ corrisponde a \_ CLSID<br/>                | Nel computer è già installato un CLSID con lo stesso GUID del nuovo ID applicazione.<br/>                                                                                                            |
| \_app COMAdmin \_ E \_ non \_ in esecuzione<br/>                     | L'applicazione specificata non è attualmente in esecuzione.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ AUTHENTICATIONLEVEL<br/>                   | Impossibile impostare il livello di autenticazione richiesto per la richiesta di aggiornamento.<br/>                                                                                                                                       |
| COMAdmin \_ E \_ BADPATH<br/>                               | Il percorso del file non è valido.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ BADREGISTRYLIBID<br/>                      | L'ID della libreria dei tipi registrati non è valido.<br/>                                                                                                                                                            |
| COMAdmin \_ E \_ BADREGISTRYPROGID<br/>                     | ProgID del componente mancante o danneggiato.<br/>                                                                                                                                                         |
| COMAdmin \_ E \_ non è in grado di esportare il \_ \_ \_ \_ proxy app<br/>          | Il proxy dell'applicazione non è esportabile.<br/>                                                                                                                                                              |
| COMAdmin \_ E \_ \_ non può \_ avviare l' \_ app<br/>                  | Non è stato possibile avviare l'applicazione perché si tratta di un'applicazione libreria o di un proxy di applicazione.<br/>                                                                                                       |
| COMAdmin \_ E \_ non è in grado di esportare l' \_ \_ \_ \_ app sys<br/>            | L'applicazione di sistema non è esportabile.<br/>                                                                                                                                                             |
| COMAdmin \_ E \_ cant \_ sottoscrivono il \_ \_ componente<br/>        | L'utente non è in grado di sottoscrivere il componente perché potrebbe essere stato importato.<br/>                                                                                                             |
| COMAdmin \_ E \_ CANTCOPYFILE<br/>                          | Si è verificato un errore durante la copia del file.<br/>                                                                                                                                                                   |
| COMAdmin \_ E \_ CLSIDORIIDMISMATCH<br/>                    | I CLSID del file dell'applicazione o IID non corrispondono alle DLL corrispondenti.<br/>                                                                                                                                      |
| spostamento di \_ \_ destinazione non \_ \_ valido \_ per COMAdmin E Comp<br/>                 | Impossibile spostare il componente. l'applicazione di destinazione non esiste più.<br/>                                                                                                                       |
| spostamento di COMAdmin \_ E \_ comp \_ \_ bloccato<br/>                    | Lo spostamento del componente non è consentito perché l'applicazione di origine o di destinazione è un'applicazione di sistema o è attualmente bloccata in caso di modifiche.<br/>                                                |
| COMAdmin \_ E \_ COMPFILE \_ BADTLB<br/>                      | Non è stato possibile caricare la libreria dei tipi.<br/>                                                                                                                                                                 |
| COMAdmin \_ E \_ COMPFILE \_ CLASSNOTAVAIL<br/>               | La DLL non supporta i componenti elencati nella libreria dei tipi.<br/>                                                                                                                                   |
| COMAdmin \_ E \_ COMPFILE \_ DOESNOTEXIST<br/>                | Il file non esiste.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ COMPFILE \_ GETCLASSOBJ<br/>                 | Il metodo [**GetClassObject**](/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject) non è riuscito nella dll.<br/>                                                                                                                |
| COMAdmin \_ E \_ COMPFILE \_ LOADDLLFAIL<br/>                 | Non è stato possibile caricare la DLL.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ COMPFILE \_ noRegistrar<br/>                 | Il registrar del componente a cui si fa riferimento in questo file non è disponibile.<br/>                                                                                                                                     |
| COMAdmin \_ E \_ COMPFILE \_ NOTINSTALLABLE<br/>              | Il file non contiene componenti o informazioni sul componente.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ COREQCOMPINSTALLED<br/>                    | Un componente nella stessa DLL è già installato.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ DLLLOADFAILED<br/>                         | Non è stato possibile caricare la DLL.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ DLLREGISTERSERVER<br/>                     | La funzione [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) non è riuscita durante l'installazione del componente.<br/>                                                                                                  |
| COMAdmin \_ E \_ EVENTCLASS non \_ può \_ essere un \_ Sottoscrittore<br/>      | Una classe di evento non può essere configurata come componente del Sottoscrittore. Quando viene effettuato un tentativo di creare una sottoscrizione con una classe di evento come Sottoscrittore, viene restituito questo errore.<br/>                          |
| COMAdmin \_ E \_ INVALIDUSERIDS<br/>                        | Uno o più utenti nel file dell'applicazione non sono validi.<br/>                                                                                                                                              |
| COMAdmin \_ E \_ mancato<br/>                            | Impossibile trovare l'oggetto nel catalogo.<br/>                                                                                                                                                              |
| \_proxy app COMAdmin E \_ lib non \_ \_ \_ compatibile<br/>         | Le applicazioni e i proxy di applicazione della libreria non sono compatibili. Questo errore viene restituito quando si tenta di esportare un proxy di applicazione e la proprietà di attivazione dell'applicazione è una libreria. <br/> |
| COMAdmin \_ E \_ NOREGISTRYCLSID<br/>                       | Il CLSID del componente è mancante o danneggiato.<br/>                                                                                                                                                          |
| COMAdmin \_ E \_ NOSERVERSHARE<br/>                         | Non è disponibile alcuna condivisione file server.<br/>                                                                                                                                                                    |
| COMAdmin \_ E \_ NOTCHANGEABLE<br/>                         | Le modifiche apportate a questo oggetto e ai relativi oggetti secondari sono state disabilitate.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ NOTDELETEABLE<br/>                         | La funzione Delete è stata disabilitata per questo oggetto.<br/>                                                                                                                                                |
| COMAdmin \_ E \_ NOTINREGISTRY<br/>                         | L'oggetto non è stato trovato nel registro di sistema.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ nouser<br/>                                | Uno o più utenti non sono validi.<br/>                                                                                                                                                                      |
| l'oggetto COMAdmin \_ E non \_ \_ \_ \_ esiste<br/>              | Impossibile trovare uno degli oggetti specificati.<br/>                                                                                                                                                         |
| \_elemento padre dell'oggetto COMAdmin E \_ \_ \_ mancante<br/>               | Uno degli oggetti inseriti o aggiornati non appartiene a una raccolta padre valida.<br/>                                                                                                            |
| COMAdmin \_ E \_ OBJECTERRORS<br/>                          | Errori durante l'accesso a uno o più oggetti. Per ulteriori informazioni, vedere la raccolta [**errorInfo**](errorinfo.md) .<br/>                                                                               |
| COMAdmin \_ E \_ OBJECTEXISTS<br/>                          | L'oggetto che si sta tentando di aggiungere o rinominare esiste già.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ OBJECTINVALID<br/>                         | Una o più proprietà dell'oggetto sono mancanti o non valide.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ OBJECTNOTPOOLABLE<br/>                     | Questo oggetto non può essere in pool.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ PROPERTYSAVEFAILED<br/>                    | Una o più impostazioni delle proprietà non sono valide o sono in conflitto tra loro.<br/>                                                                                                                      |
| OVERFLOW della proprietà COMAdmin \_ E \_ \_<br/>                    | Il valore della proprietà è troppo grande.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ REGFILE \_ danneggiati<br/>                      | Il file di registrazione è danneggiato.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ REGISTERTLB<br/>                           | Il sistema non è stato in grado di registrare la libreria dei tipi.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ REGISTRARFAILED<br/>                       | Si sono verificati errori durante il registro componenti.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ REMOTEINTERFACE<br/>                       | Informazioni sull'interfaccia mancanti o modificate.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ richiede \_ una \_ piattaforma diversa<br/>         | Questa operazione non è abilitata in questa piattaforma.<br/>                                                                                                                                                       |
| \_il ruolo COMAdmin E non \_ \_ \_ \_ esiste<br/>                | Un ruolo assegnato a un componente, un'interfaccia o un metodo non esiste nell'applicazione.<br/>                                                                                                               |
| COMAdmin \_ E \_ ROLEEXISTS<br/>                            | Il ruolo esiste già.<br/>                                                                                                                                                                              |
| COMAdmin \_ E \_ SERVICENOTINSTALLED<br/>                   | Il servizio non è installato.<br/>                                                                                                                                                                         |
| sessione COMAdmin \_ E \_<br/>                               | La versione del catalogo server non è supportata.<br/>                                                                                                                                                          |
| COMAdmin \_ S \_ SOMEALREADYPAUSED<br/>                     | Uno o più processi dell'applicazione specificati sono già stati sospesi.<br/>                                                                                                                               |
| COMAdmin \_ S \_ SOMEALREADYRUNNING<br/>                    | Uno o più processi dell'applicazione specificati erano già in esecuzione.<br/>                                                                                                                              |
| componenti dell' \_ app di avvio E di COMAdmin \_ \_ \_ necessari \_<br/>         | Per avviare l'applicazione, è necessario disporre di componenti in un'applicazione.<br/>                                                                                                                                 |
| COMAdmin \_ E \_ SVCAPP \_ non in \_ pool \_ o \_ riciclabile<br/> | Le applicazioni COM+ eseguite come servizio NT potrebbero non essere contrassegnate come in pool o riciclate.<br/>                                                                                                               |
| COMAdmin \_ E \_ SYSTEMAPP<br/>                             | Impossibile eseguire l'operazione sull'applicazione di sistema.<br/>                                                                                                                                         |
| \_utente COMAdmin \_ E \_ in \_ set<br/>                         | Uno o più utenti sono già assegnati a un set di partizioni locale.<br/>                                                                                                                                      |
| COMAdmin \_ E \_ USERPASSWDNOTVALID<br/>                    | L'identità o la password impostata per l'applicazione non è valida.<br/>                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Criteri di isolamento degli errori e FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Individuazione dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Risoluzione dei problemi](troubleshooting-the-com--crm.md)
</dt> </dl>

 

