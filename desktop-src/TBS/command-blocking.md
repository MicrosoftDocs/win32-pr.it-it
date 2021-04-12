---
title: Blocco comandi
description: Per mantenere l'integrità delle operazioni, alcuni comandi TPM non possono essere eseguiti dal software sulla piattaforma.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104398807"
---
# <a name="command-blocking"></a>Blocco comandi

Per mantenere l'integrità delle operazioni, alcuni comandi TPM non possono essere eseguiti dal software sulla piattaforma. Alcuni comandi, ad esempio, vengono eseguiti solo dal software di sistema. Quando TBS blocca un comando, viene restituito un errore nel modo appropriato. Per impostazione predefinita, TBS blocca i comandi che potrebbero influisca sulla privacy, sulla sicurezza e sulla stabilità del sistema. In TBS si presuppone inoltre che altre parti dello stack software possano limitare l'accesso a determinati comandi a entità autorizzate.

Per i comandi TPM versione 1,2 sono disponibili tre elenchi di comandi bloccati: un elenco controllato da criteri di gruppo, un elenco controllato dagli amministratori locali e un elenco predefinito. Un comando TPM viene bloccato se si trova in uno qualsiasi degli elenchi. Esistono tuttavia flag di criteri di gruppo che consentono a TBS di ignorare l'elenco locale e l'elenco predefinito. I flag di criteri di gruppo possono essere modificati direttamente o a cui si accede tramite la Editor oggetti Criteri di gruppo.

> [!Note]  
> L'elenco dei comandi bloccati localmente non viene mantenuto dopo un aggiornamento al sistema operativo. I comandi bloccati nell'elenco Criteri di gruppo vengono conservati.

 

Per i comandi TPM versione 2,0, la logica per il blocco viene invertita; Usa un elenco di comandi consentiti. Questa logica bloccherà automaticamente i comandi che non erano noti quando l'elenco è stato creato per la prima volta. Quando i comandi vengono aggiunti alla specifica TPM dopo che è stata spedita una versione di Windows, questi nuovi comandi vengono bloccati automaticamente. Solo un aggiornamento del registro di sistema aggiungerà questi nuovi comandi all'elenco dei comandi consentiti.

A partire da Windows 10 1809 (Windows Server 2019), i comandi TPM 2,0 consentiti non possono più essere modificati tramite le impostazioni del registro di sistema. Per queste versioni di Windows 10, i comandi TPM 2,0 consentiti sono corretti nel driver TPM. È ancora possibile bloccare e sbloccare i comandi TPM 1,2 tramite modifiche al registro di sistema. 

## <a name="direct-registry-access"></a>Accesso diretto al registro di sistema

I flag di criteri di gruppo si trovano nella chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.

Per determinare gli elenchi da usare per bloccare i comandi TPM, sono disponibili due valori **DWORD** usati come flag booleani:

-   "IgnoreDefaultList"

    Se impostato (il valore esiste e è diverso da zero), TBS ignora l'elenco dei comandi bloccati predefiniti.

-   "IgnoreLocalList"

    Se impostato (il valore esiste e è diverso da zero), TBS ignora l'elenco dei comandi bloccati locali.

## <a name="group-policy-object-editor"></a>Editor oggetti Criteri di gruppo

**Per accedere all'Editor oggetti di Criteri di gruppo**

1.  Fare clic su **Start** (Avvia).
2.  Fare clic su **Esegui**.
3.  Nella casella **Apri** digitare **gpedit.msc**. Fare clic su **OK**. Verrà aperto l'Editor oggetti Criteri di gruppo.
4.  Espandere **Configurazione computer**.
5.  Espandere **modelli amministrativi**.
6.  Espandere **sistema**.
7.  Espandere **Trusted Platform Module Services**.

Gli elenchi di comandi TPM 1.2 bloccati specifici possono essere modificati direttamente nei percorsi seguenti.

-   Elenco criteri di gruppo:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   Elenco locale:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   Elenco predefinito:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

In ognuna di queste chiavi del registro di sistema è presente un elenco di valori del registro di sistema di \_ tipo reg SZ. Ogni valore rappresenta un comando TPM bloccato. Ogni chiave del registro di sistema ha un campo "nome valore" e un campo "dati valore". Sia i campi ("nome valore" che "dati valore") devono corrispondere esattamente al valore decimale dell'ordinale del comando TPM da bloccare.

L'elenco di specifici comandi TPM 2,0 consentiti può essere modificato direttamente nel percorso seguente. Nella chiave del registro di sistema è presente un elenco dei valori del registro di sistema REG \_ DWORD Type. Ogni valore rappresenta un comando TPM 2,0 consentito. Ogni valore del registro di sistema ha un **nome** e un campo **valore** . Il **nome** corrisponde al numero ordinale del comando TPM 2,0 esadecimale che deve essere consentito. Se **il comando** è consentito, il valore è 1. Se un ordinale del comando non è presente o ha un valore pari a 0, il comando verrà bloccato.

-   Elenco predefinito:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

Per Windows 8, Windows Server 2012 e versioni successive, le chiavi del registro di sistema **BlockedCommands** e **AllowedW8Commands** stabiliscono rispettivamente i comandi TPM bloccati o consentiti per gli account amministratore. Gli account utente includono rispettivamente un elenco di comandi TPM bloccati o consentiti nelle chiavi del registro di sistema **BlockedUserCommands** e **AllowedW8UserCommands** . In Windows 10 versione 1607 sono state introdotte nuove chiavi del registro di sistema per le applicazioni AppContainer: **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands**.

 

 




