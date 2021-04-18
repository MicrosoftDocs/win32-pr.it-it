---
description: In alcuni casi potrebbe essere necessario installare una versione più recente di un provider in un sistema in esecuzione.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Aggiornamento di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315191"
---
# <a name="updating-a-provider"></a>Aggiornamento di un provider

In alcuni casi potrebbe essere necessario installare una versione più recente di un provider in un sistema in esecuzione. Se il provider è installato come DLL, è possibile installare un nuovo provider senza dover riavviare il servizio, riavviare il computer o influire in altro modo sulle applicazioni che utilizzano WMI in quel momento.

Nella procedura riportata di seguito viene descritto come aggiornare un provider.

**Per aggiornare un provider**

1.  Compilare il nuovo provider.

    1.  Compilare il nuovo provider con un nome di DLL diverso e un **CLSID** diverso.

        Modificare, ad esempio, Myprov.dll in Myprov1.dll e **CLSID \_ MyProProv** in **CLSID \_ diprov** 1.

    2.  Modificare il file MOF di registrazione del provider in modo da utilizzare il nuovo CLSID (CLSID \_ MyProv1), ma lo stesso nome del provider ("prov").

2.  Installare il nuovo provider.

    1.  Copiare la nuova DLL del provider con il nuovo nome insieme a quello precedente.
    2.  Registrare autonomamente il nuovo provider.

        Ad esempio, usare il comando **regsvr32** **myprov1.dll** per registrare il nuovo provider.

    3.  Compilare il nuovo MOF di registrazione del provider, sovrascrivendo quindi la registrazione del provider precedente. Fino a questo punto, il vecchio provider era completamente funzionante; il nuovo provider è ora completamente operativo.

3.  Rimuovere la versione precedente del provider, se necessario.

    1.  Annulla la registrazione della DLL precedente.

        Usare, ad esempio, il comando **regsvr32** **/umyprov.dll** per annullare la registrazione della dll precedente.

    2.  Contrassegnare la vecchia DLL da eliminare al riavvio chiamando [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).

Per aggiornare un provider implementato da server locale, è possibile eseguire una procedura simile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> </dl>

 

 
