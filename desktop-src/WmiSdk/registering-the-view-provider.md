---
description: WMI registra automaticamente la DLL del provider di visualizzazione durante il processo di installazione wmi. Tuttavia, è comunque necessario registrare il provider di visualizzazione con WMI per ogni spazio dei nomi che conterrà le classi di visualizzazione.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrazione del provider di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a119816d388e07f1f032557af1171bb2666ef02a63d959b843b99b7942a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992461"
---
# <a name="registering-the-view-provider"></a>Registrazione del provider di visualizzazione

WMI registra automaticamente la DLL del provider di visualizzazione durante il processo di installazione wmi. Tuttavia, è comunque necessario registrare il provider di visualizzazione con WMI per ogni spazio dei nomi che conterrà le classi di visualizzazione.

La procedura seguente descrive come registrare il provider di visualizzazione.

**Per registrare il provider di visualizzazione**

1.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) per descrivere l'implementazione del provider di visualizzazione.

    [**\_ \_ L'istanza Win32Provider**](--win32provider.md) descrive il nome del provider e il relativo identificatore di classe (CLSID), nonché le impostazioni di sicurezza predefinite.

    Nell'esempio di codice seguente viene descritta un'implementazione di [**\_ \_ Win32Provider**](--win32provider.md).

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  Creare un'istanza della [**\_ \_ classe InstanceProviderRegistration.**](--instanceproviderregistration.md)

    Nell'esempio di codice seguente viene illustrato come creare un'istanza della **\_ \_ classe InstanceProviderRegistration.**

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  Creare un'istanza della [**\_ \_ classe MethodProviderRegistration**](--methodproviderregistration.md) se si vogliono usare i metodi di supporto della classe di visualizzazione unione.

    Nell'esempio di codice seguente viene illustrato come creare un'istanza della **\_ \_ classe MethodProviderRegistration.**

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Compilare il codice MOF usando il compilatore MOF ([mofcomp](mofcomp.md)) o [**l'interfaccia IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

    Se si salva l'esempio di codice MOF elencato in precedenza in un file denominato Viewtest.mof, usare il comando Mofcomp per caricare il codice MOF nello spazio dei nomi di destinazione. *NamespacePath è* lo spazio dei nomi in cui si vuole creare l'istanza della classe di visualizzazione.

    Digitare il comando seguente al prompt dei comandi per caricare il codice MOF nello spazio dei nomi di destinazione.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Per altre informazioni, vedere [Compilazione di file MOF](compiling-mof-files.md).

Per altre informazioni, vedere [Registrazione di un provider](registering-a-provider.md).

 

 



