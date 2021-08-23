---
description: Questo argomento illustra le istruzioni di programmazione per l'individuazione delle stringhe del Registro di sistema reindirizzate. Per altre informazioni, vedere Uso del reindirizzamento delle stringhe del Registro di sistema.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Individuazione di stringhe reindirizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c4e1a46b2c12af839e4c5b562eba18a80c8e814e5a6071dca925a14a46d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788481"
---
# <a name="locating-redirected-strings"></a>Individuazione di stringhe reindirizzate

Questo argomento illustra le istruzioni di programmazione per l'individuazione delle stringhe del Registro di sistema reindirizzate. Per altre informazioni, vedere [Uso del reindirizzamento delle stringhe del Registro di sistema.](using-registry-string-redirection.md)

## <a name="load-a-language-neutral-registry-value"></a>Caricare un valore Language-Neutral Registro di sistema

In Windows Vista e versioni successive, l'applicazione MUI usa un valore del Registro di sistema indipendente dalla lingua per consentire l'accesso alle stringhe specifiche della lingua archiviate in una tabella di risorse di tipo stringa. Per altre informazioni, vedere Creare una risorsa Language-Neutral in [Uso del reindirizzamento delle stringhe del Registro di sistema.](using-registry-string-redirection.md)

Il codice dell'applicazione che legge il valore indipendente dalla lingua dal Registro di sistema deve caricare le stringhe nella lingua corretta dell'interfaccia utente chiamando [**RegLoadMUIStringW.**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) Se si usa questa funzione, l'applicazione non deve gestire in modo esplicito il caricamento delle risorse.

Se si aggiorna un'applicazione esistente in base all'uso indipendente dalla lingua del Registro di sistema, in genere si manteneranno i valori stringa esistenti, localizzati in inglese o in un'altra lingua nel Registro di sistema, come fallback e per compatibilità con le versioni precedenti. Mantenere una stringa letterale nel Registro di sistema consente all'applicazione di eseguire il fall back alla stringa letterale se una chiamata a [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) ha esito negativo. È necessario decidere come implementare tale fallback, perché MUI non fornisce supporto per tale implementazione.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Usare l'API shell per impostare stringhe di collegamento dal Registro di sistema

L'applicazione può usare l'API shell per creare stringhe per i collegamenti che collegano file o cartelle nel menu **Start** o sul desktop. Per altre informazioni, vedere Creare risorse per le stringhe di collegamento in [Uso del reindirizzamento delle stringhe del Registro di sistema.](using-registry-string-redirection.md)

L'applicazione può [**usare SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) per caricare il nome visualizzato conforme a MUI per un collegamento. Deve usare [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) per impostare la descrizione comandi associata. Le chiamate registrano le stringhe con il Registro di sistema. Si considerino gli esempi seguenti, per i quali "HKCR" rappresenta la chiave del Registro di sistema HKEY \_ CLASSES \_ ROOT:


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



La prima riga fornisce una stringa letterale non localizzata per la compatibilità con le versioni precedenti e di fallback. La seconda riga mostra il modo conforme a MUI per registrare il nome visualizzato. Questa riga indica l'identificatore di stringa 104 archiviato in Msascui.exe (per Windows XP) o nel file specifico della lingua associato (per Windows Vista). Questo identificatore di stringa corrisponde a "Risorse di rete". La terza riga dell'esempio gestisce la registrazione del suggerimento informazioni. %CLSID AntiSpyware% specifica una variabile di ambiente che rappresenta il \_ GUID corrispondente all'identificatore di classe di questo componente.

Per l'esempio illustrato in precedenza, l'applicazione chiama [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) per specificare il percorso del file eseguibile per i primi due parametri e *specificare idsRes* come "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,104". Una chiamata a [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)specifica il percorso della descrizione comandi come "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,208".

## <a name="query-friendly-document-type-names-in-the-registry"></a>Nomi descrittivi dei tipi di documento nel Registro di sistema

La creazione di risorse per i nomi descrittivi dei tipi di documento è descritta in Creare risorse per nomi descrittivi dei tipi di documento in [Uso del reindirizzamento delle stringhe del Registro di sistema.](using-registry-string-redirection.md) Per eseguire una query su un nome di documento descrittivo, l'applicazione deve usare [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init), seguito da una chiamata a [**IQueryAssociations::GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring). La chiamata a **IQueryAssociations::Init** specifica il tipo di documento, ad esempio ".txt". La chiamata a **IQueryAssociations::GetString** deve specificare ASSOCSTR \_ FRIENDLYDOCNAME come identificatore di stringa.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Registrare Microsoft Management Console stringhe dello snap-in non lette dal Registro di sistema

L'applicazione può usare uno snap-in Microsoft Management Console (MMC) per ospitare le attività di gestione. La maggior parte delle stringhe viene gestita come risorse usando le impostazioni del Registro di sistema descritte in Create String Resources for Microsoft Management Console Snap-Ins in [Using Registry String Redirection](using-registry-string-redirection.md). Tuttavia, alcuni snap-in registrano valori di stringa del Registro di sistema che MMC non è in grado di leggere dal Registro di sistema. In questo caso, lo snap-in deve ottenere i valori usando [**l'interfaccia ISnapinAbout,**](/windows/win32/api/mmc/nn-mmc-isnapinabout) compatibile con MUI.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Impostare il nome visualizzato e la descrizione per Windows servizio dal Registro di sistema

Se l'applicazione MUI usa un servizio Windows, deve visualizzare il nome visualizzato e la descrizione del servizio. Le risorse associate sono descritte in "Creare risorse stringa per un servizio Windows" in [Uso del reindirizzamento delle stringhe del Registro di sistema.](using-registry-string-redirection.md)

Per impostare il nome visualizzato del servizio, l'applicazione MUI chiama [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig.**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga) Il nome è una stringa nel formato " `@<PE-path>,-<stringID>[;<comment>]` ". Ad esempio, se il servizio viene implementato da un file .dll con percorso %ProgramFiles% %MyPath%MyDll.dll e l'identificatore di stringa del nome visualizzato specifico della lingua è \\ \\ 347, il parametro viene specificato come " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` ". Le doppie barre rovesciate ( ) sono necessarie perché \\ C/C++ usa la barra rovesciata come carattere \\ di escape nelle stringhe.

Per impostare la descrizione del servizio specifica della lingua, l'applicazione MUI deve fare in modo che il membro **lpDescription** di una struttura [**SERVICE \_ DESCRIPTION**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) indichi una stringa nel formato " ", facendo riferimento all'identificatore di `@<PE-path>,-<stringID>[;<comment>]` stringa appropriato. L'applicazione chiama [**quindi ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) con il parametro *dwInfoLevel* specificato come SERVICE CONFIG DESCRIPTION e il parametro \_ \_ *lpInfo* specificato come **struttura SERVICE \_ DESCRIPTION.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione delle risorse PE Win32](locating-win32-pe-resources.md)
</dt> <dt>

[Uso del reindirizzamento delle stringhe del Registro di sistema](using-registry-string-redirection.md)
</dt> </dl>

 

 
