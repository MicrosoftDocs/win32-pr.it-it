---
description: Per migliorare la sicurezza del processo host del provider condiviso Windows Management Instrumentation (WMI) (wmiprvse.exe), sono state apportate modifiche alle piattaforme Windows che protegge il processo host del provider con un ID di sicurezza del servizio (SID).
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Chiavi e valori del Registro di sistema per il controllo della sicurezza del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916a5910a6ad21e9f9dfdcfc0992de10ae30da82
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884353"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>Chiavi e valori del Registro di sistema per il controllo della sicurezza del provider

Per migliorare la sicurezza del processo host del provider condiviso Windows Management Instrumentation (WMI) (wmiprvse.exe), sono state apportate modifiche alle piattaforme Windows che protegge il processo host del provider con un ID di sicurezza [*del servizio (SID).*](gloss-s.md) Queste modifiche introducono le modalità di esecuzione seguenti per l'host condiviso WMI: sicuro e compatibile.

In questo argomento vengono trattate le sezioni seguenti:

-   [Modalità sicure e compatibili](#secure-and-compatible-modes)
-   [Chiavi e valori del Registro di sistema](#registry-keys-and-values)
-   [Configurazione di un provider per l'esecuzione in modalità protetta o compatibile](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>Modalità sicure e compatibili

A partire Windows 7 sono state aggiunte le due modalità di esecuzione seguenti per il processo host condiviso WMI:

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Modalità sicura
</dt> <dd>

Le risorse del processo host del provider WMI sono protette con un [*SID del servizio*](gloss-s.md). Solo il *SID del servizio* dispone delle autorizzazioni per queste risorse.

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Modalità compatibile
</dt> <dd>

Il processo host del provider condiviso WMI non è protetto con un [*SID del servizio*](gloss-s.md). Il processo host del provider consente l'accesso agli account NetworkService o LocalService a seconda del modello di hosting. Per altre informazioni sui modelli di hosting, vedere [Hosting e sicurezza del provider.](provider-hosting-and-security.md)

</dd> </dl>

**Windows Vista e Windows Server 2008:** Per accedere alle chiavi e ai valori del Registro di sistema per il controllo delle modalità protette e compatibili per il processo host del provider, è necessario installare l'aggiornamento della sicurezza nella [Knowledge Base 959454](https://support.microsoft.com/kb/959454). Per altre informazioni, vedere il [Bollettino Microsoft sulla sicurezza MS09-012.](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx)

## <a name="registry-keys-and-values"></a>Chiavi e valori del Registro di sistema

Le impostazioni della modalità protetta e compatibile vengono specificate tramite chiavi del Registro di sistema. Le chiavi del Registro di sistema per WMI si trovano nel Registro di sistema in **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

Le chiavi del Registro di sistema **e il valore DWORD** descritti nell'elenco seguente sono stati aggiunti per controllare il comportamento dei provider WMI.

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**
</dt> <dd>

Questa chiave controlla il comportamento dei singoli provider. Tutti i provider elencati in questa chiave vengono sempre eseguiti in modalità sicura. Tutti i provider della posta in arrivo forniti con Windows sono elencati in questa chiave e vengono eseguiti in modalità sicura per impostazione predefinita.

Questa chiave ha la precedenza sui provider elencati nella **chiave CompatibleHostProviders.**

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**
</dt> <dd>

Questa chiave controlla il comportamento dei singoli provider. Tutti i provider elencati in questa chiave vengono sempre eseguiti in modalità compatibile. Questa chiave è vuota per impostazione predefinita.

Se un provider è elencato sia nella chiave **SecuredHostProviders** che nella chiave **CompatibleHostProviders,** il provider viene eseguito in modalità sicura.

> [!Note]  
> La **chiave CompatibleHostProviders** garantisce la compatibilità delle applicazioni di terze parti se la chiave **DefaultSecuredHost** è impostata su 1 e il provider non funziona in modalità sicura.

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

Valore **DWORD** globale del Registro di sistema che determina se tutti i provider, che non sono elencati nelle chiavi **SecuredHostProviders** o **CompatibleHostProviders,** vengono eseguiti in modalità protetta o compatibile. Questo **valore DWORD** consente all'amministratore di decidere in quale modalità deve essere eseguito un provider di terze parti. Per impostazione predefinita, questo valore è impostato su zero e tutti i provider di terze parti vengono eseguiti in modalità compatibile. Gli amministratori possono rendere il computer più sicuro per impostazione predefinita impostando il **valore DefaultSecuredHost** su 1.

> [!Note]  
> Il **valore DefaultSecuredHost** non influisce sulle altre chiavi del Registro di sistema. I provider elencati nella chiave **SecuredHostProviders** rimangono in modalità sicura e quelli elencati nella chiave **CompatibleHostProviders** rimangono in modalità compatibile.

 

Sono possibili le impostazioni seguenti:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Specifica che i provider vengono eseguiti in modalità compatibile.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Specifica che i provider vengono eseguiti in modalità protetta.

</dd> </dl> </dd> </dl>

Nell'elenco seguente sono elencate le possibili impostazioni del Registro di sistema e le modalità di esecuzione associate per un provider.



| Elencato in SecuredHostProviders | Elencato in CompatibleHostProviders | Impostazione DefaultSecuredHost | Mode       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| No                                | No                                   | 0                          | Compatibile |
| No                                | Sì                                  | 0                          | Compatibile |
| Sì                               | No                                   | 0                          | Sicuro     |
| Sì                               | Sì                                  | 0                          | Sicuro     |
| No                                | No                                   | 1                          | Sicuro     |
| No                                | Sì                                  | 1                          | Compatibile |
| Sì                               | No                                   | 1                          | Sicuro     |
| Sì                               | Sì                                  | 1                          | Sicuro     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>Configurazione di un provider per l'esecuzione in modalità protetta o compatibile

Le chiavi del Registro di sistema possono essere modificate usando la console Console Gestione Criteri di gruppo (GPMC). Per altre informazioni, vedere [Console Gestione Criteri di gruppo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Le procedure seguenti illustrano come gestire le impostazioni della modalità protetta e compatibile usando le preferenze di Criteri di gruppo. Per altre informazioni sulle preferenze di Criteri di gruppo, vedere panoramica [Criteri di gruppo preferenze.](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11))

**Per aggiungere un provider alla modalità protetta o compatibile utilizzando Criteri di gruppo**

1.  Aprire Console Gestione Criteri di gruppo (GPMC).
2.  Creare un oggetto Criteri di gruppo (GPO).
3.  Modificare l'oggetto Criteri di gruppo.
4.  Passare a Preferenze/Windows Impostazioni/Registro di sistema.
5.  Fare clic con il pulsante destro del mouse e **scegliere Nuovo... Registro di sistema**. Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del Registro di sistema.
6.  Selezionare il **comando** Crea.
7.  Selezionare il percorso della chiave del Registro di sistema seguente:

    **Modalità sicura: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modalità compatibile: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  Nel campo **nome** immettere il nome del provider da aggiungere a questa chiave. Il nome del provider deve essere nel formato seguente: &lt; namespace &gt; :<\_ \_ RELPATH>. Ad esempio, \\ cimv2 radice: \_ \_ win32provider.name="MyProvider".
9.  Nel campo **dati** immettere 0.
10. Fare clic su OK.

**Per rimuovere un provider dalla modalità protetta o compatibile tramite Criteri di gruppo**

1.  Aprire Console Gestione Criteri di gruppo (GPMC).
2.  Creare un oggetto Criteri di gruppo.
3.  Modificare l'oggetto Criteri di gruppo.
4.  Passare a Preferenze/Windows Impostazioni/Registro di sistema.
5.  Fare clic con il pulsante destro del mouse e **scegliere Nuovo... Registro di sistema**. Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del Registro di sistema.
6.  Selezionare il **comando** Rimuovi.
7.  Selezionare il percorso della chiave del Registro di sistema seguente:

    **Modalità sicura: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modalità compatibile: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  Nel campo **nome** immettere il nome del provider da rimuovere da questa chiave.
9.  Nel campo **dati** immettere 0.
10. Fare clic su OK.

La procedura seguente fornisce informazioni dettagliate su come modificare il comportamento dei provider non elencati nelle chiavi **SecuredHostProviders** o **CompatibleHostProviders.**

**Per modificare il valore predefinito della chiave DefaultSecuredHost usando Criteri di gruppo**

1.  Aprire Console Gestione Criteri di gruppo (GPMC).
2.  Creare un oggetto Criteri di gruppo.
3.  Modificare l'oggetto Criteri di gruppo.
4.  Passare a Preferenze/Windows Impostazioni/Registro di sistema.
5.  Fare clic con il pulsante destro del mouse e **scegliere Nuovo... Registro di sistema**. Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del Registro di sistema.
6.  Selezionare il **comando** Aggiorna.
7.  Selezionare il percorso della chiave del Registro di sistema **seguente: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.
8.  Nel campo **nome** immettere **DefaultSecuredHost**.
9.  Nel campo **dati** immettere 0 per la modalità compatibile o 1 per la modalità protetta.
10. Fare clic su OK.

 

 
