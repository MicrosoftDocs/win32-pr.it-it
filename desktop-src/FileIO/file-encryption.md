---
description: Il file system crittografato (EFS) fornisce la protezione crittografica di singoli file nei volumi file system NTFS usando un sistema a chiave pubblica.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Crittografia file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dbbfa82024bea13eab9e672b482ea18bc1051cd6e86b97d2a405351e3b078b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107571"
---
# <a name="file-encryption"></a>Crittografia file

Il file system crittografato, o EFS, offre un livello aggiuntivo di sicurezza per file e directory. Fornisce la protezione crittografica di singoli file in volumi file system NTFS usando un sistema a chiave pubblica.

In genere, il controllo di accesso agli oggetti file e directory forniti dal modello di sicurezza Windows è sufficiente per proteggere l'accesso non autorizzato a informazioni riservate. Tuttavia, se un portatile che contiene dati sensibili viene smarrito o rubato, la protezione di sicurezza di tali dati potrebbe essere compromessa. La crittografia dei file aumenta la sicurezza.

Per determinare se un file system supporta la crittografia dei file per file e directory, chiamare la [**funzione GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il flag di bit **FS FILE \_ \_ ENCRYPTION.** Si noti che non è possibile crittografare gli elementi seguenti:

-   File compressi
-   File di sistema
-   Directory di sistema
-   Directory radice
-   Transazioni

I file sparse possono essere crittografati.

TxF non supporta la maggior parte delle operazioni sui file EFS (Encrypted File System). Le uniche operazioni supportate da TxF sono le operazioni di lettura, ad [**esempio ReadEncryptedFileRaw.**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestione di file e directory crittografati](handling-encrypted-files-and-directories.md)<br/> | Un file contrassegnato come crittografato viene crittografato dal file system NTFS usando il driver di crittografia corrente.<br/>                                                          |
| [File crittografati e chiavi utente](encrypted-files-and-user-keys.md)<br/>                       | Elenca le funzioni da usare per creare una nuova chiave, aggiungere una chiave a un file crittografato, eseguire una query delle chiavi per un file crittografato e rimuovere le chiavi da un file crittografato.<br/> |
| [Backup e ripristino di file crittografati](backup-and-restore-of-encrypted-files.md)<br/>       | Le funzioni di crittografia non elaborata consentono il backup dei file crittografati.<br/>                                                                                                |



 

Per altre informazioni sulla crittografia, vedere [Aggiunta di utenti a un file crittografato.](adding-users-to-an-encrypted-file.md)

Per altre informazioni sulla crittografia, vedere [Crittografia.](/windows/desktop/SecCrypto/cryptography-portal)

 

