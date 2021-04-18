---
description: Le operazioni con privilegi richiedono privilegi di sicurezza, ad esempio SeLoadDriverPrivilege (wbemPrivilegeLoadDriver nelle costanti API di scripting), un privilegio che deve essere abilitato per un account che sta caricando un driver di dispositivo.
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
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310353"
---
# <a name="executing-privileged-operations"></a>Esecuzione di operazioni con privilegi

Le operazioni con privilegi richiedono privilegi di sicurezza, ad esempio **SeLoadDriverPrivilege** (**WBEMPRIVILEGELOADDRIVER** nelle [costanti API di scripting](scripting-api-constants.md)), un privilegio che deve essere abilitato per un account che sta caricando un driver di dispositivo. Non è possibile aggiungere privilegi a un amministratore o a un utente tramite WMI. è possibile abilitare solo i privilegi già presenti nell'account. Per un elenco dei privilegi, vedere [**\_ costanti Privilege**](privilege-constants.md).

Per impostazione predefinita, un utente locale in un computer può leggere i dati statici dal [*repository WMI*](gloss-w.md), scrivere nelle istanze fornite dai provider ed eseguire i metodi del provider, a meno che il provider non imponga specifici requisiti di sicurezza. Solo gli amministratori possono [connettersi a un computer remoto](connecting-to-wmi-on-a-remote-computer.md), modificare i descrittori di sicurezza o modificare i dati del repository WMI statici, ad esempio una definizione di classe WMI. Tutti i privilegi sono abilitati per una connessione remota. Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).

Le costanti dei privilegi per C++ sono diverse da quelle utilizzate dai linguaggi di automazione, ad esempio Visual Basic. Gli script devono usare il valore della costante anziché il nome. Per altre informazioni, vedere [esecuzione di operazioni con privilegi con C++](executing-privileged-operations-using-c-.md) o [esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md).

Una causa comune degli errori di accesso negato quando si utilizza WMI è la mancanza di un privilegio abilitato per le operazioni, ad esempio il recupero di tutte le istanze di [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)). Se non si Abilita il privilegio di **sesecurity** , non è possibile accedere al file di registro di sicurezza.

Nell'esempio di codice VBScript riportato di seguito viene illustrato come impostare il privilegio di **sesicurezza** nella stringa del moniker. Quando viene usato nel moniker, il nome del privilegio tra parentesi Elimina il "se" iniziale. Per ulteriori informazioni, vedere [creazione di una stringa di moniker](constructing-a-moniker-string.md).


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

[**Costanti Privilege**](privilege-constants.md)
</dt> </dl>

 

 
