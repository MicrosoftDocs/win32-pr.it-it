---
title: Impostazione della sicurezza durante la creazione dello spazio dei nomi
description: Il file Managed Object Format (MOF) che crea uno spazio dei nomi può anche definire i descrittori di sicurezza per lo spazio dei nomi includendo il qualificatore NamespaceSecuritySDDL con il descrittore di sicurezza nel formato SDDL (Security Descriptor Definition Language).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004e1897553ef2ec0bd57067b17d714f6aaf8b17059c1078a2fc0da8a060a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315638"
---
# <a name="setting-security-on-namespace-creation"></a>Impostazione della sicurezza durante la creazione dello spazio dei nomi

Il file Managed Object Format (MOF) che crea uno [](/windows/desktop/SecGloss/s-gly) spazio dei nomi può anche definire i descrittori di sicurezza per lo spazio dei nomi includendo il qualificatore **NamespaceSecuritySDDL** con il descrittore di sicurezza nel formato [SDDL (Security Descriptor Definition Language).](/windows/desktop/SecAuthZ/security-descriptor-definition-language)

È possibile usare **NamespaceSecuritySDDL per** proteggere qualsiasi spazio dei nomi. È anche possibile usare questo qualificatore in un semplice file MOF per modificare il descrittore di sicurezza in uno spazio dei nomi esistente. La stringa SDDL viene elaborata da WMI per stabilire la sicurezza dello spazio dei nomi, ma non viene archiviata come stringa. Se non viene specificato alcun descrittore di sicurezza, viene usata la sicurezza predefinita. Per altre informazioni, vedere [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md)(Impostazione dei descrittori di sicurezza diPace).

La procedura seguente imposta il descrittore di sicurezza per lo spazio dei *\\ nomi MyNamespace* radice. La stringa SDDL imposta il proprietario e il gruppo per gli utenti autenticati e specifica un elenco di controllo di accesso discrezionale [*ereditato*](/windows/desktop/SecGloss/d-gly) dagli spazi dei nomi figlio. L'elenco DACL consente all'utente di leggere i dati, eseguire metodi, scrivere dati nelle classi provider e usare l'accesso remoto: **WBEM \_ ENABLE,** **WBEM \_ METHOD \_ EXECUTE,** **WBEM \_ WRITE \_ PROVIDER,** **WBEM \_ REMOTE \_ ACCESS.** Per altre informazioni, vedere [Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).

**Per impostare un elenco DACL dello spazio dei nomi**

1.  Creare un file MANAGED OBJECT FORMAT (MOF) o modificare il file MOF esistente che definisce lo spazio dei nomi per aggiungere il qualificatore **NamespaceSecuritySDDL** con la stringa SDDL.

    L'esempio di codice seguente mostra che lo spazio dei nomi da modificare è MyNamespace radice e \\ il file è denominato MyNamespace \_ security.mof.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Tenere presente che la stringa SDDL fa distinzione tra maiuscole e minuscole: le lettere devono essere in maiuscolo.

    L'esempio di codice seguente mostra le lettere "o" e "g" nella stringa SDDL come minuscole e Mofcomp.exe restituirà un errore.

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

    **c: \\ mofcomp MyNamespace \_ security.mof**

    In C++ usare i metodi [**IMoFCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

4.  Se il tentativo di impostare l'elenco DACL dello spazio dei nomi ha esito negativo, considerare i messaggi di errore seguenti:

    

    | Errore                           | Descrizione                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **PARAMETRO WBEM \_ E \_ NON \_ VALIDO** | Non è presente alcun elenco DACL ereditato. In alternativa, il chiamante ha violato l'elenco DACL o l'unità SD nello spazio dei nomi padre. |
    | **ACCESSO WBEM \_ E \_ \_ NEGATO**     | Il chiamante non dispone dell'autorizzazione per aggiornare il file SDDL in MOF.                                               |

    

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dei descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Costanti dei diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md)
</dt> <dt>

[**Costanti del flag ACE dello spazio dei nomi**](namespace-ace-flag-constants.md)
</dt> <dt>

[Modifica della sicurezza degli accessi per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
