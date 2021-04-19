---
description: Il file system crittografato (EFS) fornisce la protezione crittografica dei singoli file nei volumi file system NTFS usando un sistema a chiave pubblica.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Crittografia file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317795"
---
# <a name="file-encryption"></a>Crittografia file

Il file system crittografato, o EFS, fornisce un livello aggiuntivo di sicurezza per i file e le directory. Fornisce la protezione crittografica dei singoli file in NTFS file system volumi utilizzando un sistema a chiave pubblica.

In genere, il controllo di accesso agli oggetti file e directory fornito dal modello di sicurezza di Windows è sufficiente per proteggere l'accesso non autorizzato alle informazioni riservate. Tuttavia, se un portatile che contiene dati sensibili viene smarrito o rubato, la protezione dei dati potrebbe essere compromessa. La crittografia dei file aumenta la sicurezza.

Per determinare se un file system supporta la crittografia dei file per i file e le directory, chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il flag di bit di **\_ \_ crittografia del file FS** . Si noti che non è possibile crittografare gli elementi seguenti:

-   File compressi
-   File di sistema
-   Directory di sistema
-   Directory radice
-   Transazioni

I file sparse possono essere crittografati.

TxF non supporta la maggior parte delle operazioni sui file EFS (Encrypted File System). Le uniche operazioni supportate da TxF sono operazioni di lettura, ad esempio [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestione di file e directory crittografati](handling-encrypted-files-and-directories.md)<br/> | Un file contrassegnato come crittografato viene crittografato dall'file system NTFS usando il driver di crittografia corrente.<br/>                                                          |
| [Chiavi utente e file crittografati](encrypted-files-and-user-keys.md)<br/>                       | Elenca le funzioni da usare per creare una nuova chiave, aggiungere una chiave a un file crittografato, eseguire una query sulle chiavi per un file crittografato e rimuovere le chiavi da un file crittografato.<br/> |
| [Backup e ripristino di file crittografati](backup-and-restore-of-encrypted-files.md)<br/>       | Le funzioni di crittografia RAW consentono di eseguire il backup dei file crittografati.<br/>                                                                                                |



 

Per ulteriori informazioni sulla crittografia, vedere [aggiunta di utenti a un file crittografato](adding-users-to-an-encrypted-file.md).

Per ulteriori informazioni sulla crittografia, vedere [crittografia](/windows/desktop/SecCrypto/cryptography-portal).

 

