---
description: È possibile richiedere che le applicazioni e gli script client stabiliscano una connessione crittografata per l'autenticazione aggiungendo il qualificatore RequiresEncryption al file MOF (Managed Object Format). mof che crea lo spazio dei nomi.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Richiesta di una connessione crittografata a uno spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318535"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a>Richiesta di una connessione crittografata a uno spazio dei nomi

È possibile richiedere che le applicazioni e gli script client stabiliscano una connessione crittografata per l'autenticazione aggiungendo il qualificatore **RequiresEncryption** al file mof (Managed Object Format). mof che crea lo spazio dei nomi.


Una connessione crittografata a uno spazio dei nomi WMI specifica il livello di autenticazione **\_ \_ \_ \_ PKT \_** (o **su PktPrivacy** in uno script) RPC C per l'autenticazione. Il qualificatore **RequiresEncryption** fa in modo che WMI rifiuti le richieste di dati in ingresso a meno che non utilizzi in modo esplicito l'autenticazione crittografata. Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md) o [impostazione dell'autenticazione mediante C++](setting-authentication-using-c-.md).

È anche possibile modificare uno spazio dei nomi esistente aggiungendo questo attributo e quindi compilare nuovamente il file MOF. **RequiresEncryption** viene usato in [*MOF*](gloss-m.md) con l'istruzione del preprocessore [pragma namespace](pragma-namespace.md) .

La procedura seguente imposta lo spazio dei nomi per richiedere una connessione crittografata.

**Per impostare la crittografia necessaria**

1.  Creare un file di Managed Object Format (MOF) o modificare il file MOF esistente che definisce lo spazio dei nomi.

    Nell'esempio di codice seguente viene illustrato lo spazio dei nomi che verrà modificato è *root \\ MyNamespace* e il file è denominato *MyNamespace \_ Security. mof*. **RequiresEncryption** ha un tipo di dati booleano, quindi deve essere impostato su **true** o **false**.

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  Eseguire [**mofcomp.exe**](mofcomp.md) per compilare il file MOF.

    **c: \\ mofcomp MyNamespace \_ Security. mof**

    In C++ usare i metodi [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

WMI rifiuta un client che utilizza il livello di autenticazione predefinito perché DCOM negozia la sicurezza al livello richiesto dal processo SVCHOST in cui è in esecuzione il servizio WMI. Per ulteriori informazioni sugli host del servizio, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md). Per ulteriori informazioni su come impostare i livelli di autenticazione durante la connessione agli spazi dei nomi WMI, vedere [impostazione del livello di sicurezza del processo predefinito mediante c++](setting-the-default-process-security-level-using-c-.md), [impostazione dell'autenticazione mediante c++](setting-authentication-using-c-.md)o [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

Quando si restituiscono dati in una connessione di callback asincrona, WMI restituisce un messaggio di accesso negato al computer richiedente. WMI rende inoltre una voce di log nel registro eventi NT del computer con lo spazio dei nomi crittografato che informa che non è possibile stabilire una connessione protetta al client.

A partire da Windows Vista, il file WbemCore. log non esiste più. È possibile controllare il registro eventi NT per le voci che indicano le richieste di dati in ingresso rifiutate agli spazi dei nomi che richiedono la crittografia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[Protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



