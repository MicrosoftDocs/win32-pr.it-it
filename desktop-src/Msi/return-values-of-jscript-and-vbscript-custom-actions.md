---
description: Le azioni personalizzate scritte in JScript o Visual Basic, Scripting Edition (VBScript) può chiamare una funzione facoltativa. Queste funzioni devono restituire uno dei valori illustrati nella tabella seguente.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valori restituiti delle JScript personalizzate e VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50a2b225c59b0e4d1787f2eaceeb094d6fb2abe7f9d9600822b6295ef2dd273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626091"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Valori restituiti delle JScript personalizzate e VBScript

Le azioni personalizzate scritte in JScript o Visual Basic, Scripting Edition (VBScript) può chiamare una funzione facoltativa. Queste funzioni devono restituire uno dei valori illustrati nella tabella seguente.



| Valore restituito              | Valore        | Descrizione                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | Azione non eseguita.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | Azione completata.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Interruzione prematura da parte dell'utente.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Errore irreversibile. Restituito se si verifica un errore durante l'analisi o l'esecuzione del JScript o VBScript. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Sequenza sospesa da riprendere in un secondo momento.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Ignorare le azioni rimanenti. Non è un errore.                                                                      |



 

Si noti Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Ad esempio, se il valore restituito dell'azione viene visualizzato come 1 (uno) nel file di log, significa che l'azione ha restituito msiDoActionStatusSuccess. Per altre informazioni su questa traduzione, vedere [Registrazione dei valori restituiti delle azioni.](logging-of-action-return-values.md)

Per restituire un valore diverso da success da un'azione personalizzata dello script, è necessario usare una destinazione di funzione per l'azione personalizzata. La funzione di destinazione viene specificata nella colonna Target della [tabella CustomAction](customaction-table.md).

L'esempio di script seguente illustra come restituire l'esito positivo o negativo da un'azione personalizzata VBScript.


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



Se questo vbScript è stato incorporato nella tabella [binaria](binary-table.md) del pacchetto di installazione come MyCA.vbs, la voce [Tabella CustomAction](customaction-table.md) per lo script sarà la seguente:



| Azione         | Tipo | Source (Sorgente)   | Destinazione       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



