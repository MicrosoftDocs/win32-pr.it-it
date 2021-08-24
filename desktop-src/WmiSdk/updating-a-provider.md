---
description: In alcuni casi potrebbe essere necessario installare una versione più recente di un provider in un sistema in esecuzione.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Aggiornamento di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8c40a3d50672115478ae62135774f5a1aad93373bd5b844402e89462b44fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757651"
---
# <a name="updating-a-provider"></a>Aggiornamento di un provider

In alcuni casi potrebbe essere necessario installare una versione più recente di un provider in un sistema in esecuzione. Se il provider è installato come DLL, è possibile installare un nuovo provider senza dover riavviare il servizio, riavviare il computer o influire in altro modo sulle applicazioni che usano WMI in quel momento.

Nella procedura seguente viene descritto come aggiornare un provider.

**Per aggiornare un provider**

1.  Compilare il nuovo provider.

    1.  Compilare il nuovo provider con un nome dll diverso e un **CLSID diverso.**

        Ad esempio, modificare Myprov.dll in Myprov1.dll e **CLSID \_ MyProProv** in **CLSID \_ MyProv** 1.

    2.  Modificare il file MOF di registrazione del provider in modo da usare il nuovo CLSID (CLSID MyProv1), ma lo stesso \_ nome del provider ("MyProv").

2.  Installare il nuovo provider.

    1.  Copiare la nuova DLL del provider con il nuovo nome insieme a quello precedente.
    2.  Registrare automaticamente il nuovo provider.

        Ad esempio, usare il **comando regsvr32** **myprov1.dll** per registrare il nuovo provider.

    3.  Compilare il file MOF di registrazione del nuovo provider, sovrascrivendo così la registrazione del provider precedente. Fino a questo punto, il provider precedente era completamente funzionante; ora il nuovo provider è completamente operativo.

3.  Rimuovere la versione precedente del provider, se necessario.

    1.  Annullare la registrazione della DLL precedente.

        Ad esempio, usare il **comando regsvr32** **/umyprov.dll** per annullare la registrazione della DLL precedente.

    2.  Contrassegnare la DLL precedente da eliminare al riavvio chiamando [**MoveFileEx.**](/windows/desktop/api/winbase/nf-winbase-movefileexa)

È possibile eseguire una procedura simile per aggiornare un provider locale implementato dal server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione dei descrittori di sicurezza namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> </dl>

 

 
