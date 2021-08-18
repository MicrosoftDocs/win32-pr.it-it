---
description: Le operazioni con privilegi richiedono privilegi di sicurezza, ad esempio SeLoadDriverPrivilege (wbemPrivilegeLoadDriver nelle costanti dell'API di scripting), un privilegio che deve essere abilitato per un account che sta caricando un driver di dispositivo.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Esecuzione di operazioni con privilegi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce87a5783462be86d6e2e2b0565e93d811b972393319a34f84be2ab3d8e34c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050869"
---
# <a name="executing-privileged-operations"></a>Esecuzione di operazioni con privilegi

Le operazioni con privilegi richiedono privilegi di sicurezza, ad esempio **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** nelle costanti dell'API di scripting ), un privilegio che deve essere abilitato per un account che sta caricando un driver di dispositivo. [](scripting-api-constants.md) Non è possibile aggiungere privilegi a un amministratore o a un utente tramite WMI, ma solo privilegi già disponibili per l'account. Per un elenco dei privilegi, vedere [**Costanti \_ di privilegi.**](privilege-constants.md)

Per impostazione predefinita, un utente locale in un computer può leggere dati statici dal [*repository WMI,*](gloss-w.md)scrivere nelle istanze fornite dai provider ed eseguire metodi del provider, a meno che il provider non applicherà requisiti di sicurezza specifici. Solo gli amministratori [possono connettersi a un computer](connecting-to-wmi-on-a-remote-computer.md)remoto, modificare i descrittori di sicurezza o modificare i dati statici del repository WMI, ad esempio una definizione di classe WMI. Tutti i privilegi sono abilitati per una connessione remota. Per altre informazioni, vedere [Protezione di una connessione WMI remota.](securing-a-remote-wmi-connection.md)

Le costanti di privilegio per C++ differiscono da quelle usate dai linguaggi di automazione, ad esempio Visual Basic. Gli script devono usare il valore della costante anziché il nome. Per altre informazioni, vedere [Esecuzione di operazioni con privilegi tramite C++](executing-privileged-operations-using-c-.md) o Esecuzione di operazioni con privilegi tramite [VBScript.](executing-privileged-operations-using-vbscript.md)

Una causa comune degli errori di accesso negato quando si usa WMI è la mancanza di un privilegio abilitato per le operazioni, ad esempio il recupero di tutte le istanze di [**Win32 \_ NTEventlogFile.**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) Senza abilitare il **privilegio SeSecurity,** non è possibile accedere al file di log di sicurezza.

Nell'esempio di codice VBScript seguente viene illustrato come impostare il **privilegio SeSecurity** nella stringa del moniker. Se usato nel moniker, il nome del privilegio tra parentesi elimina la "Se" iniziale. Per altre informazioni, vedere [Costruzione di una stringa di moniker.](constructing-a-moniker-string.md)


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti privilege**](privilege-constants.md)
</dt> </dl>

 

 
