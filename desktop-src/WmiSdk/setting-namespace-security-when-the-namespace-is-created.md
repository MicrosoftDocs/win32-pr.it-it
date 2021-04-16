---
title: Impostazione della sicurezza per la creazione dello spazio dei nomi
description: Il file di Managed Object Format (MOF) che crea uno spazio dei nomi può anche definire i descrittori di sicurezza per lo spazio dei nomi includendo il qualificatore NamespaceSecuritySDDL con il descrittore di sicurezza in formato SDDL (Security Descriptor Definition Language).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530138"
---
# <a name="setting-security-on-namespace-creation"></a>Impostazione della sicurezza per la creazione dello spazio dei nomi

Il file di Managed Object Format (MOF) che crea uno spazio dei nomi può anche definire i [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly) per lo spazio dei nomi includendo il qualificatore **NamespaceSecuritySDDL** con il descrittore di sicurezza in formato [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .

È possibile usare **NamespaceSecuritySDDL** per proteggere qualsiasi spazio dei nomi. È inoltre possibile utilizzare questo qualificatore in un semplice file MOF per modificare il descrittore di sicurezza in uno spazio dei nomi esistente. La stringa SDDL viene elaborata da WMI per stabilire la sicurezza dello spazio dei nomi, ma non viene archiviata come stringa. Se non viene specificato alcun descrittore di sicurezza, viene utilizzata la sicurezza predefinita. Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).

La procedura seguente consente di impostare il descrittore di sicurezza per lo spazio dei nomi MyNamespace *radice \\* . La stringa SDDL imposta il proprietario e il gruppo sugli utenti autenticati e specifica un [*elenco di controllo di accesso discrezionale (DACL)*](/windows/desktop/SecGloss/d-gly) ereditato dagli spazi dei nomi figlio. L'elenco DACL consente all'utente di leggere i dati, eseguire metodi, scrivere dati nelle classi del provider e utilizzare accesso remoto **: \_ Abilita WBEM**, **\_ Metodo WBEM \_ Execute**, **\_ \_ provider di scrittura WBEM**, **\_ \_ accesso remoto WBEM**. Per ulteriori informazioni, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).

**Per impostare un DACL dello spazio dei nomi**

1.  Creare un file di Managed Object Format (MOF) o modificare il file MOF esistente che definisce lo spazio dei nomi per aggiungere il qualificatore **NamespaceSecuritySDDL** con la stringa SDDL.

    L'esempio di codice seguente mostra che lo spazio dei nomi da modificare è radice \\ MyNamespace e il file è denominato MyNamespace \_ Security. mof.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Tenere presente che la stringa SDDL distingue tra maiuscole e minuscole: le lettere devono essere maiuscole.

    Nell'esempio di codice riportato di seguito vengono illustrate le lettere "o" e "g" nella stringa SDDL come minuscole e la Mofcomp.exe restituirà un errore.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  Eseguire [**Mofcomp.exe**](mofcomp.md) per compilare il file MOF.

    **c: \\ mofcomp MyNamespace \_ Security. mof**

    In C++ usare i metodi [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

4.  Se il tentativo di impostare l'elenco DACL dello spazio dei nomi ha esito negativo, considerare i messaggi di errore seguenti:

    

    | Errore                           | Descrizione                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **\_parametro WBEM E \_ non valido \_** | Non esiste alcun DACL ereditato. In alternativa, il chiamante ha violato il DACL o la SD nello spazio dei nomi padre. |
    | **accesso a WBEM \_ E \_ \_ negato**     | Il chiamante non dispone dell'autorizzazione per aggiornare SDDL in MOF.                                               |

    

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Costanti dei diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md)
</dt> <dt>

[**Costanti del flag ACE dello spazio dei nomi**](namespace-ace-flag-constants.md)
</dt> <dt>

[Modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
