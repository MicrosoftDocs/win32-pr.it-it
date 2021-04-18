---
title: RunAs
description: Configura una classe per l'esecuzione con un account utente specifico quando viene attivato da un client remoto senza essere scritto come applicazione di servizio.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valore COM del registro di sistema RunAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300500"
---
# <a name="runas"></a>RunAs

Configura una classe per l'esecuzione con un account utente specifico quando viene attivato da un client remoto senza essere scritto come applicazione di servizio.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a>Commenti

Il valore specifica il nome utente e deve essere del formato *username*, *Domain ***\\*** username* o della stringa "Interactive User". È inoltre possibile specificare le stringhe "NT Authority \\ LocalService" (per il servizio locale) e "NT Authority \\ NetworkService" (per servizio di rete). È inoltre possibile specificare la stringa "NT Authority \\ System" quando {*AppID \_ GUID*} fa riferimento a un server com già avviato o con una voce nella tabella della classe. Tuttavia, non è possibile utilizzare "NT Authority \\ System" con un server com non ancora avviato. La password predefinita per "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System" è "" (stringa vuota).

> [!Note]  
> A partire da Windows Vista, non è più necessaria una password vuota per configurare le \\ Impostazioni RunAs "NT Authority LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System". 

 

Le classi configurate per l'esecuzione come utente specifico potrebbero non essere registrate con altre identità, quindi le chiamate a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con questo CLSID hanno esito negativo a meno che il processo non sia stato avviato da com per conto di una richiesta di attivazione effettiva.

Il nome utente viene tratto dal valore **RunAs** sotto la chiave **AppID** della classe. Se il nome utente è "utente interattivo", il server viene eseguito con l'identità dell'utente attualmente connesso ed è connesso al desktop interattivo.

In caso contrario, la password viene recuperata da una parte del registro di sistema disponibile solo per gli amministratori del computer e del sistema. Il nome utente e la password vengono quindi utilizzati per creare una sessione di accesso in cui viene eseguito il server. Quando viene avviato in questo modo, l'utente viene eseguito con il proprio desktop e la propria stazione di Windows e non condivide gli handle di finestra, gli Appunti o altri elementi dell'interfaccia utente con l'utente interattivo o con un altro utente in esecuzione in altri account utente.

Per stabilire una password per una classe **RunAs** , è necessario utilizzare lo strumento di amministrazione DCOMCNFG installato nella directory di sistema.

Per le identità **RunAs** utilizzate dai server DCOM, l'account utente specificato nel valore deve disporre dei diritti di accesso come processo batch. Questo diritto può essere aggiunto utilizzando lo strumento di amministrazione Criteri di sicurezza locali. Passare a **criteri locali** e aprire **assegnazione diritti utente**. Selezionare **Accedi come processo batch** e aggiungere l'account utente.

Il valore **RunAs** non viene utilizzato per i server configurati per l'esecuzione come servizi. I servizi COM che devono essere eseguiti con un'identità diversa da LocalSystem devono impostare il nome utente e la password appropriati utilizzando l'applet del pannello di controllo dei servizi o le funzioni del controller di servizio. Per ulteriori informazioni su queste funzioni, vedere [Servizi](/windows/desktop/Services/services).

> [!Note]  
> A partire da Microsoft Windows Server 2003, la classe AppID viene letta in modo esplicito dalle **\_ \_ classi software del computer locale HKEY \\ \\ \\ AppID**, che, a differenza della maggior parte delle chiavi del registro di sistema, non è interscambiabile con le **\_ classi HKEY \_ radice \\ AppID**.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> </dl>

 

 