---
description: Azioni personalizzate scritte in JScript o Visual Basic, Scripting Edition (VBScript) può chiamare una funzione facoltativa. Queste funzioni devono restituire uno dei valori mostrati nella tabella seguente.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valori restituiti di azioni personalizzate JScript e VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309463"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Valori restituiti di azioni personalizzate JScript e VBScript

Azioni personalizzate scritte in JScript o Visual Basic, Scripting Edition (VBScript) può chiamare una funzione facoltativa. Queste funzioni devono restituire uno dei valori mostrati nella tabella seguente.



| Valore restituito              | Valore        | Descrizione                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | L'azione non è stata eseguita.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | L'azione è stata completata correttamente.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Terminazione prematura dall'utente.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Errore irreversibile. Restituito se si verifica un errore durante l'analisi o l'esecuzione di JScript o VBScript. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Sequenza sospesa da riprendere in un secondo momento.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Ignora le azioni rimanenti. Non è un errore.                                                                      |



 

Si noti che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 (uno) nel file di log, significa che l'azione ha restituito msiDoActionStatusSuccess. Per ulteriori informazioni su questa traduzione, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).

Per restituire un valore diverso da esito positivo da un'azione personalizzata script, è necessario utilizzare una destinazione di funzione per l'azione personalizzata. La funzione di destinazione viene specificata nella colonna di destinazione della [tabella CustomAction](customaction-table.md).

Nell'esempio di script seguente viene illustrato come restituire l'esito positivo o negativo di un'azione personalizzata VBScript.


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



Se questo VBScript era incorporato nella [tabella binaria](binary-table.md) del pacchetto di installazione come MyCA.vbs, la voce della [tabella CustomAction](customaction-table.md) per lo script sarà la seguente:



| Azione         | Tipo | Source (Sorgente)   | Destinazione       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



