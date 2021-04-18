---
description: Questo argomento descrive le istruzioni di programmazione per individuare le stringhe del registro di sistema reindirizzate Per ulteriori informazioni, vedere Utilizzo del reindirizzamento delle stringhe del registro di sistema.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Individuazione di stringhe reindirizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f11600ad57c04de54d914c2c876b67967dfa1467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308702"
---
# <a name="locating-redirected-strings"></a>Individuazione di stringhe reindirizzate

Questo argomento descrive le istruzioni di programmazione per individuare le stringhe del registro di sistema reindirizzate Per ulteriori informazioni, vedere [utilizzo del reindirizzamento delle stringhe del registro di sistema](using-registry-string-redirection.md).

## <a name="load-a-language-neutral-registry-value"></a>Carica un valore del registro di sistema Language-Neutral

In Windows Vista e versioni successive, l'applicazione MUI utilizza un valore del registro di sistema indipendente dalla lingua per consentire l'accesso alle stringhe specifiche della lingua archiviate in una tabella delle risorse di stringa. Per altre informazioni, vedere creare una risorsa Language-Neutral in [uso del reindirizzamento delle stringhe del registro di sistema](using-registry-string-redirection.md).

Il codice dell'applicazione che legge il valore indipendente dalla lingua dal registro di sistema deve caricare le stringhe nella lingua dell'interfaccia utente corretta chiamando [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa). Se si usa questa funzione, l'applicazione non deve gestire in modo esplicito il caricamento delle risorse.

Se si sta aggiornando un'applicazione esistente all'uso indipendente dalla lingua del registro di sistema, in genere si manterranno i valori di stringa esistenti, localizzati in inglese o in un'altra lingua singola nel registro di sistema, come fallback e per compatibilità con le versioni precedenti. Il mantenimento di una stringa letterale nel registro di sistema consente all'applicazione di eseguire il fallback alla stringa letterale se una chiamata a [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) ha esito negativo. È necessario decidere come implementare tale fallback, perché MUI non fornisce alcun supporto per tale implementazione.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Usare l'API shell per impostare le stringhe di collegamento dal registro di sistema

L'applicazione può usare l'API shell per creare stringhe per i collegamenti che collegano file o cartelle nel menu **Start** o sul desktop. Per altre informazioni, vedere creare risorse per le stringhe di collegamento in [uso del reindirizzamento delle stringhe del registro di sistema](using-registry-string-redirection.md).

L'applicazione può usare [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) per caricare il nome visualizzato compatibile con MUI per un collegamento. Per impostare il InfoTip associato, è necessario utilizzare [**IShellLink:: FileDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) . Le chiamate registrano le stringhe con il registro di sistema. Si considerino gli esempi seguenti, per i quali "HKCR" rappresenta la \_ \_ chiave del registro di sistema radice delle classi HKEY:


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



La prima riga fornisce una stringa letterale non localizzata per il fallback e la compatibilità con le versioni precedenti. La seconda riga Mostra il modo conforme a MUI per registrare il nome visualizzato. Questa riga indica l'identificatore di stringa 104 archiviato in Msascui.exe (per Windows XP) o nel file specifico della lingua associato (per Windows Vista). Questo identificatore di stringa corrisponde a "My Network posizioni". La terza riga nell'esempio gestisce la registrazione di InfoTip. % CLSID \_ antispyware% specifica una variabile di ambiente che rappresenta il GUID corrispondente all'identificatore di classe del componente.

Per l'esempio illustrato in precedenza, l'applicazione chiama [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) per specificare il percorso del file eseguibile per i primi due parametri e specificare *idsRes* come "@% ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe, 104". Una chiamata a [**IShellLink:: FileDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)specifica il percorso di infotip come "@% ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe, 208".

## <a name="query-friendly-document-type-names-in-the-registry"></a>Eseguire query sui nomi dei tipi di documento nel registro di sistema

La creazione di risorse per i nomi descrittivi dei tipi di documento è illustrata in creare risorse per i nomi dei tipi di documenti descrittivi in [uso del reindirizzamento delle stringhe](using-registry-string-redirection.md) Per eseguire una query su un nome descrittivo del documento, l'applicazione deve usare [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init), seguito da una chiamata a [**IQueryAssociations:: GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring). La chiamata a **IQueryAssociations:: init** specifica il tipo di documento, ad esempio ". txt". La chiamata a **IQueryAssociations:: GetString** deve specificare ASSOCSTR \_ FRIENDLYDOCNAME come identificatore di stringa.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Registra stringhe di snap-in di Microsoft Management Console non lette dal registro di sistema

L'applicazione può utilizzare uno snap-in di Microsoft Management Console (MMC) per ospitare le attività di gestione. La maggior parte delle stringhe viene gestita come risorse usando le impostazioni del registro di sistema descritte in creare risorse stringa per Microsoft Management Console Snap-Ins in [uso del reindirizzamento delle stringhe del registro di sistema](using-registry-string-redirection.md). Tuttavia, alcuni snap-in registrano i valori stringa del registro di sistema che MMC non è in grado di leggere dal registro di sistema In questo caso, è necessario che lo snap-in ottenga i valori usando l'interfaccia [**ISnapinAbout**](/windows/win32/api/mmc/nn-mmc-isnapinabout) , che è compatibile con MUI.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Impostare il nome visualizzato e la descrizione di un servizio Windows dal registro di sistema

Se l'applicazione MUI usa un servizio Windows, deve visualizzare il nome visualizzato e la descrizione del servizio. Le risorse associate sono descritte in "creare risorse di stringa per un servizio Windows" in [uso del reindirizzamento delle stringhe del registro di sistema](using-registry-string-redirection.md).

Per impostare il nome visualizzato del servizio, l'applicazione MUI chiama [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga). Il nome è una stringa nel formato " `@<PE-path>,-<stringID>[;<comment>]` ". Se, ad esempio, il servizio è implementato da un file con estensione dll con percorso% ProgramFiles% \\ % MyFile% \\MyDll.dll e l'identificatore di stringa del nome visualizzato specifico della lingua è 347, il parametro viene specificato come " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` ". Le barre rovesciate doppie ( \\ \\ ) sono necessarie perché C/C++ usa la barra rovesciata come carattere di escape nelle stringhe.

Per impostare la descrizione del servizio specifica del linguaggio, l'applicazione MUI deve fare in modo che il membro **lpDescription** di una struttura di [**\_ Descrizione del servizio**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) indichi una stringa di formato " `@<PE-path>,-<stringID>[;<comment>]` ", facendo riferimento all'identificatore di stringa appropriato. Quindi, l'applicazione chiama [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) con il parametro *dwInfoLevel* specificato \_ come \_ Descrizione della configurazione del servizio e il parametro *LpInfo* specificato come struttura della **\_ Descrizione del servizio** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione delle risorse PE Win32](locating-win32-pe-resources.md)
</dt> <dt>

[Uso del reindirizzamento delle stringhe del registro di sistema](using-registry-string-redirection.md)
</dt> </dl>

 

 
