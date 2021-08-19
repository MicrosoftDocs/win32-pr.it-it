---
description: Dopo aver creato un'estensione dello snap-in degli allegati, è necessario registrarla per consentire a MMC e agli snap-in Di configurazione della sicurezza di individuarlo e usarlo.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrazione di un'estensione snap-in allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7af8b586f0071a5718b420612fd552d578bf30bb083cca45a43f38198e1aee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005019"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registrazione di un'estensione snap-in allegati

Dopo aver creato un'estensione dello snap-in degli allegati, è necessario registrarla per consentire a MMC e agli snap-in Di configurazione della sicurezza di individuarlo e usarlo.

Lo snap-in degli allegati deve estendere lo spazio dei nomi degli snap-in Di configurazione della sicurezza aggiungendo il proprio nodo come descritto nella procedura seguente.

**Per installare e registrare l'estensione dello snap-in degli allegati**

1.  Registrare l'estensione dello snap-in nella chiave del Registro di sistema seguente. Non creare una chiave StandAlone nello snap-in. Le estensioni degli snap-in degli allegati devono essere solo estensioni.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Registrare l'estensione dello snap-in degli allegati nelle sottochiavi seguenti. Questa operazione può essere eseguita come parte delle implementazioni delle funzioni **DllRegisterServer** e **DllUnregisterServer.**

    [Spazio dei nomi dei modelli di](security-templates.md) sicurezza:

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

    [Spazio dei nomi Analisi e configurazione della](security-configuration-and-analysis.md) sicurezza:

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

 

 



