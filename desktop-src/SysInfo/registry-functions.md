---
description: Di seguito sono riportate le funzioni del Registro di sistema.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Funzioni del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81f5aff4dad00691f606911c1cf092933aa121eaf7a2d25aacbcc8a83948b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885214"
---
# <a name="registry-functions"></a>Funzioni del Registro di sistema

Di seguito sono riportate le funzioni del Registro di sistema.



| Funzione                                                           | Descrizione                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Recupera le dimensioni correnti del Registro di sistema e le dimensioni massime che il Registro di sistema può ottenere nel sistema.                          |
| [**Regclosekey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Chiude un handle alla chiave del Registro di sistema specificata.                                                                                                 |
| [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Stabilisce una connessione a un handle del Registro di sistema predefinito in un altro computer.                                                                  |
| [**RegCopyTree**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Copia la chiave del Registro di sistema specificata, insieme ai relativi valori e sottochiavi, nella chiave di destinazione specificata.                                        |
| [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Crea la chiave del Registro di sistema specificata.                                                                                                            |
| [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Crea la chiave del Registro di sistema specificata e la associa a una transazione.                                                                       |
| [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Elimina una sottochiave e i relativi valori.                                                                                                               |
| [**RegDeleteKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Elimina una sottochiave e i relativi valori dalla visualizzazione specifica della piattaforma specificata del Registro di sistema.                                                     |
| [**RegDeleteKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Elimina una sottochiave e i relativi valori dalla visualizzazione specifica della piattaforma specificata del Registro di sistema come operazione transazione.                           |
| [**RegDeleteKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Rimuove il valore specificato dalla chiave e dalla sottochiave del Registro di sistema specificate.                                                                        |
| [**RegDeleteTree**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Elimina in modo ricorsivo le sottochiavi e i valori della chiave specificata.                                                                               |
| [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Rimuove un valore denominato dalla chiave del Registro di sistema specificata.                                                                                         |
| [**RegDisablePredefinedCache**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Disabilita la memorizzazione nella cache degli handle per l'handle del Registro di sistema predefinito **per HKEY \_ CURRENT \_ USER** per il processo corrente.                                |
| [**RegDisablePredefinedCacheEx**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Disabilita la memorizzazione nella cache degli handle per tutti gli handle predefiniti del Registro di sistema per il processo corrente.                                                           |
| [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Disabilita la reflection del Registro di sistema per la chiave specificata.                                                                                            |
| [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Abilita la reflection del Registro di sistema per la chiave disabilitata specificata.                                                                                    |
| [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Enumera le sottochiavi della chiave del Registro di sistema aperta specificata.                                                                                     |
| [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Enumera i valori per la chiave del Registro di sistema aperta specificata.                                                                                     |
| [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Scrive tutti gli attributi della chiave del Registro di sistema aperta specificata nel Registro di sistema.                                                                    |
| [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Recupera una copia del descrittore di sicurezza che protegge la chiave del Registro di sistema aperta specificata.                                                        |
| [**RegGetValue**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Recupera il tipo e i dati per il valore del Registro di sistema specificato.                                                                                  |
| [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Crea una sottochiave in **HKEY \_ USERS** o **HKEY \_ LOCAL \_ MACHINE** e archivia le informazioni di registrazione da un file specificato in tale sottochiave. |
| [**RegLoadMUIString**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Carica la stringa specificata dalla chiave e dalla sottochiave specificate.                                                                                  |
| [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Notifica al chiamante le modifiche apportate agli attributi o al contenuto di una chiave del Registro di sistema specificata.                                                   |
| [**RegOpenCurrentUser**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Recupera un handle per la **chiave HKEY \_ CURRENT \_ USER** per l'utente rappresentato dal thread corrente.                                        |
| [**Regopenkeyex**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Apre la chiave del Registro di sistema specificata.                                                                                                              |
| [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Apre la chiave del Registro di sistema specificata e la associa a una transazione.                                                                         |
| [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Recupera un handle per la chiave **HKEY \_ CLASSES \_ ROOT** per l'utente specificato.                                                                  |
| [**RegOverridePredefKey**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Mappe una chiave del Registro di sistema predefinita a una chiave del Registro di sistema specificata.                                                                                    |
| [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Recupera informazioni sulla chiave del Registro di sistema specificata.                                                                                        |
| [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Recupera il tipo e i dati per un elenco di nomi di valori associati a una chiave del Registro di sistema aperta.                                                    |
| [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Determina se la reflection è stata disabilitata o abilitata per la chiave specificata.                                                              |
| [**Regqueryvalueex**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Recupera il tipo e i dati per un nome di valore specificato associato a una chiave del Registro di sistema aperta.                                                   |
| [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Sostituisce il file che contiene una chiave del Registro di sistema e tutte le relative sottochiavi con un altro file.                                                                |
| [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Legge le informazioni del Registro di sistema in un file specificato e le copia sulla chiave specificata.                                                       |
| [**Regsavekey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Salva la chiave specificata e tutte le relative sottochiavi e valori in un nuovo file.                                                                       |
| [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Salva la chiave specificata e tutte le relative sottochiavi e valori in un nuovo file. È possibile specificare il formato per la chiave salvata o l'hive.                 |
| [**RegSetKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Imposta i dati per il valore specificato nella chiave e nella sottochiave del Registro di sistema specificate.                                                                |
| [**RegSetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Imposta la sicurezza di una chiave del Registro di sistema aperta.                                                                                                     |
| [**Regsetvalueex**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Imposta i dati e il tipo di un valore specificato in una chiave del Registro di sistema.                                                                              |
| [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Scarica la chiave del Registro di sistema specificata e le relative sottochiavi dal Registro di sistema.                                                                          |



 

Con il Registro di sistema è possibile usare le funzioni della shell seguenti:

-   [**AssocCreate**](/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate)
-   [**AssocQueryKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya)
-   [**AssocQueryString**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa)
-   [**AssocQueryStringByKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya)
-   [**SHCopyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya)
-   [**SHDeleteEmptyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya)
-   [**SHDeleteKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya)
-   [**SHDeleteValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletevaluea)
-   [**SHEnumKeyEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumkeyexa)
-   [**SHEnumValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumvaluea)
-   [**SHGetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea)
-   [**SHQueryInfoKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryinfokeya)
-   [**SHQueryValueEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryvalueexa)
-   [**SHRegCloseUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey)
-   [**SHRegCreateUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcreateuskeya)
-   [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya)
-   [**SHRegDeleteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea)
-   [**SHRegDuplicateHKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregduplicatehkey)
-   [**SHRegEnumUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumuskeya)
-   [**SHRegEnumUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumusvaluea)
-   [**SHRegGetBoolUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetboolusvaluea)
-   [**SHRegGetIntW**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetintw)
-   [**SHRegGetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetpatha)
-   [**SHRegGetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea)
-   [**SHRegOpenUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya)
-   [**SHRegQueryInfoUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryinfouskeya)
-   [**SHRegQueryUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea)
-   [**SHRegSetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetpatha)
-   [**SHRegSetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetusvaluea)
-   [**SHRegWriteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea)
-   [**SHSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea)

Di seguito sono riportate le funzioni del file di inizializzazione. Recuperano informazioni da e copiano le informazioni in un file di inizializzazione definito dal sistema o dall'applicazione. Queste funzioni vengono fornite solo per la compatibilità con le versioni a 16 bit Windows. Le nuove applicazioni devono usare il Registro di sistema.



| Funzione                                                               | Descrizione                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**GetPrivateProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Recupera un intero associato a una chiave nella sezione specificata di un file di inizializzazione.     |
| [**GetPrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Recupera tutte le chiavi e i valori per la sezione specificata di un file di inizializzazione.             |
| [**GetPrivateProfileSectionNames**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Recupera i nomi di tutte le sezioni in un file di inizializzazione.                                     |
| [**Getprivateprofilestring**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Recupera una stringa dalla sezione specificata in un file di inizializzazione.                           |
| [**GetPrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Recupera i dati associati a una chiave nella sezione specificata di un file di inizializzazione.       |
| [**GetProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Recupera un numero intero da una chiave nella sezione specificata del file Win.ini file.                      |
| [**GetProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Recupera tutte le chiavi e i valori per la sezione specificata del file Win.ini file.                   |
| [**GetProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Recupera la stringa associata a una chiave nella sezione specificata del file Win.ini file.           |
| [**WritePrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Sostituisce le chiavi e i valori per la sezione specificata in un file di inizializzazione.                  |
| [**WritePrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Copia una stringa nella sezione specificata di un file di inizializzazione.                              |
| [**WritePrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Copia i dati in una chiave nella sezione specificata di un file di inizializzazione.                         |
| [**WriteProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Sostituisce il contenuto della sezione specificata nel file Win.ini con chiavi e valori specificati. |
| [**WriteProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Copia una stringa nella sezione specificata del file Win.ini file.                                    |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Queste funzioni vengono fornite solo per la compatibilità con le versioni a 16 bit Windows:

-   [**RegCreateKey**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**RegEnumKey**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**RegOpenKey**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**RegQueryValue**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**RegSetValue**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
