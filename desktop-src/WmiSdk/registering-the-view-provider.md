---
description: WMI registra automaticamente la DLL del provider di visualizzazione durante il processo di installazione di WMI. Tuttavia, è comunque necessario registrare il provider di visualizzazione con WMI per ogni spazio dei nomi che conterrà le classi di visualizzazione.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrazione del provider di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318537"
---
# <a name="registering-the-view-provider"></a>Registrazione del provider di visualizzazione

WMI registra automaticamente la DLL del provider di visualizzazione durante il processo di installazione di WMI. Tuttavia, è comunque necessario registrare il provider di visualizzazione con WMI per ogni spazio dei nomi che conterrà le classi di visualizzazione.

Nella procedura riportata di seguito viene descritto come registrare il provider di viste.

**Per registrare il provider di visualizzazione**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) per descrivere l'implementazione del provider di visualizzazione.

    L'istanza di [**\_ \_ Win32Provider**](--win32provider.md) descrive il nome del provider e il relativo identificatore di classe (CLSID), nonché le impostazioni di sicurezza predefinite.

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

2.  Creare un'istanza della classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

    Nell'esempio di codice seguente viene illustrato come creare un'istanza della classe **\_ \_ InstanceProviderRegistration** .

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

3.  Creare un'istanza della classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) se si desidera che i metodi di supporto della classe Union View.

    Nell'esempio di codice seguente viene illustrato come creare un'istanza della classe **\_ \_ MethodProviderRegistration** .

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Compilare il codice MOF usando il compilatore MOF ([mofcomp](mofcomp.md)) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Se si salva l'esempio di codice MOF elencato in precedenza in un file denominato Viewtest. mof, utilizzare il comando mofcomp per caricare il codice MOF nello spazio dei nomi di destinazione. *NamespacePath* è lo spazio dei nomi in cui si desidera creare l'istanza della classe di visualizzazione.

    Al prompt dei comandi digitare il comando seguente per caricare il codice MOF nello spazio dei nomi di destinazione.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).

 

 



