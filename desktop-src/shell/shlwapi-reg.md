---
description: In questa sezione vengono descritte le funzioni di gestione del registro di sistema di Windows Shell. Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.
title: Funzioni di gestione del registro di sistema shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8a3e4f65904fa97635b3ef4dc3abd9f01344f6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995069"
---
# <a name="shell-registry-handling-functions"></a>Funzioni di gestione del registro di sistema shell

In questa sezione vengono descritte le funzioni di gestione del registro di sistema di Windows Shell. Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                             | Descrizione                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Restituisce un puntatore a un oggetto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                                                         |
| [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Recupera il tipo percepito di un file in base alla relativa estensione.<br/>                                                                                                                |
| [**AssocIsDangerous**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Determina se un tipo di file è considerato un potenziale rischio per la sicurezza.<br/>                                                                                                  |
| [**AssocQueryKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Cerca e recupera una chiave correlata a un'associazione di file o protocolli dal registro di sistema.<br/>                                                                            |
| [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Cerca e recupera una stringa relativa all'associazione di file o protocolli dal registro di sistema.<br/>                                                                              |
| [**AssocQueryStringByKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Cerca e recupera una stringa correlata all'associazione di file dal registro di sistema a partire da una chiave specificata.<br/>                                                            |
| [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Copia in modo ricorsivo le sottochiavi e i valori della sottochiave di origine nella chiave di destinazione. [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) non copia gli attributi di sicurezza delle chiavi.<br/> |
| [**SHDeleteEmptyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Elimina una chiave vuota.<br/>                                                                                                                                                    |
| [**SHDeleteKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Elimina una sottochiave e tutti i relativi discendenti. Questa funzione rimuove la chiave e tutti i valori della chiave dal registro di sistema.<br/>                                                      |
| [**SHDeleteValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Elimina un valore denominato dalla chiave del registro di sistema specificata.<br/>                                                                                                                   |
| [**SHEnumKeyEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Enumera le sottochiavi della chiave del registro di sistema aperta specificata.<br/>                                                                                                               |
| [**SHEnumValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Enumera i valori della chiave del registro di sistema aperta specificata.<br/>                                                                                                                |
| [**SHGetAssocKeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Recupera una matrice di sottochiavi di classe associate a un oggetto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                          |
| [**SHGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Recupera un valore del registro di sistema.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Apre un valore del registro di sistema e fornisce un flusso che può essere utilizzato per leggere o scrivere nel valore. Questa funzione sostituisce [**SHOpenRegStream**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama).<br/>   |
| [**SHQueryInfoKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Recupera le informazioni su una chiave del registro di sistema specificata.<br/>                                                                                                                    |
| [**SHQueryValueEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Apre una chiave del registro di sistema ed esegue una query per un valore specifico.<br/>                                                                                                                |
| [**SHRegCloseUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Chiude un handle a una sottochiave del registro di sistema specifica dell'utente in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                             |
| [**SHRegCreateUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Crea o apre una sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                             |
| [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Elimina una sottochiave del registro di sistema vuota in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                               |
| [**SHRegDeleteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Elimina un valore della sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                                |
| [**SHRegDuplicateHKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Duplica un handle HKEY della chiave del registro di sistema.<br/>                                                                                                                                 |
| [**SHRegEnumUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Enumera le sottochiavi di una sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                    |
| [**SHRegEnumUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Enumera i valori della sottochiave del registro di sistema specificata in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                         |
| [**SHRegGetBoolUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Recupera un valore booleano da una sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                               |
| [**SHRegGetIntW**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Legge un valore stringa numerico dal registro di sistema e lo converte in un numero intero.<br/>                                                                                            |
| [**SHRegGetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Recupera un percorso di file dal registro di sistema, espandendo le variabili di ambiente in base alle esigenze.<br/>                                                                                      |
| [**SHRegGetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Recupera un valore da una sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                       |
| [**SHRegOpenUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Apre una sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                                        |
| [**SHRegQueryInfoUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Recupera le informazioni su una sottochiave del registro di sistema specificata in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                        |
| [**SHRegQueryUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Recupera il tipo e i dati per un nome specificato associato a una sottochiave del registro di sistema aperta in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>       |
| [**SHRegSetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Accetta un percorso di file, sostituisce i nomi delle cartelle con le stringhe di ambiente e inserisce la stringa risultante nel registro di sistema.<br/>                                                      |
| [**SHRegSetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Imposta un valore della sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                                   |
| [**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Imposta un valore del registro di sistema.<br/> Usare [**RegSetValue**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) al suo posto.<br/>                                                                                  |
| [**SHRegWriteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Scrive un valore in una sottochiave del registro di sistema in un sottoalbero specifico dell'utente (HKEY \_ Current \_ User o HKEY \_ Local \_ computer).<br/>                                                            |
| [**SHSetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Imposta il valore di una chiave del registro di sistema.<br/>                                                                                                                                        |



 

 

 
