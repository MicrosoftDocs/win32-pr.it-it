---
description: Dopo aver creato un'estensione dello snap-in allegati, è necessario registrarla affinché gli snap-in MMC e configurazione di sicurezza vengano individuati e usati.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrazione di un'estensione dello snap-in allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306425"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registrazione di un'estensione dello snap-in allegati

Dopo aver creato un'estensione dello snap-in allegati, è necessario registrarla affinché gli snap-in MMC e configurazione di sicurezza vengano individuati e usati.

Lo snap-in allegato deve estendere lo spazio dei nomi degli snap-in configurazione di sicurezza aggiungendo il proprio nodo, come descritto nella procedura seguente.

**Per installare e registrare l'estensione dello snap-in allegati**

1.  Registrare l'estensione dello snap-in nella seguente chiave del registro di sistema. Non creare una chiave autonoma nello snap-in; le estensioni degli snap-in allegati devono essere solo estensioni.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Registrare l'estensione dello snap-in allegati nelle sottochiavi seguenti. Questa operazione può essere eseguita come parte delle implementazioni delle funzioni **DllRegisterServer** e **DllUnregisterServer** .

    Spazio dei nomi [modelli di sicurezza](security-templates.md) :

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    [Configurazione della sicurezza e](security-configuration-and-analysis.md) spazio dei nomi di analisi:

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



