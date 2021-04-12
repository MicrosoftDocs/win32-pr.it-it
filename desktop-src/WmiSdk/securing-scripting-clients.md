---
description: Per gli script e le applicazioni Visual Basic è necessario impostare la sicurezza DCOM, in particolare per l'accesso remoto, e potrebbe inoltre essere necessario abilitare i privilegi.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Protezione dei client di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226822"
---
# <a name="securing-scripting-clients"></a>Protezione dei client di scripting

Per gli script e le applicazioni Visual Basic è necessario impostare la sicurezza DCOM, in particolare per l'accesso remoto, e potrebbe inoltre essere necessario abilitare i privilegi.

## <a name="default-access-permissions"></a>Autorizzazioni di accesso predefinite

L'accesso WMI è diverso tra computer locali e remoti. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

Di seguito sono riportate le autorizzazioni di accesso predefinite per account:

-   Tutti, LocalService, NetworkService

    Autorizzazione per la lettura o la scrittura di dati e per l'esecuzione di [*metodi del provider*](gloss-p.md) nel computer locale. Questi account non possono creare nuove classi o installare nuovi provider.

-   Account amministratore

    Controllo completo sul computer locale. Quando ci si connette a un computer remoto, l'account deve essere anche un amministratore locale nel computer remoto.

## <a name="securing-a-scripting-client"></a>Protezione di un client di scripting

Gli script WMI e le applicazioni Visual Basic devono impostare i livelli di sicurezza DCOM in modo appropriato per i sistemi operativi di destinazione. Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

Quando ci si connette a un computer remoto, potrebbe essere necessario modificare il servizio (NTLM o Kerberos) che gestisce l'autenticazione. Per ulteriori informazioni, vedere [impostazione del servizio di autenticazione tramite VBScript](setting-the-authentication-service-using-vbscript.md).

L'accesso ad alcune classi o dati WMI potrebbe richiedere un privilegio non abilitato. Ad esempio, è necessario includere il privilegio di sicurezza quando ci si connette alla classe [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) . Per ulteriori informazioni, vedere [esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md).

Se si accede a WMI da una pagina di Active Server (ASP), è necessaria una configurazione di IIS. Per ulteriori informazioni, vedere [la pagina relativa alla configurazione di IIS 5,0 e versioni successive per lo scripting ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).

È possibile che si stia tentando di connettersi a uno spazio dei nomi che richiede una connessione crittografata, ovvero una connessione che richiede un livello di autenticazione su PktPrivacy. Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
